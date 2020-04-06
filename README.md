# java-itextpdf-template
Learning Java Apache Maven iText

### Notes

Following the examples from [Itext 7 jump start tutorial java / Chapter 1](https://itextpdf.com/en/resources/books/itext-7-jump-start-tutorial-java/chapter-1).

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
