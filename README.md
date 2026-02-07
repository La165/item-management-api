# Item Management REST API

This is a simple Java Spring Boot backend application that provides a RESTful API for managing items (similar to an e‑commerce or catalog system).

The application uses **in‑memory storage** (ArrayList) and does not require any database.

---

## 🚀 Technologies Used

* Java 17
* Spring Boot
* Spring Web
* Spring Validation
* Spring Devtools
* Maven

---

## ▶️ How to Run the Application Locally

1. Clone the repository
2. Open the project in IntelliJ IDEA / Eclipse
3. Run the main class:

   ```
   ItemManagementApplication.java
   ```
4. The application will start on:

   ```
   http://localhost:8080
   ```

---

## 📦 Data Storage

* Data is stored **in memory** using `ArrayList`
* No database (H2 / MySQL / Oracle) is used
* Data will be lost when the application restarts

---

## 🔗 API Endpoints

### 1️⃣ Add a New Item

**Endpoint**

```
POST /api/items
```

**Request Body (JSON)**

```json
{
  "id": 1,
  "name": "iPhone",
  "description": "Apple smartphone",
  "price": 79999
}
```

**Response**

```json
{
  "id": 1,
  "name": "iPhone",
  "description": "Apple smartphone",
  "price": 79999
}
```

---

### 2️⃣ Get Item by ID

**Endpoint**

```
GET /api/items/{id}
```

**Example**

```
GET /api/items/1
```

**Response**

```json
{
  "id": 1,
  "name": "iPhone",
  "description": "Apple smartphone",
  "price": 79999
}
```

If the item does not exist, the API returns:

```
Item not found
```

---

## ✅ Input Validation

* Required fields are validated using Spring Validation
* Missing or invalid inputs return **400 Bad Request**

---

## ☁️ Deployment

* The application is deployed on **Render**
* Render is used because it provides native support for Java Spring Boot applications
* The service runs on a dynamically assigned port managed by the platform

---

## 📝 Notes

* This project is created as part of a backend assessment task
* The focus is on REST API design, validation, and in‑memory data handling
