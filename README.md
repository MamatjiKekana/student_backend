Student Management System - Backend API

A robust Spring Boot backend API for managing student records with complete CRUD operations and exception handling.

Features
Student CRUD Operations:

Create new student records

Retrieve all students or by ID/name

Update existing student information

Delete student records

Advanced Functionality:

Builder pattern implementation for Student entity

Custom exception handling (404 for not found)

Case-insensitive name search

Comprehensive logging (SLF4J)

RESTful API:

Proper HTTP status codes

Clean endpoint structure

Request/response validation

Technologies
Backend:

Java 17

Spring Boot 3.1

Spring Data JPA

Hibernate ORM

Database:

H2 (in-memory) or MySQL (configurable)

Tools:

Lombok (boilerplate reduction)

SLF4J (logging)

Maven (dependency management)

API Endpoints
Method	Endpoint	Description
GET	/students	Get all students
GET	/students/{id}	Get student by ID
GET	/students/name/{name}	Get student by name (case-insensitive)
POST	/students	Create new student
PUT	/students/{id}	Update student
DELETE	/students/{id}	Delete student
