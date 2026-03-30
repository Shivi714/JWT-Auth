# 🔐 Spring Boot JWT Authentication API

## 📌 Project Description

This project is a **Spring Boot REST API** that implements **JWT (JSON Web Token) based authentication**. It allows users to log in and receive a token, which can be used to access secured endpoints.

---

## 🚀 Features

* User login authentication
* JWT token generation
* Secure API endpoints
* RESTful API design

---

## 🛠 Technologies Used

* Java
* Spring Boot
* Spring Security
* Spring Data JPA
* MySQL
* Maven
* JWT (JJWT)

---

## 📂 Project Structure

```
com.JWTExample.JWT_Demo
│
├── config
│   └── SecurityConfig.java
│
├── controller
│   └── AuthController.java
│
├── model
│   └── User.java
│
├── repository
│   └── UserRepository.java
│
├── security
│   └── JwtUtil.java
│
└── service
    └── AuthService.java
```

---

## ⚙️ How It Works

1. User sends login request (`/api/login`)
2. Backend checks username & password from database
3. If valid → JWT token is generated
4. Token is used to access secured APIs

---

## 🔑 API Endpoints

### 🔹 Login

**POST** `/api/login`

**Params:**

```
username=your_username
password=your_password
```

**Response:**

```
JWT Token (if valid)
OR
Invalid Credentials
```

---

### 🔹 Test Endpoint

**GET** `/api/hello`

**Response:**

```
Hello! JWT Authentication Successful
```

---

## 🧩 Dependencies

Add in `pom.xml`:

```xml
<dependency>
    <groupId>io.jsonwebtoken</groupId>
    <artifactId>jjwt-impl</artifactId>
    <version>0.11.5</version>
    <scope>runtime</scope>
</dependency>

<dependency>
    <groupId>io.jsonwebtoken</groupId>
    <artifactId>jjwt-jackson</artifactId>
    <version>0.11.5</version>
    <scope>runtime</scope>
</dependency>
```

---

## 🔒 Security Config

* CSRF disabled
* CORS disabled
* Form login disabled
* JWT-based authentication

---

## 🗄️ Database

**Table:** `users`

| Column   | Type   |
| -------- | ------ |
| id       | Long   |
| username | String |
| password | String |

---

## 📸 Screenshots

### 🔹 Project Structure

<img width="210" height="209" alt="{58B31D49-2895-4557-9CF1-0C04AC4DC042}" src="https://github.com/user-attachments/assets/780ab5ff-3a56-4ded-ad6c-ccb61354f237" />


### 🔹 Login API (Postman)

<img width="899" height="278" alt="Screenshot 2026-03-11 093954" src="https://github.com/user-attachments/assets/7fced5a2-9481-4cc5-bb41-371f26621f5f" />


### 🔹 Invalid Login

<img width="902" height="375" alt="{5472FDF4-4FA1-4638-AE73-F6431351AE07}" src="https://github.com/user-attachments/assets/582f3c0b-29ed-47e2-b356-aed3f5e20161" />


### 🔹 Secured API (JWT Token)

<img width="960" height="295" alt="Screenshot 2026-03-11 094028" src="https://github.com/user-attachments/assets/7416ad1a-be3b-4f0c-9be1-e5f25ad65d5b" />


### 🔹 Database (MySQL)

![WhatsApp Image 2026-03-30 at 14 53 08](https://github.com/user-attachments/assets/ef45b400-ef62-4941-90d7-2c23db71a302)


---



## ▶️ Run Project

```bash
mvn spring-boot:run
```

---

## ⚠️ Note

* Password stored in plain text (for learning only)
* In production:

  * Use BCrypt password encoding
  * Add JWT filter & validation
  * Enable proper security

---

## 📖 Reference

Based on JWT Authentication implementation in Spring Boot
