---
title: Java Commands
---

/ [Home](index.md)

# Java Commands

**Note:** tbw



## Run Javac
```
javac -d . -cp "./resource_files/jars/*:." PredictNER.java

```

## Verify class
```
javap batch/code/ner/PredictNER.class

You should see something like this:

Compiled from "PredictNER.java"
public class batch.code.ner.PredictNER {
    public batch.code.ner.PredictNER();
    public java.util.Map<java.lang.String, java.lang.String> getEntities(edu.stanford.nlp.ie.crf.CRFClassifier, java.lang.String);
    public java.lang.String getTokens(java.lang.String, java.lang.String);
    public static batch.code.ner.PredictNER getInstance(java.lang.String);
    public static void main(java.lang.String[]);
}
```

## Create Jar
```
jar cvf ./resource_files/jars/rner_202312051.jar batch/code/ner/PredictNER.class ./jars/stanford-ner.jar

You should see something like this:

added manifest
adding: batch/code/ner/PredictNER.class(in = 3362) (out= 1624)(deflated 51%)
adding: jars/stanford-ner.jar(in = 4661456) (out= 4341948)(deflated 6%)
```


## Verify 
```
jar tf ./resource_files/jars/rner_202312051.jar

You shoule see something like this:
META-INF/
META-INF/MANIFEST.MF
batch/code/ner/PredictNER.class
jars/stanford-ner.jar
```