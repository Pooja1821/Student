# 🎓 Student Management System (Console Based)

A simple **menu-driven Java console application** using **Maven**, **JPA**, and **Hibernate 7.0.5** with **PostgreSQL** as the backend database.

---

## 🚀 Features

- Add new students
- View all students
- Search student by ID
- Delete student
- Menu-driven command-line interface

---

## 🛠 Tech Stack

- Java 17+
- Maven (Build Tool)
- Hibernate ORM 7.0.5
- Jakarta Persistence API (JPA 3.1.0)
- PostgreSQL (Database)

---

## 📁 Project Structure

student-management/
├── pom.xml
└── src/
└── main/
├── java/
│ └── com/example/sms/
│ ├── App.java
│ ├── Student.java
│ └── StudentDAO.java
└── resources/
└── META-INF/
└── persistence.xml

<property name="jakarta.persistence.jdbc.url" value="jdbc:postgresql://localhost:5432/smsdb"/>
<property name="jakarta.persistence.jdbc.user" value="postgres"/>
<property name="jakarta.persistence.jdbc.password" value="admin"/>



===hibernate.cfg.xml===

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE hibernate-configuration PUBLIC
	"-//Hibernate/Hibernate Configuration DTD 3.0//EN"
	"http://www.hibernate.org/dtd/hibernate-configuration-3.0.dtd">
<hibernate-configuration>
	<session-factory>
	
            <property name="connection.driver-class">org.postgresql.Driver</property>
            <property name="connection.url">jdbc:postgresql://localhost:5432/Student</property>
            <property name="connection.username">postgres</property>
            <property name="connection.password">1234</property>
            
            <property name="hibernate.dialect">org.hibernate.dialect.PostgreSQLDialect</property>
            <property name="hbm2ddl.auto">update</property>
            
            <property name="hibernate.show_postgres">true</property>
            <mapping class="com.hibernate.hebernate.Student"/>
            
            
	</session-factory>
</hibernate-configuration>
	


==== pom.xm====

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.hibernate</groupId>
  <artifactId>hibernate</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>jar</packaging>

  <name>hibernate</name>
  <url>http://maven.apache.org</url>

  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
  </properties>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>3.8.1</version>
      <scope>test</scope>
    </dependency>
    <dependency>
    <groupId>org.hibernate.orm</groupId>
    <artifactId>hibernate-core</artifactId>
    <version>7.0.5.Final</version>
</dependency>
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <version>9.4-1205-jdbc42</version>
</dependency>

  </dependencies>
</project>


==sample output==

=== Student Management System ===
1. Add Student
2. View All Students
3. Search Student by ID
4. Delete Student
5. Exit
Enter choice: 1

Enter Student Name: Aarti
Enter Branch: Computer
Enter Marks: 92.4
✅ Student added successfully!


    

