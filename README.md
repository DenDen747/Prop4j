Latest release: [Prop4j_1.3.jar](https://github.com/DenDen747/Prop4j/raw/main/builds/Prop4j_1.3.jar)
# Prop4j
Reading and writing to properties files can be a hassle with Java, that's why I've create Prop4j. Prop4j makes it really easy and staight-forward to use propterties files.
## Registering a properties file
To register a properties file, you have to do the following:
```java
PropertiesFile propertiesFile = new PropertiesFile(path);
```
If you want a properties file to get returned regardless if it exists or doesn't, you can run the following method:

```java
PropertiesFile propertiesFile = PropertiesFile.returnObject(path);
```

This method returns the file if it exists, and creates a new one if it doesn't exist.

You can then run baic actions, like this:

```java
if(propertiesFile.exists) {
  //only happens if the file physically exists
}
```
## Reading
You can get the value of a key by doing the following:
```java
propertiesFile.getProperty(key);
```
## Writing
You can write to a properties file by doing the following:
```java
propertiesFile.setProperty(key, value);
//or if you want to add a comment
propertiesFile.setProperty(key, value, comment);
```
## Bulk actions
If you want to carry out multiple tasks at once, do the following:
```java
propertiesFile.getProperties(keys[]); //returns an arrays with values in order
propertiesFile.setProperties(keys[], values[]); //sets the keys with the corresponding values in order
propertiesFile.setProperties(keys[], values[], comment); //does the same thing except with a comment
```

