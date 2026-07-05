# Laravel Sanctum REST API

A RESTful API built with **Laravel 12** and **Laravel Sanctum** that provides secure user authentication and Product CRUD operations.

## 🚀 Features

* User Registration
* User Login
* User Logout
* Token-Based Authentication using Laravel Sanctum
* Protected API Routes
* Product CRUD Operations
* Request Validation
* JSON Responses
* MySQL Database

---

## 🛠️ Tech Stack

* Laravel 12
* PHP 8.2+
* Laravel Sanctum
* MySQL
* Composer
* Postman (API Testing)

---

## 📂 Project Structure

```text
app/
├── Http/
│   └── Controllers/
│       └── Api/
│           ├── AuthController.php
│           └── ProductController.php
├── Models/
│   ├── User.php
│   └── Product.php

database/
└── migrations/

routes/
└── api.php
```

---

## 📥 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/tulsipatel5084/laravel-sanctum-rest-api.git
```

### 2. Navigate to the Project

```bash
cd laravel-sanctum-rest-api
```

### 3. Install Dependencies

```bash
composer install
```

### 4. Create Environment File

```bash
cp .env.example .env
```

### 5. Generate Application Key

```bash
php artisan key:generate
```

### 6. Configure Database

Update your `.env` file:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=rest_api
DB_USERNAME=root
DB_PASSWORD=
```

### 7. Run Migrations

```bash
php artisan migrate
```

### 8. Start Development Server

```bash
php artisan serve
```

Server URL:

```
http://127.0.0.1:8000
```

---

# 🔐 Authentication

The API uses **Laravel Sanctum** for authentication.

After successful login or registration, a token is returned.

Include the token in the request header:

```http
Authorization: Bearer YOUR_ACCESS_TOKEN
Accept: application/json
```

---

# 📌 API Endpoints

## Authentication

### Register

**POST**

```
/api/register
```

Request

```json
{
    "name":"Tulsi Patel",
    "email":"tulsipatel5084@gmail.com",
    "password":"password123"
}
```

---

### Login

**POST**

```
/api/login
```

Request

```json
{
    "email":"tulsipatel5084@gmail.com",
    "password":"password123"
}
```

---

### Logout

**POST**

```
/api/logout
```

Authentication Required

---

# 📦 Product API

## Get All Products

**GET**

```
/api/products
```

---

## Create Product

**POST**

```
/api/products
```

Request

```json
{
    "name":"Laptop",
    "description":"Dell Inspiron",
    "price":50000
}
```

---

## Get Single Product

**GET**

```
/api/products/{id}
```

---

## Update Product

**PUT**

```
/api/products/{id}
```

Request

```json
{
    "name":"MacBook Pro",
    "description":"Apple Laptop",
    "price":180000
}
```

---

## Delete Product

**DELETE**

```
/api/products/{id}
```

---

# 📬 API Response Example

```json
{
    "user": {
        "id": 1,
        "name": "Tulsi Patel",
        "email": "tulsipatel5084@gmail.com"
    },
    "token": "1|abcdefghijklmnopqrstuvwxyz"
}
```

---

# 🧪 Testing

You can test the API using:

* Postman
* Thunder Client (VS Code)
* Insomnia

---

# 📸 Screenshots

You can add screenshots of:

* Register API
* Login API
* Product CRUD
* Logout API

---

# 📄 License

This project is licensed under the MIT License.

---

# 👩‍💻 Author

**Tulsi Patel**

* GitHub: https://github.com/tulsipatel5084
* Email: [tulsipatel5084@gmail.com](mailto:tulsipatel5084@gmail.com)

---

⭐ If you found this project helpful, consider giving it a star on GitHub!
