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
3. Retrieve Beans from Container 
```java
// Create a spring container
ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");

// Retrieve bean from spring container
Coach theCoach = context.getBean("myCoach", Coach.class);
```

## Dependency Injection
The client delegates to calls to another object the responsibility of providing its dependencies.
 
**Constructor Injection**
1. Define the dependency interface and class
```java
public interface FortuneService {
  public String getFortune();
}

public class HappyFortuneService implements FortuneService {
  public String getFortune() {
    return "No fortune";
  }
}
```
