# Behind the scenes - Annotations

#### Spring Boot Application - @SpringBootApplication
	Used in the main class or bootstrap class and a single annotation is used to enable Auto configuration, component scan and do a extra configuration on the application class.

#### Auto Configuration - @EnableAutoConfiguration - 
	Spring Boot Auto configuration automatically configures your spring application based on the JAR dependencies added in your project.
	For Example : if MySQL DB is in your class path then spring boot auto configures an in memory database.

#### Component Scan - @ComponentScan
It scans all the beans and package declarations when the application initializes

#### SpringBootConfiguration - @SpringBootConfiguration
	Configuration – @Configuration  
		Allow to register extra beans in the context or import additional configuration classes

#### Request Mapping - @RequestMapping
This annotation maps HTTP requests to handler methods of MVC and REST controllers.
	It can be applied to class-level and/or method-level in a controller.

#### Componet- @Componet
A Java class decorated with @Component is found during classpath scanning and registered in the context as a Spring bean.
@Service, @Repository, and @Controller are specializations of @Component, which are used for more specific cases.

