# Inventory Management System

A secure and scalable **Inventory Management System** built using **Java, Spring Boot, Spring Security, JWT, Spring Data JPA, and MySQL**. The project follows a layered architecture (Controller → Service → Repository) and provides RESTful APIs for managing products, categories, and inventory with role-based access control.

---

## Tech Stack

* Java 21
* Spring Boot 3
* Spring Security
* JWT Authentication
* Spring Data JPA (Hibernate)
* MySQL
* Maven
* Swagger / OpenAPI
* Lombok
* Jakarta Bean Validation

---

## Features

* JWT Authentication & Authorization
* Role-Based Access Control (Admin, Manager, Employee)
* Product Management (CRUD)
* Category Management (CRUD)
* Inventory Management
* Pagination & Sorting
* Product Search & Filtering
* Request Validation
* Global Exception Handling
* RESTful API Design
* Swagger API Documentation

---

## Project Structure

```text
inventory-management-system
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── om
│   │   │           └── inventory
│   │   │               ├── config
│   │   │               ├── controller
│   │   │               ├── dto
│   │   │               ├── entity
│   │   │               ├── exception
│   │   │               ├── repository
│   │   │               ├── security
│   │   │               ├── service
│   │   │               │   └── impl
│   │   │               ├── util
│   │   │               └── InventoryApplication.java
│   │   │
│   │   └── resources
│   │       ├── application.properties
│   │       └── static
│   │
│   └── test
│
├── pom.xml
├── README.md
└── .gitignore
```

---

## Database Schema

### User

* id
* name
* email
* password
* role

### Category

* id
* name
* description

### Product

* id
* name
* sku
* description
* price
* category

### Inventory

* id
* product
* quantity
* warehouse
* lastUpdated

---

## User Roles

### ADMIN

* Manage Users
* Create Products
* Update Products
* Delete Products
* Manage Categories
* Manage Inventory

### MANAGER

* View Products
* Update Inventory
* Add Stock
* Remove Stock

### EMPLOYEE

* View Products
* View Inventory

---

## REST API Endpoints

### Authentication

| Method | Endpoint             |
| ------ | -------------------- |
| POST   | `/api/auth/register` |
| POST   | `/api/auth/login`    |

### Products

| Method | Endpoint             |
| ------ | -------------------- |
| GET    | `/api/products`      |
| GET    | `/api/products/{id}` |
| POST   | `/api/products`      |
| PUT    | `/api/products/{id}` |
| DELETE | `/api/products/{id}` |

### Categories

| Method | Endpoint               |
| ------ | ---------------------- |
| GET    | `/api/categories`      |
| POST   | `/api/categories`      |
| PUT    | `/api/categories/{id}` |
| DELETE | `/api/categories/{id}` |

### Inventory

| Method | Endpoint                           |
| ------ | ---------------------------------- |
| GET    | `/api/inventory`                   |
| PUT    | `/api/inventory/{id}`              |
| PATCH  | `/api/inventory/add-stock/{id}`    |
| PATCH  | `/api/inventory/remove-stock/{id}` |

---

## Advanced Features

* Product Search
* Pagination
* Sorting
* Category Filtering
* Price Range Filtering
* Low Stock Alerts

---

## API Documentation

Swagger UI:

```text
http://localhost:8080/swagger-ui/index.html
```

---

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/your-username/inventory-management-system.git
```

### Navigate to the Project

```bash
cd inventory-management-system
```

### Configure the Database

Update the `application.properties` file with your MySQL credentials.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/inventory_db
spring.datasource.username=root
spring.datasource.password=your_password
```

### Create the Database

```sql
CREATE DATABASE inventory_db;
```

### Run the Application

```bash
mvn spring-boot:run
```

The application will start on:

```text
http://localhost:8080
```

---

## Testing

The APIs can be tested using:

* Postman
* Swagger UI
* cURL

---

## Future Enhancements

* Docker Support
* Redis Caching
* Audit Logging
* Email Notifications
* Inventory Transaction History
* Product Image Upload
* Unit Testing with JUnit and Mockito
* Integration Testing
* CI/CD using GitHub Actions

---

## Author

**Om Kumar Singh**

Java Backend Developer

Technologies: Java, Spring Boot, Spring Security, Hibernate, MySQL, REST APIs, JWT

---

## License

This project is intended for educational and portfolio purposes.
