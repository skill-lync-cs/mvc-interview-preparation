---
marp : true
---
# $~~~~~~~~~~~~~$ Microservices Interview preparation
---
# $~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~$Spring
---

- ## What is Loose Coupling?
- ## What is a Dependency?
- ## What is IOC (Inversion of Control)?
- ## What is Dependency Injection, Can you give few examples of Dependency Injection?
- ## What is Auto Wiring?
- ## What are Bean Factory and Application Context?


---
- ## How do you create an application context with Spring?
- ## What is a Component Scan?
- ## What does @Autowired signify?
- ## What is the default scope of a bean?
- ## Are Spring beans thread safe? 
- ## What are the different types of dependency injections?
---
- ## What is the difference between XML and Java Configurations for Spring? 
- ## How do you debug problems with Spring Framework? 
- ## What are important Spring Modules?
- ## Name some of the design patterns used in Spring Framework?
- ## What do you think about Spring Framework? 
---
- ### What is Loose Coupling?
``` 
Loose coupling is a software design principle that 
aims to minimize dependencies between components in a 
system, allowing them to operate independently and be 
easily replaced or modified without affecting the rest 
of the system.

```
---
- ### What is a Dependency?
```
In Spring, a dependency is a Java object that is 
needed by a component to perform its function, and is 
injected into the component using the Spring 
dependency injection framework. Spring manages the 
dependencies between the components of a Spring-based 
application, allowing for loose coupling and easier 
testing and maintenance of the code. Dependencies in 
Spring are typically defined in a configuration file 
or via annotations, and can be automatically injected 
into components at runtime by Spring's dependency 
injection mechanism.

```
---
- ### What is Dependency Injection, Can you give few examples of Dependency Injection?
```
Dependency Injection is a software design pattern that 
allows objects to be created and configured dynamically by 
an external framework or container, rather than being 
instantiated and configured by the objects themselves. In 
Dependency Injection, the objects specify their 
dependencies as interfaces, and the framework provides the 
concrete implementation of those interfaces at runtime, 
without requiring the objects to know about the specific 
implementation details.
Overall, Dependency Injection helps to reduce the 
complexity of managing dependencies in large software 
applications, making it easier to maintain and test the 
code.
```
---
- ### What is IOC (Inversion of Control)?
```
In Spring IOC, the control of the flow of an application is 
inverted or flipped from the application itself to the 
Spring container, which takes care of instantiating and 
configuring objects, and managing their dependencies.

Spring IOC is typically configured using an XML file or 
annotations, which specify the dependencies between 
objects, and allow Spring to automatically wire the objects 
together at runtime.

```
---
- ### What is Auto Wiring?
```
In Spring, Autowiring is a feature that allows Spring to 
automatically wire together the dependencies of beans 
(objects) in a Spring-based application. Autowiring 
eliminates the need for manual wiring of beans by 
automatically detecting the dependencies and injecting them 
at runtime.
Spring can also use annotations such as @Autowired, 
@Qualifier, and @Resource to specify the dependencies.
```
---
- ### What are Bean Factory and Application Context?
```
Both Bean Factory and Application Context are configurable 
using XML files or Java annotations, and allow developers 
to define and configure beans and their dependencies. The 
choice between using Bean Factory and Application Context 
depends on the specific requirements of the application, 
with Bean Factory being a good choice for simple 
applications, and Application Context being more suitable
for larger and more complex applications.

```

---
- ### How do you create an application context with Spring?
``` 
To create an application context with Spring, you typically 
need to perform the following steps:

Choose a type of application context to create, such as 
AnnotationConfigApplicationContext or ClassPathXmlApplicationContext.

Create an instance of the chosen application context class.

Use the application context to retrieve any required 
components or beans.

```
```
// Create an instance of the AnnotationConfigApplicationContext class
AnnotationConfigApplicationContext context = new AnnotationConfigApplicationContext();
```
---
- ### What is a Component Scan?
```
In Spring, component scanning is a feature that allows the framework to automatically 
discover and register beans based on classpath scanning.

By using component scanning, you can avoid the need to explicitly configure individual 
beans in your Spring configuration files. Instead, you can simply annotate your classes 
with certain annotations (such as @Component, @Service, @Controller, or @Repository), 
and Spring will automatically detect and register those classes as beans.

```
---
- ### What does @Autowired signify?
```
In Spring, the @Autowired annotation is used to automatically wire (i.e., inject) 
 dependencies into a bean.
 
When you annotate a field, constructor, or setter method with @Autowired, Spring will 
look for a matching bean of the required type in the application context, and 
automatically wire it into the annotated component.
```
---
- ### What is the default scope of a bean?
```
In Spring, the default scope of a bean is singleton.

This means that by default, Spring will create a single instance of the bean and share
it across all the application's components that require it. Whenever a component 
requests the bean from the application context, Spring will return the same shared 
instance.


For example, consider the following class:
@Service
public class MyService {
}

In this example, MyService is annotated with @Service, which is a specialization of the
@Component annotation. By default, Spring will create a single instance of MyService 
and share it across all the components that require it.

```
---
- ### Are Spring beans thread safe? 
```
It depends on the implementation and scope of the bean. By default, Spring beans are 
singleton-scoped and shared across threads, so if a bean maintains mutable state, it 
may not be thread-safe. To ensure thread-safety, synchronization or other thread-safe
techniques can be used, or a different scope, such as prototype scope, can be used to 
avoid shared mutable state.

```
---
- ### What are the different types of dependency injections?
```
There are three main types of dependency injection:

Constructor Injection: Dependencies are injected through a class constructor. This is 
the most commonly used type of injection.

Setter Injection: Dependencies are injected through a setter method of the class.

Interface Injection: Dependencies are injected through an interface that is implemented 
by the class. This type of injection is less common than the other two.
```


