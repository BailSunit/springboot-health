# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/3.2.2/maven-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/3.2.2/maven-plugin/reference/html/#build-image)
* [Spring Web](https://docs.spring.io/spring-boot/docs/3.2.2/reference/htmlsingle/index.html#web)
* [Spring Boot Actuator](https://docs.spring.io/spring-boot/docs/3.2.2/reference/htmlsingle/index.html#actuator)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)
* [Building a RESTful Web Service with Spring Boot Actuator](https://spring.io/guides/gs/actuator-service/)

### Actuator responses

1. GET request - localhost:8080/actuator</br>
    Response : 200 OK
   ```{
   "_links": {
   "self": {
   "href": "http://localhost:8080/actuator",
   "templated": false
   },
   "health-path": {
   "href": "http://localhost:8080/actuator/health/{*path}",
   "templated": true
   },
   "health": {
   "href": "http://localhost:8080/actuator/health",
   "templated": false
   }
   }
   }```
2. GET request - localhost:8080/actuator/health <br/>Response : 200 OK
```
{
    "status": "UP",
    "groups": [
        "liveness",
        "readiness"
    ]
}
```
3. GET request - localhost:8080/actuator/health/liveness <br/>Response : 200 OK
```
{
    "status": "UP"
}
```
4. GET request - localhost:8080/actuator/health/readiness <br/>Response : 200 OK
```
{
    "status": "UP"
}
```
