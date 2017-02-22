# Spring-and-Hibernate

Inversion of Control: outsourcing the construction and management of objects.

**Spring Container**

Primary functions:
* Create and manage objects (Inversion of Control)
* Inject object's dependencies (Dependency Injection)

**Spring Development Process**

1. Configure Spring Beans
```xml
<beans>
  <bean id="myCoach"
    class="myPackage.BaseballCoach">
  </bean>
</beans>
```
2. Create a Spring Container
Spring container is generally known as **ApplicationContext**.

Spcialized implementations:
* ClassPathXmlApplicationContext
* AnnotationConfigApplicationContext
* GenericWebApplicationContext

```java
ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
```
