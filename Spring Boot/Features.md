# Features
#### AutoConfiguration
It detects the presence of certain a Class in the Classpath and then automatically configures it for you.

For example, if you have added the JDBC Template into your classpath and the H2.jar, then Spring Boot can automatically configure an in-memory database for you and a JDBC Template, which is ready to use. You don't need to write any above code to use the JDBC Template in your DAO layer.

The Auto-Configuration feature is, by default, disabled, and you need to enable it by using @EnableAutoConfiguration or the @SpringBootApplication annotation on your Configuration class.

#### Starter POMs & Dependency management
While AutoConfiguration takes away the pain of configuring common functionalities, the Starter POMs take away pain by finding and adding common dependencies in your project.

In order to build a simple Spring MVC-based REST application that supports Jackson and to run it an embedded container, you would at least need the following dependencies:
spring-core.jar
spring-web.jar
spring-webmvc.jar
jackson-databind.jar
tomcat-embed-core.jar
tomcat-embed-el.jar
tomcat-embed-logging-juil.jar

By using Spring Boot Starter POMs or starter dependency feature, you can get all of these by just adding spring-boot-starter-web dependency in your pom.xml or gradle file

So instead of adding all these dependencies and worrying about their compatible version, you just need to add one. You will also be more confident that tried and tested versions of libraries are used, and there won't be any incompatibility issue in future.

Another benefit of the starter POMs feature is that you don't need to remember or search dependencies. 

If you are building a web application, you can add a 'web' starter. 
If you are building a JPA application, you could add the 'JPA' starter by aggregating common dependencies and functionalities that Spring Boot has made easy to remember and use.

In short, Starter POMs or starter dependencies are another awesome feature of Spring Boot that really helps to simplify Spring application development. It's like a close cousin of auto-configuration and you will frequently use them together.

#### Spring Boot Initializer
Spring Initializer is another feature of Spring Boot that solves the problem with respect to project structure. It's a web application that allows you to generate a Maven or Gradle projects with Java, Kotlin, Groovy, or Spring Boot.

All you need to provide is the Project MetaData in GUI, e.g. name of your project, Group, Artifact, etc. It also allows you to choose a starter dependency from a big list, e.g. web, JPA, or security starter.

The Spring Initializer project can be accessed at https://start.spring.io/. Once you create a project, you can download the Zip file and then open into an IDE like Eclipse or IntelliJ IDEA. You can then edit this sample project to use with your code.

As per my experience, one of the common problems many Java and Spring developers face is how to start a project. Many of them are clueless about whether to put use your Java file, resource file, etc.

Though Maven, Gradle, IntelliJ IDEA, and Eclipse help to give you a basic structure, you still need to be proficient on those two skills to get a head start, and if you are not familiar with Maven or your IDE, it can be a nightmare.

Spring Boot Initaizer solves this problem and makes it easy to create a Spring-based Java application without really knowing about a lot of internal details of Spring framework.

#### Actuator
The actuator is another awesome feature of Spring Boot that allows seeing what's going on inside a running Spring Boot application. With all its goodness of auto-configuration, there comes a risk of not knowing what is inside your application and that risk is addressed by the Spring Actuator.

It provides a lot of insight and metrics about running applications in production. For example, by using Actuator, you can find out exactly which beans are configured in the Application context, what are auto-configuration decisions made, what environment variables, system properties, command line arguments are available to an application, and many more.

You can even get a trace of HTTP requests handled by the application, along with various useful application metrics, e.g. CPU and Memory usage, garbage collection details, web requests, and data source usage.

Spring Boot Actuator also provides several endpoints to retrieve this data, e.g. you can get all this using RESTful APIs

At the same time, you also need to secure access to Actuator endpoints because it not only exposes confidential information but also it's dangerous. For example, anyone can stop your application by using /shutdown endpoints.

Though, you don't need to worry. Like any other Spring application, you can use Spring Security to protect Actuator endpoints. 

#### Externalised Configuration
Using this feature enables the developer to work with the same application in different environments. From properties files, YAML files environmental variables arguments are taken to use directly to the beans either by @Value annotation or use @ConfigurationProperties for bounding to structured objects.
