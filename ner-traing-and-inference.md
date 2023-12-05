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

javac -d . -cp "./jars/*" PredictNER.java

java -cp "./jars/*" PredictNER.java "ecolab_address_20231026_1.model.ser.gz" "1421-2030 Spadina Road" "STREET_NAME,HOUSE_NO,SUITE_NO"
```

## How to make custom Jar?
```
custom-jar

jar tf ner.jar


javac -d . *.java
jar cvf rner.jar *


javac -d . -cp "jars/*:." PredictNER.java

javac -d . PredictNER.java 


https://www.baeldung.com/java-create-jar

java -cp rner.jar com.baeldung.jar.JarExample


java -cp "jars/*:." one.two.SimplePredictNER.java models/v1.model.ser.gz


ref:
https://stackoverflow.com/questions/25116532/does-the-javac-command-automatically-create-directories-specified-in-the-package
https://github.com/buildpacks/sample-java-app/tree/main/src/main/java/io/buildpacks/example/sample
https://www.baeldung.com/java-create-jar
```


## Create JAR File


## Testing with JAR and JPype

