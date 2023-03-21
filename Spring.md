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
