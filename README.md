# 🔐 JWT Authentication System (Spring Boot)

This is a simple **JWT-based Authentication System** built using **Spring Boot**.  
It provides secure login and signup functionality using **JSON Web Tokens (JWT)** for stateless authentication.

---

## 🛠️ Tech Stack Using

- Java 17+
- Spring Boot
- Spring Security
- Spring Data JPA
- MySQL / H2 (configurable)
- JWT (JSON Web Token)
- Maven

---

## 📁 Features

- ✅ User Registration (Signup)
- ✅ User Login (with token generation)
- ✅ Secure endpoints (accessible only with a valid JWT)
- ✅ Password hashing using BCrypt
- ✅ Role-based access (optional)
- ✅ Token validation in every request

---

## 📦 API Endpoints

| Method | Endpoint           | Description              | Access      |
|--------|--------------------|--------------------------|-------------|
| POST   | `/api/auth/signup` | Register a new user      | Public      |
| POST   | `/api/auth/login`  | Authenticate and get JWT | Public      |
| GET    | `/api/test/user`   | User content (test)      | Requires JWT|
| GET    | `/api/test/admin`  | Admin content (test)     | Requires JWT|

---

## ⚙️ How to Run Locally  

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/jwt-auth-springboot.git
   cd jwt-auth-springboot
````

2. **Configure Database**
   In `application.properties` or `application.yml`, set:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/jwt_auth_db
   spring.datasource.username=root
   spring.datasource.password=your_password
   ```

3. **Build the Project**

   ```bash
   mvn clean install
   ```

4. **Run the Application**

   ```bash
   mvn spring-boot:run
   ```

5. **Test the APIs using Postman** or Swagger (if enabled).

---

## 🔑 JWT Format

After login, you'll receive a JWT token:

```
Authorization: Bearer <your-token>
```

Include this token in the header for all secured API requests.

---

## 🧪 Example Test User

```json
{
  "username": "testuser",
  "email": "test@example.com",
  "password": "test123"
}
```

---

## 📂 Folder Structure

```
src/
├── controller/
├── service/
├── repository/
├── model/
├── config/
└── JwtAuthSystemApplication.java
```


