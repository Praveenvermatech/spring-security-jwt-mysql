# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/maven-plugin/)
* [Spring Data JPA](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/reference/htmlsingle/#boot-features-jpa-and-spring-data)
* [Spring Security](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/reference/htmlsingle/#boot-features-security)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.2.1.RELEASE/reference/htmlsingle/#boot-features-developing-web-applications)

### Guides
The following guides illustrate how to use some features concretely:

* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Securing a Web Application](https://spring.io/guides/gs/securing-web/)
* [Spring Boot and OAuth2](https://spring.io/guides/tutorials/spring-boot-oauth2/)
* [Authenticating a User with LDAP](https://spring.io/guides/gs/authenticating-ldap/)
* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)


### Consume Services
There are following services here:

### Register Service
http://localhost:8085/register 

Request body : 
{
  "username" : "Praveenverma",
  "password" : "pr@veen"
}

Response: 200 OK
{
"username": "praveenverma"
}

### Create Token Service
http://localhost:8085/authenticate

Request body : 
{
  "username" : "Praveenverma",
  "password" : "pr@veen"
}
  
Response: 200 OK
{
"token": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJBamVldCIsImV4cCI6MTU3NDE4NTM0MiwiaWF0IjoxNTc0MTY3MzQyfQ.qee9p__gtDZJ7CAGmCYtYI7Z1tqEYkOw0RJosg13dWh-K-t4T630qzKIjK1AwEVgT1JSf8xLkwWfn9RTcOW2Aw"
}   


### Consume hello world service with token:
http://localhost:8085/hello

header: authorization : Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJBamVldCIsImV4cCI6MTU3NDE4NTM0MiwiaWF0IjoxNTc0MTY3MzQyfQ.qee9p__gtDZJ7CAGmCYtYI7Z1tqEYkOw0RJosg13dWh-K-t4T630qzKIjK1AwEVgT1JSf8xLkwWfn9RTcOW2Aw

Response: Hello world  // 200 OK
