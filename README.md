# WebApp-Servlets-JSP-DB

Java web applications using Servlets and JSP for user input handling and database integration. This repository contains three comprehensive projects demonstrating enterprise web development patterns.

## Project Overview

This repository showcases three essential web application development patterns:

### Part A: User Login Using Servlet and HTML Form

**Objective:**
Develop a Java Servlet that accepts user credentials through an HTML form and displays a personalized welcome message upon successful login.

**Key Features:**
- HTML form for capturing username and password
- Form submission using POST method
- Servlet request parameter handling with `request.getParameter()`
- Credential validation (hardcoded or database-backed)
- Personalized welcome message display using PrintWriter
- Error message display for invalid credentials
- Dynamic HTML content generation

**Technologies:** Java Servlet, HTML Forms, HTTP POST

**Learning Outcomes:**
- Form submission and HTTP POST handling
- Servlet request/response lifecycle
- Dynamic content generation in Java
- Basic authentication patterns

---

### Part B: Display Employee Records with JDBC and Servlet Integration

**Objective:**
Create a Java Servlet that integrates with a database using JDBC and displays a list of employees. Includes a search feature to fetch employee details by ID.

**Key Features:**
- Employee database table with fields: EmpID, Name, Salary
- JDBC database connectivity
- SQL queries to fetch all employee records
- Dynamic HTML table generation for employee listing
- HTML search form for Employee ID lookup
- Filtered result display based on search query
- Database connection pooling best practices

**Technologies:** Java Servlet, JDBC, SQL, HTML Tables

**Learning Outcomes:**
- Servlet and JDBC integration
- Dynamic HTML table generation
- SQL query execution from Java
- Handling both list and filtered views
- Database connection management

---

### Part C: Student Attendance Portal Using JSP and Servlet

**Objective:**
Develop a simple student attendance portal using JSP for the frontend and a Servlet for handling form submissions and saving attendance data to a database.

**Key Features:**
- JSP page for user interface
- HTML form for collecting attendance details (Student ID, Date, Status)
- Form submission to Servlet using POST method
- Servlet processing and data validation
- JDBC database integration for data persistence
- Attendance table management in database
- Confirmation response or success page redirect
- Separation of concerns (View: JSP, Controller: Servlet)

**Technologies:** Java Servlet, JSP, JDBC, HTML Forms, SQL

**Learning Outcomes:**
- MVC architecture implementation (JSP as View, Servlet as Controller)
- End-to-end data flow from UI to database
- Form submission and server-side processing
- Real-time web form submission and data storage
- JSP and Servlet interaction

---

## Project Structure

```
WebApp-Servlets-JSP-DB/
├── README.md
├── .gitignore
├── Part_A_UserLogin/
│   ├── src/
│   │   └── LoginServlet.java
│   └── WebContent/
│       └── login.html
├── Part_B_EmployeeRecords/
│   ├── src/
│   │   └── EmployeeServlet.java
│   └── WebContent/
│       └── employees.html
└── Part_C_StudentAttendance/
    ├── src/
    │   └── AttendanceServlet.java
    └── WebContent/
        └── attendance.jsp
```

## Prerequisites

- Java Development Kit (JDK) 8 or higher
- Apache Tomcat or equivalent Servlet container
- JDBC driver for your database (MySQL, PostgreSQL, etc.)
- IDE: NetBeans, Eclipse, or IntelliJ IDEA
- Database system (MySQL, PostgreSQL, SQLite, etc.)

## Database Setup

### Employee Table (Part B)
```sql
CREATE TABLE Employee (
    EmpID INT PRIMARY KEY,
    Name VARCHAR(100) NOT NULL,
    Salary DECIMAL(10, 2)
);
```

### Attendance Table (Part C)
```sql
CREATE TABLE Attendance (
    AttendanceID INT PRIMARY KEY AUTO_INCREMENT,
    StudentID INT NOT NULL,
    Date DATE NOT NULL,
    Status VARCHAR(20) NOT NULL
);
```

## Getting Started

1. Clone this repository
2. Import projects into your IDE
3. Configure database connection details
4. Deploy to Tomcat or your Servlet container
5. Access applications through your browser

## Configuration

Update database connection parameters in each Servlet:
- Database URL
- Username
- Password
- JDBC Driver class name

## Usage

### Part A - User Login
1. Navigate to login.html
2. Enter username and password
3. Submit form
4. View personalized welcome message or error

### Part B - Employee Records
1. View all employee records in table format
2. Use search form to find employee by ID
3. View filtered results

### Part C - Student Attendance
1. Navigate to attendance.jsp
2. Enter Student ID, Date, and Attendance Status
3. Submit form
4. View confirmation message

## Technologies Stack

- **Backend:** Java Servlets
- **Frontend:** HTML, JSP
- **Database:** JDBC
- **Server:** Apache Tomcat
- **Version Control:** Git

## Learning Resources

- Servlet API Documentation
- JDBC Tutorial
- JSP Best Practices
- HTTP Protocol Basics
- SQL Query Fundamentals

## Best Practices Demonstrated

✓ Separation of concerns (MVC pattern)
✓ Parameterized queries (SQL injection prevention)
✓ Proper exception handling
✓ Database connection management
✓ Input validation and sanitization
✓ HTTP POST for form submissions
✓ Dynamic content generation
✓ RESTful principles in URL patterns

## License

This project is provided as educational material without a specific license.

## Author

Created as a comprehensive guide for learning Java web development with Servlets and JSP.

## Contributing

Feel free to fork, modify, and enhance these examples for your learning purposes.
