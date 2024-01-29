---
title: Azure Container App
---

/ [Home](index.md)

# Azure Container App





### Clone and run Docker
```
git clone git@github.com:rajasgs/simple-flask.git
```


### V1:
```
docker build -t simple-flask-server:v1 .
docker run -p 9090:5000 --name simple-flask-server-112 simple-flask-server:v1

http://0.0.0.0:9090/


Push to DockerHub:

  docker build -t simple-flask-server:v1 .

  docker tag simple-flask-server:v1 rajacsp/simple-flask-server:v1
    
  docker push rajacsp/simple-flask-server:v1


Login to ACR:

  az login
  az acr login --name rjsimpleflask


Push to ACR:

  docker tag simple-flask-server:v1 rjsimpleflask.azurecr.io/simple-flask-server:v1

  docker push rjsimpleflask.azurecr.io/simple-flask-server:v1
```


### V2:
```
Push to DockerHub:

  docker build -t simple-flask-server:v2 .

  docker tag simple-flask-server:v2 rajacsp/simple-flask-server:v2
    
  docker push rajacsp/simple-flask-server:v2


Login to ACR:

  az login
  az acr login --name rjsimpleflask


Push to ACR:

  docker tag simple-flask-server:v2 rjsimpleflask.azurecr.io/simple-flask-server:v2

  docker push rjsimpleflask.azurecr.io/simple-flask-server:v2
```



### V1 - Create a new container app
```
#
verify:
az containerapp env list --resource-group rjresroucegroup


# how to create a container app
az containerapp up \
	  --name simple-flask-server-conapp-1 \
	  --resource-group rjresroucegroup \
	  --location centralindia \
	  --environment 'rjresroucegroup-env' \
	  --image rjsimpleflask.azurecr.io/simple-flask-server:v1 \
	  --target-port 5000 \
	  --ingress external \
	  --query properties.configuration.ingress.fqdn


	# verify
	az containerapp logs show -n simple-flask-server-conapp-1 -g rjresroucegroup --type system --tail 50

	az containerapp show -n simple-flask-server-conapp-1 -g rjresroucegroup


# Check revision
az containerapp revision list \
  --name simple-flask-server-conapp-1 \
  --resource-group rjresroucegroup \
  -o table

# Adding Label to the recent revision
az containerapp revision label add -n simple-flask-server-conapp-1 -g rjresroucegroup --label v1 --revision latest


# Update existing containerapp
az containerapp update \
  --container-name simple-flask-server-conapp-1 \
  --name simple-flask-server-conapp-1 \
  --resource-group rjresroucegroup \
  --image rjsimpleflask.azurecr.io/simple-flask-server:v1 \
  --min-replicas 1 \
  --max-replicas 5 \
  --query properties.configuration.ingress.fqdn

# Change revision mode
az containerapp revision set-mode \
  --name simple-flask-server-conapp-1 \
  --resource-group rjresroucegroup \
  --mode multiple
```


### V3
```
# Push to ACR:
docker build -t simple-flask-server:v3 .

docker tag simple-flask-server:v3 rjsimpleflask.azurecr.io/simple-flask-server:v3

docker push rjsimpleflask.azurecr.io/simple-flask-server:v3

# Update existing containerapp with v3
az containerapp update \
  --container-name simple-flask-server-conapp-1 \
  --name simple-flask-server-conapp-1 \
  --resource-group rjresroucegroup \
  --image rjsimpleflask.azurecr.io/simple-flask-server:v3 \
  --min-replicas 1 \
  --max-replicas 5 \
  --revision-suffix v3 \
  --query properties.configuration.ingress.fqdn

  verify:
  simple-flask-server-conapp-1.wittyfield-91da3b68.centralindia.azurecontainerapps.io


# Adding Label to the recent revision
az containerapp revision label add -n simple-flask-server-conapp-1 -g rjresroucegroup --label v3 --revision latest


# Split traffic
az containerapp ingress traffic set \
    --name simple-flask-server-conapp-1 \
    --resource-group rjresroucegroup \
    --label-weight v2=80 v3=20
```