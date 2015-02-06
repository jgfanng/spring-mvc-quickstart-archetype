# Spring MVC 4 Quickstart Maven Archetype

## Summary
This project is a Maven archetype for Spring MVC 4 web application.

## Prerequisites
* JDK 1.7+
* Servlet 3.1 compliant containers

## Install to local repository
Execute following commands to install the archetype to your local repository:
```
git clone https://github.com/jgfanng/spring-mvc-quickstart-archetype.git
cd spring-mvc-quickstart-archetype
mvn clean install
```

## Create a project in command line
Run maven command:
```
mvn archetype:generate \
    -DarchetypeGroupId=com.jgfanng \
    -DarchetypeArtifactId=spring-mvc-quickstart-archetype \
    -DarchetypeVersion=1.0.0 \
    -DgroupId=my.groupid \
    -DartifactId=my-artifactId \
    -Dversion=version \
    -Dpackage=my-package \
    -DarchetypeCatalog=local
```

For example:
```
mvn archetype:generate -DarchetypeGroupId=com.jgfanng -DarchetypeArtifactedId=spring-mvc-quickstart-archetype -DarchetypeVersion=1.0.0 -DgroupId=com.jgfanng -DartifactId=spring-mvc-hello-world -Dversion=0.0.1-SNAPSHOT -Dpackage=com.jgfanng.controller -DarchetypeCatalog=local
```
The folder structure will be like this:
```
spring-mvc-hello-world
│  pom.xml
│
└─src
   ├─main
   │  ├─java
   │  │  └─me
   │  │      └─jgfanng
   │  │          └─controller
   │  │                  HelloWorldController.java
   │  │
   │  ├─resources
   │  └─webapp
   │      │  index.jsp
   │      │
   │      └─WEB-INF
   │          │  dispatcher-servlet.xml
   │          │  web.xml
   │          │
   │          └─views
   │                  helloworld.jsp
   │
   └─test
       ├─java
       └─resources
```
Then import it as a Maven project in Eclipse.

## Creating a project in Eclipse

* Go to `Preferences > Maven > Archetypes` and `Add Local Catalog`
* Select the catalog from file (` ${user.home}/.m2/archetype-catalog.xml`) 
* Create a new Maven project and select spring-mvc-quickstart-archetype
