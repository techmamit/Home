# Spring Notes

### Spring Libraries download
> https://repo.spring.io/release/org/springframework/spring/

### Sample application Context file

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:c="http://www.springframework.org/schema/c"
    xmlns:p="http://www.springframework.org/schema/p" xmlns:context="http://www.springframework.org/schema/context"
    xsi:schemaLocation="http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans-4.1.xsd
    http://www.springframework.org/schema/context
    http://www.springframework.org/schema/context/spring-context-4.1.xsd">
    
    <!-- Adding properties file -->
    <context:property-placeholder location= "classpath:sports.properties"/>
    
    <!-- Adding Beans -->
	<bean id="myFortune" class="com.akv.spring.ioc.xml.demo.HappyFortuneService"/>
	<bean id="MyCoach" class="com.akv.spring.ioc.xml.demo.CricketCoach">
	
	     <!-- injecting Constructor dependencies -->
		<!-- <constructor-arg ref="myFortune"></constructor-arg> -->
		
	    <!-- injecting Setter dependencies -->
		<property name="fortuneService" ref="myFortune"></property>
		
	    <!-- injecting literals  -->
		<property name="email" value="akv@hotmail.com"/>
		<property name="team" value="hyderabad Sunrisers"/>

	    <!-- injecting literals from properties file -->		
		<property name="captain" value="${akv.captain}"/>
	
	</bean>

</beans>

```

### Sample App Class
```

package com.akv.spring.ioc.xml.demo;

import org.springframework.context.support.ClassPathXmlApplicationContext;

public class CricketCoachApp {
	
	public static void main(String args[]) {
		
		ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
		
		CricketCoach coach = context.getBean("MyCoach",CricketCoach.class);
		
		coach.getDailyWorkout();
		
		coach.getDailyFortune();
		
		System.out.println(coach.getEmail());
		
		System.out.println(coach.getTeam());
		
		System.out.println(coach.getCaptain());
		
		context.close();
		
	}	
}



```