---
- ### What is the difference between XML and Java Configurations for Spring? 
```
Both approaches have their advantages and disadvantages. XML Configuration is more 
flexible and can be easier to manage for larger projects. Java Configuration is more
concise, readable, and can benefit from the type-safety of the Java language. 
Ultimately, the choice between the two depends on the specific needs of the project and 
personal preferences.

```
---
- ### How do you debug problems with Spring Framework? 
```
Debugging problems with Spring Framework involves the following steps:

Check the logs: Spring Framework logs detailed information about its operations and any 
issues that occur. Checking the logs can help identify the root cause of the problem.

Review the code: Review the code to ensure that it is correctly configured and that the 
dependencies are properly injected.

Check the configuration: Review the Spring configuration files or Java code to ensure 
that the application context is correctly configured.

Use debugging tools: Use a debugger to step through the code and identify the specific 
location where the problem is occurring. Tools like Eclipse or IntelliJ IDEA provide 
debugging support for Spring applications.

Check external dependencies: Verify that any external dependencies, such as databases 
or web services, are correctly configured and accessible.

Seek help from the community: If the problem is complex, seek help from the Spring 
community by posting on forums or using other support channels.
```
---
- ### What are important Spring Modules?
```
Spring is a very comprehensive framework with many modules that provide different 
functionalities for building enterprise applications. Some of the most important Spring
modules are:

Spring Core: This module provides the basic features of the Spring framework, including 
the Inversion of Control (IoC) container and the Dependency Injection (DI) mechanism.

Spring MVC: This module provides a web framework for building web applications, with 
support for handling requests, processing views, and managing the application flow.

Spring Data: This module provides a consistent and simple programming model for data 
access, with support for many different types of data stores, such as relational 
databases, NoSQL databases.

Spring Security: This module provides a comprehensive security framework for protecting 
web applications and services, with support for authentication, authorization, and 
secure communication.
```
---
```
Spring Integration: This module provides support for building integration solutions, 
such as messaging systems, ETL pipelines, and event-driven architectures.

Spring Cloud: This module provides tools and frameworks for building and deploying 
cloud-native applications, with support for service discovery, configuration 
management, and distributed tracing.

Spring Boot: This module provides a set of opinionated configurations and conventions 
for building Spring applications, with the goal of reducing development time and 
increasing productivity.

These are just a few examples of the many Spring modules available. Each module 
provides a specific set of features and functionalities, allowing developers to choose 
the ones that best fit their project requirements.
```
---
- ### Name some of the design patterns used in Spring Framework?
```
Spring Framework makes use of several design patterns to provide a flexible and 
extensible architecture for building enterprise applications. Some of the design 
patterns used in Spring Framework are:

Dependency Injection (DI): Spring makes extensive use of the DI pattern to inject 
dependencies into components, decoupling the dependencies and providing flexibility in 
component configuration.

Singleton Pattern: Many of the Spring beans are configured as singletons, ensuring that
only one instance of a particular bean is created and shared across the application.

Template Method Pattern: Spring uses the template method pattern in its core JDBC and 
Hibernate support to provide a consistent way of performing database operations.

Proxy Pattern: Spring uses the proxy pattern extensively to provide AOP 
(Aspect-Oriented Programming) features such as transaction management, caching, and 
security.
```
---
- ### What do you think about Spring Framework? 
```
Spring Framework is a widely used open-source framework for building enterprise 
applications in Java. It provides a comprehensive set of features and functionalities 
for building scalable, flexible, and robust applications. Spring Framework makes use of 
many design patterns and architectural principles to provide a modular and extensible 
architecture, which simplifies application development and maintenance.
```