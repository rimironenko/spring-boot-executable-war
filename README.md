# spring-boot-executable-war

## About the application

A sample app of a Spring Boot web application which runs as an executable WAR instead of JAR. May be useful for anyone who is planning to use Spring Boot for a legacy Spring/Java app.

## Highlights

- Packaging is `war`
- [Main.java](src/main/java/com/home/ross/spring/Main.java) main class is specified in the configuration of spring-boot-maven-plugin
- The main class extends `org.springframework.boot.web.servlet.support.SpringBootServletInitializer` class and overrides `org.springframework.boot.web.servlet.support.SpringBootServletInitializer.configure` method
- [pom.xml](pom.xml) contains `org.apache.tomcat.embed:tomcat-embed-jasper` and `javax.servlet:jstl` dependencies for JSP rendering
- [application.properties](src/main/resources/application.properties) contains Spring MVC properties to use JSP inside `WEB-INF` folder to render application pages

## Build the application

- Build and package the application via `mvn clean package` command
- Move to the `target/` folder
- Run the application via `java -jar spring-boot-executable-war.war` command
