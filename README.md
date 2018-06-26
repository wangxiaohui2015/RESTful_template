# A simple RESTful template based on Spring MVC

## Description
This is a simple RESTful template, and based on Spring MVC, you can start from it for new project development.

## Setup environment
### Prerequisites
1. Install JDK 1.8.x  (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) and setup JAVA_HOME environment variable.
2. Install Maven 3.5.x (http://maven.apache.org/download.cgi) and setup PATH environment variable.
3. Install Tomcat 8.x (https://tomcat.apache.org/download-80.cgi)

### Building
``` shell
git clone git@cncdgitlab.ccoe.lab.emc.com:wangs56/RESTful_template.git
cd RESTful_template
mvn clean package
```

### Deployment
Copy file RESTful_template-1.0.0-RELEASE.war to \<Tomcat_Dir\>\webapps\

### Testing
1. Query one employee:
Method: GET
URL: http://localhost:8080/restful_template/employee/0

2. Query al employees:
Method: GET
URL: http://localhost:8080/restful_template/employee/

3. Add one employee:
Method: POST
URL: http://localhost:8080/restful_template/employee/
Body:
{
  "id": 5,
  "name": "user_5",
  "age": 32,
  "desc": "hello"
}
Header:
content-type: application/json

4. Update one employee:
Method: PUT
URL: http://localhost:8080/restful_template/employee/0
Body:
{
  "id": 0,
  "name": "test_user_0",
  "age": 23,
  "desc": "hello_0"
}
Header:
content-type: application/json

5. Delete one employee:
Method: DELETE
URL: http://localhost:8080/restful_template/employee/0

6. Delete all employees:
Method: DELETE
URL: http://localhost:8080/restful_template/employee/