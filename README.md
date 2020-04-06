# java-itextpdf-template
Learning Java Apache Maven iText

### Notes

Following the examples from [Itext 7 jump start tutorial java / Chapter 1](https://itextpdf.com/en/resources/books/itext-7-jump-start-tutorial-java/chapter-1).

* ``pom.xml``

[stackoverflow.com](https://stackoverflow.com/questions/10568275/noclassdeffounderror-on-maven-dependency)

- add ``maven-shade-plugin`` to build **uber-JAR**
- add ``maven-assembly-plugin`` (maybe not necessary at this point)
- add ``>maven-jar-plugin`` to define ``mainClass``
- ``maven-dependency-plugin`` was not necessary

