# 🍽️ TasteBite – Restaurant Management Application

<p align="center">
  <b>A full-stack restaurant management application built with Python and Django</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" />
  <img src="https://img.shields.io/badge/Django-5.x-green?logo=django" />
  <img src="https://img.shields.io/badge/Bootstrap-5-purple?logo=bootstrap" />
  <img src="https://img.shields.io/badge/JavaScript-ES6-yellow?logo=javascript" />
  <img src="https://img.shields.io/badge/SQLite-Database-blue?logo=sqlite" />
</p>

---

## 📌 Overview

**TasteBite** is a full-stack restaurant management web application developed using **Python, Django, HTML, CSS, Bootstrap, and JavaScript**.

The application digitizes the restaurant ordering workflow by connecting **Customers, Waiters, and Chefs** through role-based dashboards.

Customers can browse the menu, select a table, manage their cart, and place food orders.

Waiters can manage incoming orders, confirm orders, serve prepared food, and generate bills.

Chefs can manage kitchen orders, update preparation status, and mark orders as ready.

The application demonstrates practical implementation of **authentication, role-based access control, Django ORM, database relationships, cart management, order processing, inventory management, dashboards, and billing**.

---

## 🎯 Project Objectives

The main objectives of TasteBite are:

- Digitize restaurant ordering operations
- Reduce manual order management
- Provide role-specific dashboards
- Manage food items and availability
- Track orders throughout the preparation process
- Simplify waiter and chef workflows
- Automate bill calculation
- Provide a responsive user experience

---

# ✨ Key Features

## 👤 Customer Module

Customers can:

- Register and login
- Browse restaurant food items
- View food availability
- Select a restaurant table
- Add food items to cart
- Increase or decrease food quantity
- Remove items from cart
- View cart total
- Place orders
- Provide customer details
- Track order status
- View order confirmation
- View generated bill

---

## 👨‍💼 Waiter Module

The waiter dashboard provides:

- Incoming order management
- Pending order management
- Order confirmation
- Ready-order monitoring
- Food serving workflow
- Bill generation
- Order status tracking
- Dashboard statistics

### Waiter Workflow

