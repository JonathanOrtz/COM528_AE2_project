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
  This java web project is a shopping cart system that allow users (registered, anonymous) chose items in the store and add them to the basket. Then a transaction will be done       with a bank api. Only users registered can checkout so the system must give a option to be registered. Aditionally there are adminitrators that will have the capability of add,   remove items and stock, add or disable users.
## PROJECT FEATURES
  ### Main page
  * visualise item lists
  * add/remove items from basket
  * Check total price
  * check checkout
  ### User page
  * check previous orders
  * disable account
  ### admin page
  * check users orders
  * disble orders
  * add users
  * option to go to a page where items/stock will be updated
  ### register page
  * add details
  * log in
  ### items
  * add new items
  * removve items
  * reduce stock
  * add stock
  * when a order is made the items added to that basket are reduced from the item stock

## USE CASES
  | Number | actor |description| system response|
| ------------- | ------------- |-----------|-------|
| Use case 1 | users |The user enter to the page |the system redirect to the main page(Home)|
| Use case 2 | users |The users are able to add items to the basket|the system will add those items to the basket and reduce those items from the stock|
| Use case 3 | user (admin/registered) |after added those items it will be able to check out|The system will let checkout checking is the users are registered.|
| Use case 4 | Anonymous user |with the objective of checkout the anonymous user should sing in|the system will redirect to the log in/sing in page to register|
| Use case 5 | Admin/registered users |Be able to modify your data|The system must let user registered their details and the admin can changed details of all users|
| Use case 6 | admin |Admin user has the capability of change items and items stock|system will add/remove items or create new items in the store|
| Use case 7 | The admin/user registered |Be able to desactivate account|The system will delete users that desactivate their account but it will keep their information for admin view|
| Use case 8 | admin |Admin be able to change the role of the users|the system will change the role of the user from admin to desactivated|


## USE CASE DIAGRAM
![image](https://user-images.githubusercontent.com/72144755/149768351-e90c6c08-ffbe-4439-b890-bb7ad502fc44.png)
## ROBUSTNESS DIAGRAM
![image](https://user-images.githubusercontent.com/72144755/149771978-c10df483-a9a7-4b35-9fc9-2f777bd27314.png)
## SEQUENCE DIAGRAM
![image](https://user-images.githubusercontent.com/72144755/149777362-7d06cf5f-baab-439e-b521-ff100371d4ce.png)
## TESTS PLAN
### anonymous/customer

|Test number|test|result expected|result obtained|
----------- | ---- |----------------| --------------|
|1|enter to the web|web is accessed with no issue|accessed no problem|
|2|add items|add items to the cart|items added|
|3|purchase|log in before checkout|error message displayed|

### registered user
|Test number|test|result expected|result obtained|
----------- | ---- |----------------| --------------|
|4|purchase|go to checkout|as loged in and regitered checkout is accessed|
|5|access to admin panel|no be able to access|no accessed|
|6|payment|pay after checkout| be able to pay|

### adminitrator
|Test number|test|result expected|result obtained|
----------- | ---- |----------------| --------------|
|7|access to panel|be able to access to admin features|accessed without problem|
|8|add users|add users to the system|users added|
|9|dele users|delete users from the system|users deleted|
|10|enter to the web|web is accessed with no issue|accessed no problem|
|11|role|change role of users|roled changed|
|12|catalogue |visualise catalogue|catalogue visualised|

## Issues faced
The project reflected some issues that depends of the level of the students in java or coding can be easy or difficult to face. Some issues found were:
 * the organisation of depencies and modules and the relationship of them,
 * Which libraries use in the project for this.
 * knowledge of spring 
 * connect wth the database 
Most of them were not fixed.
