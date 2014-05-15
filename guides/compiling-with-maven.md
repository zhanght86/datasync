---
layout: with-sidebar
title: Compiling with Maven
bodyclass: homepage
---

DataSync uses Maven for building and package management. For more information: [What is Maven?](http://maven.apache.org/what-is-maven.html)

To build the project run:
```
mvn clean install
```

To compile the project into an executable JAR file (including all dependencies) run:
```
mvn clean compile assembly:single
```

Did it work? If not, you can always skip the tests:
```
mvn clean compile -Dmaven.test.skip=true assembly:single
```

This puts the JAR file into the "target" directory inside the repo.  So to open DataSync, simply run:
```
cd target
java -jar DataSync-1.0-jar-with-dependencies.jar
```