```text
Customer Order
      ↓
Pending
      ↓
Confirm Order
      ↓
Chef Preparation
      ↓
Ready
      ↓
Serve Food
      ↓
Generate Bill
      ↓
Completed

👨‍🍳 Chef Module
The chef dashboard provides:
- View confirmed orders
- Kitchen order queue
- Start food preparation
- Track preparing orders
- Mark orders as ready
- Monitor kitchen workload
- View order statistics

Chef Workflow
Confirmed
    ↓
Preparing
    ↓
Ready

🛒 Cart Management
The application provides a complete shopping-cart workflow.
Customers can:
- Add food items
- Increase quantity
- Decrease quantity
- Remove items
- View individual item totals
- View overall cart total
Stock availability is also considered when managing food quantities.

📦 Order Management
Orders move through different stages during restaurant operations.
Pending
   ↓
Confirmed
   ↓
Preparing
   ↓
Ready
   ↓
Completed
   ↓
Bill Generated

This workflow connects the customer, waiter, and chef modules.

🧾 Billing System
TasteBite includes a restaurant billing workflow.
The billing module calculates:
- Food item price
- Quantity
- Subtotal
- GST
- Grand total

📊 Dashboard
The application provides role-specific dashboards.
Dashboard statistics can include:
- Total Orders
- Pending Orders
- Confirmed Orders
- Preparing Orders
- Ready Orders
- Completed Orders
- Bill Generated Orders
Charts can be used to visualize order activity and restaurant workload.

🔐 Authentication & Role-Based Access
TasteBite provides role-based application access.
                     LOGIN
                       │
                       ▼
                 AUTHENTICATION
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
      CUSTOMER       WAITER        CHEF
          │            │            │
          ▼            ▼            ▼
      Customer       Waiter        Chef
      Dashboard     Dashboard     Dashboard

Each role receives functionality appropriate to its responsibilities.

🏗️ Application Architecture
                    ┌─────────────────┐
                    │     CUSTOMER    │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │  Django Web App │
                    │                 │
                    │ Authentication  │
                    │ Business Logic  │
                    │ Cart Management │
                    │ Order Management│
                    │ Billing         │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
              ▼              ▼              ▼
       ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
       │   CUSTOMER  │ │   WAITER    │ │    CHEF     │
       │  Dashboard  │ │  Dashboard  │ │  Dashboard  │
       └─────────────┘ └─────────────┘ └─────────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   Django ORM    │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │     SQLite      │
                    └─────────────────┘

🗄️ Database Design
The application uses Django ORM to interact with the database.
Major entities include:
User
 │
 └── UserProfile
       │
       └── Role

Food
 │
 └── Food Availability / Stock

RestaurantTable
 │
 └── Table Status

Cart
 │
 ├── Customer
 └── Food

Order
 │
 ├── Customer
 ├── Table
 └── OrderItem
       │
       └── Food

🛠️ Technology Stack
Frontend
- HTML5
- CSS3
- Bootstrap 5
- JavaScript
Backend
- Python
- Django
- Django ORM
Database
- SQLite
Visualization
- Chart.js
Development Tools
- Visual Studio Code
- Git
- GitHub
Deployment
- Render

📂 Project Structure
Tastebite-Restaurant-Application/
│
├── restapp/
│   ├── migrations/
│   ├── templates/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── ...
│
├── restaurant/
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   ├── asgi.py
│   └── ...
│
├── media/
│   └── food_images/
│
├── manage.py
├── requirements.txt
├── Procfile
├── runtime.txt
├── .gitignore
└── README.md

🚀 Installation & Setup
1. Clone the Repository
git clone https://github.com/Mathan495/Tastebite-Restaurant-Application.git

2. Navigate to the Project
cd Tastebite-Restaurant-Application

3. Create a Virtual Environment
Windows
python -m venv env

Linux / macOS
python3 -m venv env

4. Activate Virtual Environment
Windows
env\Scripts\activate

Linux / macOS
source env/bin/activate

5. Install Dependencies
pip install -r requirements.txt

6. Apply Migrations
python manage.py makemigrations
python manage.py migrate

7. Create Superuser
python manage.py createsuperuser

Follow the prompts to create the administrator account.
8. Run the Development Server
python manage.py runserver

Open the application:
http://127.0.0.1:8000/

🔑 Django Admin
The Django admin panel can be accessed at:
http://127.0.0.1:8000/admin/

Use the superuser credentials created during setup.
The admin interface can be used to manage application data such as:
- Food
- Restaurant Tables
- Users
- Orders
- Other application records

📱 Responsive Design
The application is designed to provide a responsive experience across:
- 💻 Desktop
- 💻 Laptop
- 📱 Mobile
- 📱 Tablet
Bootstrap's responsive grid system and custom CSS are used to maintain a consistent interface across screen sizes.

🔄 Complete Application Workflow
                    CUSTOMER
                       │
                       ▼
                 Login / Register
                       │
                       ▼
                  Select Table
                       │
                       ▼
                  Browse Menu
                       │
                       ▼
                   Add to Cart
                       │
                       ▼
                  Place Order
                       │
                       ▼
              ┌─────────────────┐
              │     WAITER      │
              │ Confirm Order   │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │      CHEF       │
              │ Prepare Order   │
              └────────┬────────┘
                       │
                       ▼
                  Mark Ready
                       │
                       ▼
              ┌─────────────────┐
              │     WAITER      │
              │  Serve Food     │
              └────────┬────────┘
                       │
                       ▼
                  Generate Bill
                       │
                       ▼
                    CUSTOMER

🚀 Deployment
The application can be deployed as a Django web service using Render.
Production deployment should include:
- Gunicorn
- Production Django settings
- Environment variables
- DEBUG=False
- Proper ALLOWED_HOSTS
- Static file configuration
- Production database
- Persistent media storage
The project uses:
Procfile

Example:
web: gunicorn restaurant.wsgi

For production use, PostgreSQL is recommended instead of SQLite, and uploaded media can be stored using a dedicated object-storage service such as Cloudinary.

🔮 Future Enhancements
Planned improvements include:
- 💳 Online payment integration
- 📱 QR-code digital menu
- 🔔 Real-time order notifications
- 📧 Email notifications
- 📱 SMS notifications
- 🤖 AI-powered food recommendations
- 💬 AI restaurant assistant
- 🪑 Online table reservation
- ☁️ Cloudinary media storage
- 🐘 PostgreSQL production database
- 🐳 Docker support
- 📈 Advanced analytics
- 🔐 Enhanced security and permissions
- 📊 Restaurant sales reports

🎓 Learning Outcomes
Through this project, I gained practical experience in:
- Full-stack web development
- Python programming
- Django framework
- Django ORM
- Authentication
- Role-based access control
- CRUD operations
- Database relationships
- Cart management
- Order processing
- Inventory management
- Billing implementation
- Dashboard development
- Responsive web design
- Git and GitHub
- Deployment concepts

👨‍💻 Developer
Mathan Kumar G
Computer Science Engineering Student
GitHub
https://github.com/Mathan495

⭐ Support
If you find this project useful, consider giving the repository a ⭐ on GitHub.

📄 License
This project is developed for educational and portfolio purposes.
