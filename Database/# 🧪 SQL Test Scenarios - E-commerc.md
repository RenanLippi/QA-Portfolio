# 🧪 SQL Test Scenarios - E-commerce (SQLite)

This project contains SQL queries designed to validate common test scenarios in a fictional e-commerce database.

## 📌 Objective

Practice QA data validation using SQL, ensuring data consistency, integrity, and reliability across the system.

---

## 🗂️ Database Schema

### Table: `users`

* id (PK)
* name
* email
* status

### Table: `products`

* id (PK)
* name
* price
* stock
* category

### Table: `orders`

* id (PK)
* user_id (FK → users.id)
* product_id (FK → products.id)
* quantity
* status
* coupon
* created_at

---

## ✅ Scenario 1: Pending orders created today

**Objective:** Retrieve all orders with `pending` status created on the current date.

```sql
SELECT *
FROM orders
WHERE status = 'pending';
```

**Expected Result:**

* Only orders with `status = 'pending'`
* Created on today's date
* Empty result if none exist

---

## ✅ Scenario 2: Users without valid email

**Objective:** Identify users with missing or empty email fields.

```sql
SELECT *
FROM users
WHERE email IS NULL OR email = '';
```

**Expected Result:**

* List of users with null or empty email values

---

## ✅ Scenario 3: Products with zero stock

**Objective:** Detect products that are out of stock.

```sql
SELECT *
FROM products
WHERE stock = 0;
```

**Expected Result:**

* Products where stock equals zero

---

## ✅ Scenario 4: Orders with applied coupon

**Objective:** Validate orders that used a discount coupon.

```sql
SELECT *
FROM orders
WHERE coupon IS NOT NULL AND coupon != '';
```

**Expected Result:**

* Only orders where a coupon was applied

---

## ✅ Scenario 5: Total orders grouped by status

**Objective:** Analyze order distribution by status.

```sql
SELECT status, COUNT(*) AS total
FROM orders
GROUP BY status;
```

**Expected Result:**

* Count of orders grouped by status (e.g., pending, delivered, cancelled)

---

## 🚀 Possible Improvements

* Add JOIN queries for more complex validations
* Create negative test scenarios (invalid data cases)
* Integrate with API testing tools like Postman
* Automate validations using test frameworks

---

## 👨‍💻 Author

This project was created as part of QA and SQL practice to simulate real-world testing scenarios.
