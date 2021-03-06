## TP4 - Book library
Test Travis 

This project is a lightweight and easy-to-use skeleton to create a JEE application that uses [Apache TomEE](http://openejb.apache.org/apache-tomee.html), a complete JEE server based on Tomcat.

### Structure

  * `main/java/car/tp4/entity`
    
    Contains all entities (EJB) (`Book` bean example).
    
  * `main/java/car/tp4/servlet`
  
    Contains all servlets (`HelloServlet` example).
    
  * `resources/META-INF`
    
    Contains all the configuration files for the deployment.
    `persistence.xml` declares how to persist the app beans.
    We have to write a `persistence-unit` for each bean of the application.
    
  * `webapp/jsp`
  
  Contains all the jsp files, excepts the index.
  
  * `webapp/WEB-INF`
  
  Contains all the configuration files for the web application.
  The mapping between each URL/Servlet has to be down in the `web.xml` file (see example).

### How to?

To build the application and to start the server:
```
mvn clean package tomee:run
```

Once started, the application is now reachable at:
```
http://localhost:8080
```

A Servlet and a JSP file is available for testing at:
```
http://localhost:8080/hello
```

When developing, all the static resources (html, css, jsp) are automatically re-deployed on the server (in few seconds).

For the Java class, you can open a new terminal (without to stop the server), and package the application (`mvn package`) for a new automatic redeployment.

To clean all data and remove the application, use `mvn:clean`.
 