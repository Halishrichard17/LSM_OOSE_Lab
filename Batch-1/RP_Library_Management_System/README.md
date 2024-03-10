# 📚 Library Management System -Java

## How to Run
1- Install these:
 * [Java SE Development Kit 8 (JDK 8)](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
 * After installing JDK 8, install [NetBeans IDE](https://netbeans.org/downloads/)

2- Open NetBeans IDE. Click on File -> Open Project and browse to the downloaded folder named "Project" and select it. It will load the NetBeans project.

3- Now everything is setup except the XAAMP MySql database for NetBeans. So, follow these steps to setup the database:

**Step 1:** First download the XAAMP server extension from [XAAMP](https://www.apachefriends.org/download.html) then open the live apache server and click 'start' on MySql
data server on port 3306.
   
**Step 2:** After that create a database named library_ms that will show up on phpmyadmin tab. To get phpmyadmin tab click on [phpmyadmin](http://127.0.0.1/phpmyadmin/).
   
**Step 3:** Provide the following database crendentials in the next popup and click Next.
  ```
  Host: localhost
  Port: 3306
  Database: library_ms
  User Name: 
  Password: 
  ````
**Step 4:** Now just click Next for the rest of the windows. After all this the database connection is made. Make sure that you connect with the database before running the project by right clicking on the connection and selecting connect. Now you are ready to run the project!

**Step 5:** Now to create the user table, issue_book table, student table etc, we have to write some sql querries in the database.
* ❏ create database library_ms;
* ❏ create table users(id int PRIMARY KEY AUTO_INCREMENT NOT null, name varchar(50), password varchar(50), email varchar(100), contact varchar(20));
* ❏ create table books_details(book_id int PRIMARY key not null, book_name varchar(100), author_name varchar(200), quantity int);
* ❏ create table student_details(student_id int PRIMARY KEY NOT null, student_name varchar(30), course_name varchar(50), branch varchar(50));
* ❏ create table issue_book_details(id int PRIMARY KEY NOT null AUTO_INCREMENT, book_id int, book_name varchar(150), student_id int, student_name varchar(50), issue_date date,      due_date date, status varchar(20));
* ❏ select book_name, count(*) as count from issue_book_details group by book_id;



![image](https://github.com/Halishrichard17/LSM_OOSE_Lab/assets/90974013/3eccf031-9f49-47ed-86bf-883a8bfea791)
