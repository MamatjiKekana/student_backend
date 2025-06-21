# **STUDENT MANAGEMENT SYSTEM - BACKEND API**  

A robust Spring Boot backend API for managing student records with complete CRUD operations and exception handling.  



## **FEATURES**  

### **STUDENT CRUD OPERATIONS**  
- Create new student records  
- Retrieve all students or by ID/name  
- Update existing student information  
- Delete student records  

### **ADVANCED FUNCTIONALITY**  
- Builder pattern implementation for Student entity  
- Custom exception handling (404 for not found)  
- Case-insensitive name search  
- Comprehensive logging (SLF4J)  

### **RESTFUL API**  
- Proper HTTP status codes  
- Clean endpoint structure  
- Request/response validation  

---  

## **TECHNOLOGIES**  

### **BACKEND**  
- Java 17  
- Spring Boot 3.1  
- Spring Data JPA  
- Hibernate ORM  

### **DATABASE**  
- H2 (in-memory) or MySQL (configurable)  

### **TOOLS**  
- Lombok (boilerplate reduction)  
- SLF4J (logging)  
- Maven (dependency management)  



## **API Endpoints**  
Method	Endpoint	Description
GET	/students	Get all students
GET	/students/{id}	Get student by ID
GET	/students/name/{name}	Get student by name (case-insensitive)
POST	/students	Create new student
PUT	/students/{id}	Update student
DELETE	/students/{id}	Delete student



## **STUDENT ENTITY STRUCTURE**  
- **id** (auto-generated)  
- **name** (required)  
- **age**  
- **email**  



## **ERROR HANDLING**  
Returns **404 status** with message when student not found:  
```json  
{  
  "status": "NOT_FOUND",  
  "message": "Student not found"  
}  
```  

 

## **SETUP INSTRUCTIONS**  
1. Clone the repository  
2. Configure database in `application.properties`  
3. Build with Maven: `mvn clean install`  
4. Run: `mvn spring-boot:run`  

---  

## **EXAMPLE REQUESTS**  

**Create student:**  
```bash  
curl -X POST http://localhost:8080/students \  
-H "Content-Type: application/json" \  
-d '{"name":"John Doe","age":"21","email":"john@example.com"}'  
```  



## **PROJECT STRUCTURE**  
```  
student-backend/  
├── src/  
│   ├── main/  
│   │   ├── java/  
│   │   │   ├── com.example.Student_Backend_Project_controller/  
│   │   │   ├── com.example.Student_Backend_Project_Entity/  
│   │   │   ├── com.example.Student_Backend_Project_Repo/  
│   │   │   ├── com.example.Student_Backend_Project_Service/  
│   │   │   └── com.example.Student_Backend_Project_Service_imp/  
│   │   └── resources/  
│   └── test/  
├── pom.xml  
└── README.md  



