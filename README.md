# Jakarta EE 8 & MVC 1.0 archetype
[![Maven Central](https://img.shields.io/maven-central/v/de.erdlet.archetypes/jakartaee8-mvc-archetype.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:%22de.erdlet.archetypes%22%20AND%20a:%22jakartaee8-mvc-archetype%22)

## About the archetype
This archetype generates a basic MVC application based on Jakarta EE 8 and the current release version of
the MVC API and Eclise Krazo.

## Usage

To generate a MVC application with **Jersey** as JAX-RS implementation (Glassfish, Payara):

```shell script
mvn archetype:generate \
    -DarchetypeGroupId=de.erdlet.archetypes \
    -DarchetypeArtifactId=jakartaee8-mvc-archetype \
    -DarchetypeVersion=1.0.0-Beta1  \
    -DgroupId=<your-groupId> \
    -DartifactId=<your-DartifactId>
```

To generate a MVC application with **RESTEasy** as JAX-RS implementation (Wildfly):

```shell script
mvn archetype:generate \
    -DarchetypeGroupId=de.erdlet.archetypes \
    -DarchetypeArtifactId=jakartaee8-mvc-archetype \
    -DarchetypeVersion=1.0.0-Beta1 \
    -DgroupId=<your-groupId> \
    -DartifactId=<your-DartifactId> \
    -DkrazoImpl=resteasy
```

To generate a MVC application with **CXF** as JAX-RS implementation (TomEE):

```shell script
mvn archetype:generate \
    -DarchetypeGroupId=de.erdlet.archetypes \
    -DarchetypeArtifactId=jakartaee8-mvc-archetype \
    -DarchetypeVersion=1.0.0-Beta1 \
    -DgroupId=<your-groupId> \
    -DartifactId=<your-DartifactId> \
    -DkrazoImpl=cxf
```

In case no JAX-RS implementation is select or none of the above mentioned is used, the
archetype will use **Jersey** as default.
