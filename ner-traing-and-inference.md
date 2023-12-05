---
title: NER Training and Inference
---

/ [Home](index.md)

## Training
```
git clone git@github.com:rajasgs/ecolab-ner-csp.git
cd ecolab-ner-csp
conda activate py39
pip install -r requirements.txt

python ner.py
  this will create a model file (sample: ecolab_address_20231026_1.model.ser.gz)
```

## verify javac and java version
```
javac --version
javac 11.0.21

java --version
openjdk 11.0.21 2023-10-17
OpenJDK Runtime Environment (build 11.0.21+9-post-Ubuntu-0ubuntu120.04)
OpenJDK 64-Bit Server VM (build 11.0.21+9-post-Ubuntu-0ubuntu120.04, mixed mode, sharing)
```

## Create Java for Testing
```
git clone git@github.com:rajasgs/nerinference-migration.git
cd nerinference-migration

javac -d . -cp "./resource_files/jars/*:." PredictNER.java

java -cp "./resource_files/jars/*" batch/code/ner/PredictNER "./models/ecolab_address_20231026_1.model.ser.gz" "1421-2030 Spadina Road" "STREET_NAME,HOUSE_NO,SUITE_NO"

You should see something like this:
  Loading classifier from ./models/ecolab_address_20231026_1.model.ser.gz ... done [0.1 sec].
  STREET_NAME=- Spadina Road
  HOUSE_NO=1421 2030
  SUITE_NO=null

```

## How to make custom Jar?
```
jar cvf ./resource_files/jars/rner_202312051.jar batch/code/ner/PredictNER.class ./jars/stanford-ner.jar

You should see something like this:

added manifest
adding: batch/code/ner/PredictNER.class(in = 3362) (out= 1624)(deflated 51%)
adding: jars/stanford-ner.jar(in = 4661456) (out= 4341948)(deflated 6%)

ref:
https://stackoverflow.com/questions/25116532/does-the-javac-command-automatically-create-directories-specified-in-the-package
https://github.com/buildpacks/sample-java-app/tree/main/src/main/java/io/buildpacks/example/sample
https://www.baeldung.com/java-create-jar
```

## Testing with JAR and JPype
```
jar tf ./resource_files/jars/rner_202312051.jar

You shoule see something like this:
META-INF/
META-INF/MANIFEST.MF
batch/code/ner/PredictNER.class
jars/stanford-ner.jar
```
