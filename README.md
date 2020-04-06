# java-itextpdf-template
Learning Java Apache Maven iText

#### Notes

Following the examples from [Itext 7 jump start tutorial java / Chapter 1](https://itextpdf.com/en/resources/books/itext-7-jump-start-tutorial-java/chapter-1).

#### Prerequisites

* Get **Maven**

```sh
brew install maven
```

* Create archetype

```sh
mkdir java-itextpdf-template
cd java-itextpdf-template
mvn archetype:generate -DgroupId=com.fourd.miyako.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```

**Note**: ``com.4D.miyako`` will fail! Use ``fourd`` not ``4D``.

* Get [iText 7 for Java](https://github.com/itext/itext7).  

```
cd kernel
mvn package
cd io
mvn package
cd layout
mvn package
```

* Get [Simple Logging Facade for Java](https://github.com/qos-ch/slf4j).  

```
cd slf4j-api
mvn package
```

##### Things to do for ``pom.xml``

- add ``maven-shade-plugin`` to build **uber-JAR** c.f. [stackoverflow.com](https://stackoverflow.com/questions/10568275/noclassdeffounderror-on-maven-dependency)
- add ``maven-jar-plugin`` to define ``mainClass``
- add iText ``kernel`` ``io`` ``layout`` c.f. [itextpdf.com](https://itextpdf.com/en/resources/installation-guides/installing-itext-7-java)
- adding ``maven-dependency-plugin`` was not necessary
- adding ``maven-assembly-plugin`` was not necessary

To package with maven:

```
cd my-app 
mvn package
```

To run:

```
cd target
java -jar my-app-1.0-SNAPSHOT.jar
```
