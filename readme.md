## Handling entities inheritance with Spring Data JPA

See more here: http://blog.netgloo.com/2014/12/18/handling-entities-inheritance-with-spring-data-jpa/


#1. Use undertow as web container
```	  
	  <dependency>
		  <groupId>org.springframework.boot</groupId>
		  <artifactId>spring-boot-starter-web</artifactId>
		  <exclusions>  
			<exclusion>
					<groupId>org.springframework.boot</groupId>
					<artifactId>spring-boot-starter-tomcat</artifactId>
			</exclusion>
		  </exclusions>
	  </dependency>
	  
	  <dependency>  
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-undertow</artifactId>
	 </dependency> 
```

#2. Mysql or H2 Memery DB config:

application.properites:

## Mysql:
```
# DataSource settings: set here configurations for the database connection
#Mysql
spring.datasource.url = jdbc:mysql://db-container:3306/spring-boot-test
spring.datasource.username = root
spring.datasource.password = root
```

## Memery:
```
#H2
spring.datasource.url = jdbc:h2:mem:datajpa
#spring.datasource.url = jdbc:h2:file:~/.h2/testdb  
spring.datasource.username = sa  
#spring.datasource.password = sa  
```