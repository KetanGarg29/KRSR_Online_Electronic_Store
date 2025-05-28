# KRSR Electronic Store 🛒

Welcome to the GitHub repository for **KRSR Online Electronic Store**, a full-stack e-commerce platform developed as part of a group project for our Database Management Systems (DBMS) course.

## 🧰 Tech Stack

### 📦 Backend
- **MySQL** – Relational database management system to store and manage all application data.
- **Flask** – Lightweight Python web framework used for backend logic and routing.

### 🖥️ Frontend
- **HTML5 / CSS3** – For building responsive and interactive user interfaces.

---

## 🛠️ Key Features

- 🧾 **User Registration & Login System**
- 🛍️ **Product Browsing with Categories**
- 🧺 **Add to Cart & Place Order**
- 📦 **Admin Panel to Add/Remove Products**
- 📊 **Order History & Inventory Management**
- 📬 **Email Confirmation for Orders (Optional if implemented)**

---

## 🧠 Database Design & Concepts Used

### ✅ Tables Implemented
- `users` – Stores user credentials and roles.
- `products` – Product catalog with name, price, description, and category.
- `cart` – Temporary storage for user's selected items.
- `orders` – Stores order history with product and user references.
- `order_items` – Details of items in each order.
- `admin` – Admin details for inventory access.

### ✅ Advanced DBMS Concepts Used

#### 🔁 Triggers
- `after_insert_order` – Automatically updates stock when a new order is placed.
- `before_delete_product` – Prevents deletion if product exists in active carts.

#### 🔐 Views
- `customer_orders_view` – Shows all past orders for a given customer.
- `inventory_status_view` – Used by admin to view current inventory with stock levels.

#### ⚙️ Procedures
- `add_product()` – Stored procedure to add a product using admin privileges.
- `get_user_cart()` – Fetches all cart items for a particular user.

#### 🔄 Transactions
- Order placement and stock deduction are handled in atomic transactions to prevent data corruption in concurrent accesses.

---

## 🔁 Flask Backend Overview

- `app.py` – Main Flask file containing route definitions.
- `db.py` – Handles MySQL connections using `mysql-connector` or `PyMySQL`.
- `routes/` – Contains modularized routes for user, cart, and admin functionalities.
- `templates/` – Jinja2 templates for rendering HTML pages with dynamic content.

---

## 🖼️ Screenshots (Add later)
- Homepage
- Product listing
- Cart page
- Admin dashboard

---

## 🚀 Getting Started

### 🔧 Requirements
- Python 3.8+
- MySQL
- Flask (`pip install flask`)
- MySQL connector (`pip install mysql-connector-python`)

### ⚙️ Setup Instructions
```bash
git clone https://github.com/your-username/KRSR-Electronic-Store.git
cd KRSR-Electronic-Store
 -Import the SQL file database_schema.sql into your MySQL server.

 - Update db.py with your MySQL credentials.

Run the app:
```bash
python server.py
Visit http://127.0.0.1:5000/ in your browser.
