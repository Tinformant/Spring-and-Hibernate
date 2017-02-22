# Spring-and-Hibernate

Inversion of Control: outsourcing the construction and management of objects.

**Spring Container**

Spring container is generally known as **ApplicationContext**.

Spcialized implementations:
* ClassPathXmlApplicationContext
* AnnotationConfigApplicationContext
* GenericWebApplicationContext

```java
ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
```
