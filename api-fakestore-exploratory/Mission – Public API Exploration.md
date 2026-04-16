# Mission – Public API Exploration

## 🎯 Objective

Perform 5 requests using public APIs and document each one.

---

## 📌 APIs Used

* Fake Store API → https://fakestoreapi.com
* Random User API → https://randomuser.me

---

## 🧪 Requests

### 🔹 Request 1 – Get all products (FakeStore)

* **URL:** https://fakestoreapi.com/products
* **Method:** GET
* **Status Code:** 200 OK
* **Response Highlight:** List of products including title, price, and category

---

### 🔹 Request 2 – Get product by ID

* **URL:** https://fakestoreapi.com/products/1
* **Method:** GET
* **Status Code:** 200 OK
* **Response Highlight:** `title` field with product name

---

### 🔹 Request 3 – Create a new product

* **URL:** https://fakestoreapi.com/products
* **Method:** POST
* **Status Code:** 200 OK

**Request Body:**

```json
{
  "title": "Test Product",
  "price": 29.99,
  "description": "Test description",
  "image": "https://i.pravatar.cc",
  "category": "electronics"
}
```

* **Response Highlight:** Returned product ID

---

### 🔹 Request 4 – Generate random user

* **URL:** https://randomuser.me/api/
* **Method:** GET
* **Status Code:** 200 OK
* **Response Highlight:** `email` field

---

### 🔹 Request 5 – Negative scenario (non-existent product)

* **URL:** https://fakestoreapi.com/products/9999
* **Method:** GET
* **Status Code:** 404 Not Found *(or empty response depending on API behavior)*
* **Response Highlight:** Product not found

---

## ✅ Requirements Covered

✔ 5 requests completed
✔ Multiple APIs used
✔ Different HTTP methods (GET, POST)
✔ Negative test scenario included

---

## 🚀 Key Learnings

* How to consume REST APIs
* Working with different endpoints
* Validating API responses
* Handling positive and negative scenarios
