# sample-app

Minimal [Spring Boot](http://projects.spring.io/spring-boot/) sample app.

## Requirements

For building and running the application you need:

- [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Maven 3](https://maven.apache.org)

## Running the application locally

There are several ways to run a Spring Boot application on your local machine. One way is to execute the `main` method in the `com.example.demo.DemoApplication` class from your IDE.

Alternatively you can use the [Spring Boot Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins-maven-plugin.html) like so:

```shell
mvn spring-boot:run
```

## About the Service

The service is just a simple demo REST service. It uses an in-memory database (H2) to store the data. You can also do with a relational database like MySQL or PostgreSQL. If your database connection properties work, you can call some REST endpoints defined in ```com.example.demo.controller.UserController``` on **port 8080**. (see below)



### Create a user

```
POST /api/user
Content-Type: application/json
{
    "firstName":"Monik",
    "lastName":"Gandhi",
    "email":"monikdmnh@gmail.com"
}
RESPONSE: HTTP 200 (OK)
Location header: http://localhost:8080/api/user
```



### Create a user

```
POST /api/user
Content-Type: application/json
{
    "firstName":"Monik",
    "lastName":"Gandhi",
    "email":"monikdmnh@gmail.com"
}
RESPONSE: HTTP 200
Location header: http://localhost:8080/api/user
```


### Retrieve all user

```
GET /api/user
Response: HTTP 200
Location header: http://localhost:8080/api/user
Content: List of all user 
```
