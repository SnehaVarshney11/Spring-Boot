# Spring-Boot
* Spring Boot is an open source Java-based framework used to create a micro Service.
* It is used to build stand-alone and production ready spring applications.
* Spring Boot provides a good platform for Java developers to develop a stand-alone and production-grade spring application that you can just run.
* <b> MicroServices:- </b> Micro Service is an architecture that allows the developers to develop and deploy services independently. 

### Advantages :- 
1. Easy to understand and develop spring applications.
2. Increases productivity
3. Reduces the development time

### Goals :-
1. To avoid complex XML configuration in Spring
2. To develop a production ready Spring applications in an easier way
3. To reduce the development time and run the application independently

### Why Spring Boot ?
1. It provides a flexible way to configure Java Beans, XML configurations, and Database Transactions.
2. It provides a powerful batch processing and manages REST endpoints.
3. In Spring Boot, everything is auto configured; no manual configurations are needed.

### How does it works ?
Spring Boot automatically configures your application based on the dependencies you have added to the project by using <b> @EnableAutoConfiguration </b> annotation.
```
E.g. If MySQL database is on your classpath, but you have not configured any database connection, then Spring Boot auto-configures an in-memory database.
```

**The entry point of the spring boot application is the class contains @SpringBootApplication annotation and the main method.** <br>
**Spring Boot automatically scans all the components included in the project by using @ComponentScan annotation.**

### Spring Boot Starters
To handle the dependency management is a difficult taks for big projects. Spring Boot resolves this problems by providing a set of dependencies.
```
For example, if you want to use Spring and JPA for database access, it is sufficient if you include spring-boot-starter-data-jpa dependency in your project.
```
_All Spring Boot starters follow the same naming pattern <b>spring-boot-starter- *</b>, where * indicates that it is a type of the application._

**Example:-** Spring Boot Starter Actuator dependency is used to monitor and manage your application. Its code is shown below −
```
<dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

### Auto Configuration:- 
Spring Boot Auto Configuration automatically configures your Spring application based on the JAR dependencies you added in the project. <br>
For this purpose, you need to add **@EnableAutoConfiguration** annotation or **@SpringBootApplication** annotation to your main class file. Then, your Spring Boot application will be automatically configured.<br>
Observe the following code for a better understanding −
```
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.EnableAutoConfiguration;

@EnableAutoConfiguration
public class DemoApplication {
   public static void main(String[] args) {
      SpringApplication.run(DemoApplication.class, args);
   }
}
```