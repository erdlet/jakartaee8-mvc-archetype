# JavaEE 8 & MVC 1.0 archetype

This archetype generates a basic MVC application based on JavaEE 8 and the current SNAPSHOT version of
the MVC API and Eclise Krazo.

## Usage

1) Download the archetype and run `mvn clean install` because it is not pushed to any repository at the moment.

2)
To generate a MVC application with **Jersey** as JAX-RS implementation (Glassfish, Payara):

```shell script
mvn archetype:generate \
    -DarchetypeGroupId=de.erdlet \
    -DarchetypeArtifactId=jee8-mvc-archetype \
    -DarchetypeVersion=1.0-SNAPSHOT  \
    -DgroupId=<your-groupId> \
    -DartifactId=<your-DartifactId>
```

To generate a MVC application with **RESTEasy** as JAX-RS implementation (Wildfly):

```shell script
mvn archetype:generate \
    -DarchetypeGroupId=de.erdlet \
    -DarchetypeArtifactId=archetype-jee8-mvc \
    -DarchetypeVersion=1.0-SNAPSHOT \
    -DgroupId=<your-groupId> \
    -DartifactId=<your-DartifactId> \
    -DkrazoImpl=resteasy
```

To generate a MVC application with **CXF** as JAX-RS implementation (TomEE):

```shell script
mvn archetype:generate \
    -DarchetypeGroupId=de.erdlet \
    -DarchetypeArtifactId=archetype-jee8-mvc \
    -DarchetypeVersion=1.0-SNAPSHOT \
    -DgroupId=<your-groupId> \
    -DartifactId=<your-DartifactId> \
    -DkrazoImpl=cxf
```

In case no JAX-RS implementation is select or none of the above mentioned is used, the
archetype will use **Jersey** as default.
