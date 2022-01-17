# COM528_AE2_project
## Requirements to run the project
  * Apache Maven
  * Apache Tomcat 9
  * Java JDK version 8 or newer
  * IDE It can be Netbeans, Eclipse, Intelij
##  How to run the program:
  Before run the project you need to clean and built the project with the following command
  ```bash
  mvn clean install
  ```
  To run the web module of the project
  ```bash
  cd web
  ```
  It will be needed move to the web folder
  ```bash
  mvn spring-boot:run
  ```
  It must be used this command to run the web module in the http://localhost:8080/index.html port.
  ## Project purpose
  This java web project is a shopping cart system that allow user(registered, anonymous)
