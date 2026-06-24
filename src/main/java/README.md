
# 2GK API Capstone

## Overview

This project is a Spring Boot REST API developed as part of the Year Up Application Development program.

The API serves as the backend for an e-commerce website and allows users to:

* Browse product categories
* View products
* Search and filter products
* Register new accounts
* Log in using JWT authentication
* Manage categories (Admin only)

The application uses:

* Java
* Spring Boot
* Spring Security
* JWT Authentication
* MySQL
* JPA/Hibernate
* Insomnia for API testing

---

## Features Completed

### User Authentication

* User Registration
* User Login
* JWT Token Authentication
* Role-Based Authorization

### Categories

* Get All Categories
* Get Category By ID
* Get Products By Category
* Create Category (Admin Only)
* Update Category (Admin Only)
* Delete Category (Admin Only)

### Bug Fixes

* Fixed product search/filter functionality
* Fixed product update functionality so all fields save correctly

---

## Technologies Used

* Java 17
* Spring Boot
* Spring Security
* JWT
* MySQL
* Maven
* JPA/Hibernate
* Insomnia
* Git & GitHub

---

## API Endpoints

### Authentication

POST /register

POST /login

### Categories

GET /categories

GET /categories/{id}

GET /categories/{id}/products

POST /categories

PUT /categories/{id}

DELETE /categories/{id}

### Products

GET /products

GET /products/{id}

POST /products

PUT /products/{id}

DELETE /products/{id}

---

## Database

The application uses MySQL and includes:

* Users
* Profiles
* Categories
* Products
* Shopping Cart
* Orders
* Order Line Items

---

## Testing

All required Phase 1 and Phase 2 Insomnia tests were completed successfully.

### Test Results

* Setup Tests Passed
* Category Tests Passed
* Product Tests Passed
* Bug Fix Tests Passed

Result: 36/36 Tests Passing

---

## Interesting Code Example

One of the most important pieces of code implemented during this project was role-based authorization using Spring Security.

Example:

```java
@PreAuthorize("hasAuthority('ROLE_ADMIN')")
@PostMapping
public ResponseEntity<Category> addCategory(@RequestBody Category category)
{
    Category newCategory = categoryService.create(category);
    return ResponseEntity.status(201).body(newCategory);
}
```

This ensures that only users with the ADMIN role can create categories.

---

## Screenshots

Add screenshots here before submitting:

### Insomnia Test Runner

![Screenshot 2026-06-24 at 11.27.54 AM.png](Screenshot%202026-06-24%20at%2011.27.54%E2%80%AFAM.png)

### Application Running

![Screenshot 2026-06-23 at 3.16.45 PM.png](Screenshot%202026-06-23%20at%203.16.45%E2%80%AFPM.png)
---

## Author

J Richard K Tougeekay

Year Up United – Application Development

Spring Boot E-Commerce API Capstone
