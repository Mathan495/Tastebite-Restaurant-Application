# 🍽️ TasteBite – Restaurant Management Application

<p align="center">
  <b>A full-stack restaurant management system built with Python and Django</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Django-5.x-green?logo=django" alt="Django">
  <img src="https://img.shields.io/badge/Bootstrap-5-purple?logo=bootstrap" alt="Bootstrap">
  <img src="https://img.shields.io/badge/JavaScript-ES6-yellow?logo=javascript" alt="JavaScript">
  <img src="https://img.shields.io/badge/SQLite-Database-blue?logo=sqlite" alt="SQLite">
</p>

---

## 📌 About the Project

**TasteBite** is a full-stack restaurant management web application developed using **Python and Django** to digitize restaurant operations.

The application connects three major user roles:

- 👤 Customer
- 👨‍💼 Waiter
- 👨‍🍳 Chef

Customers can browse the restaurant menu, select a table, add food items to their cart, and place orders.

Waiters can manage incoming orders, confirm orders, serve prepared food, and generate bills.

Chefs can view confirmed orders, manage food preparation, and update orders as ready.

The project demonstrates practical implementation of **authentication, role-based access control, Django ORM, CRUD operations, cart management, order processing, stock management, dashboard workflows, and billing**.

---

## 🎯 Project Objectives

- Digitize restaurant ordering operations
- Reduce manual order management
- Provide role-based dashboards
- Manage food items and availability
- Track orders from placement to completion
- Improve communication between customers, waiters, and chefs
- Automate restaurant billing
- Provide a responsive web interface

---

# ✨ Features

## 👤 Customer

- User registration and login
- Role-based authentication
- Restaurant table selection
- Browse food menu
- View food availability
- Add food items to cart
- Increase/decrease item quantity
- Remove cart items
- View cart total
- Place food orders
- Enter customer details
- View order confirmation
- Track order status
- View generated bill

---

## 👨‍💼 Waiter Dashboard

The waiter dashboard provides:

- View incoming orders
- View pending orders
- Confirm customer orders
- Monitor ready orders
- Serve food
- Generate bills
- View order statistics
- Manage order status

### Waiter Workflow

```text
Customer Places Order
          ↓
       Pending
          ↓
    Waiter Confirms
          ↓
    Chef Prepares
          ↓
         Ready
          ↓
    Waiter Serves
          ↓
    Generate Bill
          ↓
       Completed

👨‍🍳 Chef Dashboard
The chef dashboard provides:
- View confirmed orders
- View kitchen order queue
- Start preparing orders
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
Customers can manage their selected food items before placing an order.
Features include:
- Add food items
- Increase quantity
- Decrease quantity
- Remove items
- Calculate item totals
- Calculate cart total
- Check food stock availability
📦 Order Management
Orders follow a structured restaurant workflow.
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
TasteBite includes an automated billing workflow.
The system calculates:
- Food item price
- Quantity
- Item total
- Subtotal
- GST
- Grand total
Example:
--------------------------------------
              TASTEBITE
             RESTAURANT
--------------------------------------

Food Item          Qty        Amount
--------------------------------------
Burger              2         ₹200
Pizza               1         ₹250
Fresh Juice         2         ₹120
--------------------------------------
Subtotal                       ₹570
GST 5%                          ₹28.50
--------------------------------------
Grand Total                    ₹598.50
--------------------------------------

📊 Dashboard & Analytics
The application provides role-specific dashboards.
Dashboard statistics include:
- Total Orders
- Pending Orders
- Confirmed Orders
- Preparing Orders
- Ready Orders
- Completed Orders
- Bill Generated Orders
Chart.js can be used to visualize order status and workload.
🔐 Authentication & Role-Based Access
TasteBite provides different application workflows based on the authenticated user's role.
                       LOGIN
                         │
                         ▼
                  AUTHENTICATION
                         │
             ┌───────────┼───────────┐
             │           │           │
             ▼           ▼           ▼
         CUSTOMER      WAITER       CHEF
             │           │           │
             ▼           ▼           ▼
         Customer      Waiter       Chef
         Dashboard    Dashboard    Dashboard

Each role has access to functionality relevant to its responsibilities.
🏗️ Application Architecture
                    ┌─────────────────┐
                    │     Customer    │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   Django Web    │
                    │   Application   │
                    │                 │
                    │ Authentication │
                    │ Business Logic │
                    │ Cart Management │
                    │ Order System    │
                    │ Billing System  │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
              ▼              ▼              ▼
       ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
       │  Customer   │ │   Waiter    │ │    Chef     │
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
The application uses Django ORM for database operations.
Major entities include:
User
 │
 └── UserProfile
       │
       └── Role

Food
 │
 ├── Category
 ├── Meal Time
 ├── Price
 ├── Stock
 └── Availability

RestaurantTable
 │
 ├── Table Number
 ├── Seats
 └── Status

Cart
 │
 ├── Customer
 └── Food

Order
 │
 ├── Customer
 ├── Table
 ├── Status
 └── OrderItem
       │
       └── Food

🛠️ Technology Stack
Category	Technologies
Frontend	HTML5, CSS3, Bootstrap 5, JavaScript
Backend	Python, Django
ORM	Django ORM
Database	SQLite
Charts	Chart.js
Version Control	Git, GitHub
IDE	Visual Studio Code
Deployment	Render


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

3. Create Virtual Environment
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

7. Create Admin User
python manage.py createsuperuser

8. Run the Application
python manage.py runserver

Open:
http://127.0.0.1:8000/

🔑 Django Admin
The Django administration panel is available at:
http://127.0.0.1:8000/admin/

The admin interface can be used to manage application data such as:
- Food items
- Restaurant tables
- Users
- Orders
- User profiles
📱 Responsive Design
The application is designed for different screen sizes:
- 💻 Desktop
- 💻 Laptop
- 📱 Mobile
- 📱 Tablet
Bootstrap's responsive utilities and custom CSS are used to provide a consistent user experience across devices.
🔄 Complete Restaurant Workflow
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
                    ┌───────────────┐
                    │    WAITER     │
                    │ Confirm Order │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │     CHEF      │
                    │ Prepare Food  │
                    └───────┬───────┘
                            │
                            ▼
                       Mark Ready
                            │
                            ▼
                    ┌───────────────┐
                    │    WAITER     │
                    │   Serve Food  │
                    └───────┬───────┘
                            │
                            ▼
                       Generate Bill
                            │
                            ▼
                         CUSTOMER

🚀 Deployment
The application is structured for Django deployment using a WSGI server such as Gunicorn.
The project includes a Procfile:
web: gunicorn restaurant.wsgi

For production deployment, the following should be configured:
- Production SECRET_KEY
- DEBUG=False
- ALLOWED_HOSTS
- Static file configuration
- Production database
- Environment variables
- Gunicorn
- Persistent media storage
For a production environment, PostgreSQL is recommended instead of SQLite, while uploaded media can be stored using a dedicated object-storage service.
🔮 Future Enhancements
The following features can be added in future versions:
- 💳 Online payment integration
- 📱 QR-code based menu
- 🔔 Real-time order notifications
- 📧 Email notifications
- 📱 SMS notifications
- 🤖 AI-based food recommendations
- 💬 AI restaurant assistant
- 🪑 Online table reservation
- ☁️ Cloudinary media storage
- 🐘 PostgreSQL production database
- 🐳 Docker support
- 📈 Advanced sales analytics
- 📊 Restaurant revenue reports
- 🔐 Advanced permission management
🎓 Skills Demonstrated
This project demonstrates practical experience in:
- Python
- Django
- Django ORM
- HTML
- CSS
- Bootstrap
- JavaScript
- SQLite
- Authentication
- Role-Based Access Control
- CRUD Operations
- Database Relationships
- Cart Management
- Order Management
- Inventory Management
- Billing
- Dashboard Development
- Responsive Web Design
- Git & GitHub
- Deployment
📸 Screenshots
Add screenshots of the major application modules here.
🏠 Customer Home
 
🍴 Food Menu
 
🛒 Shopping Cart
 
👨‍💼 Waiter Dashboard
 
👨‍🍳 Chef Dashboard
 
🧾 Billing
 
Create a screenshots/ folder in the repository and add your actual screenshots before using these image paths.

👨‍💻 Developer
Mathan Kumar G
Computer Science Engineering Student
GitHub
https://github.com/Mathan495
⭐ Project
If you find this project useful, consider giving the repository a ⭐.
📄 License
This project is developed for educational and portfolio purposes.

### GitHub About section

For the repository's **About** section, use:

**Description:**

> Full-stack restaurant management system built with Python and Django featuring customer ordering, waiter and chef dashboards, cart management, order tracking, inventory, and automated billing.

**Topics:**

```text
python
django
django-orm
restaurant-management
restaurant-application
full-stack-development
bootstrap
javascript
sqlite
role-based-access
food-ordering
order-management
billing-system
web-application

One important cleanup before you make the repository public-facing: your current repository has db.sqlite3 committed. GitHub I recommend adding db.sqlite3, env/, .env, __pycache__/, and staticfiles/ to .gitignore and removing the database file from Git tracking. This will make the repository look considerably more professional for placement reviews.






    








🍽️ TasteBite Restaurant Management System

A role-based Restaurant Management System developed using Python, Django, HTML, CSS, JavaScript, Bootstrap, and SQLite. The system streamlines restaurant operations by providing dedicated dashboards for Customers, Waiters, and Chefs, ensuring an efficient order management workflow from table booking to bill generation.
\

📌 Project Overview

TasteBite Restaurant Management System is a full-stack Django web application designed to automate restaurant operations. Customers can reserve tables, browse the menu, place food orders, and track their order status. Waiters manage customer orders, while chefs handle kitchen preparation through dedicated dashboards.
\

The application follows a complete restaurant workflow and provides an intuitive user experience with responsive design and interactive analytics.
\

🚀 Features

👤 Customer Module

User Registration & Login

Role-Based Authentication

Restaurant Table Booking

Browse Food Menu

Add Food to Cart

Update Cart Quantity

Remove Cart Items

Place Order

Order Success Page

View Bill

👨‍🍳 Chef Dashboard

View Confirmed Orders

Start Preparing Orders

Mark Orders as Ready

Kitchen Order Queue

Order Status Management

👨‍💼 Waiter Dashboard

View Customer Orders

Confirm Orders

Serve Ready Orders

Generate Customer Bill

Order Status Analysis (Bar Chart)

Dashboard Statistics

📄 Billing System

Generate Customer Bill

Automatic GST Calculation

Grand Total Calculation

Print Bill

Professional Invoice Layout

📊 Dashboard Analytics

Total Orders

Pending Orders

Confirmed Orders

Preparing Orders

Ready Orders

Completed Orders

Interactive Order Status Bar Chart

📱 Responsive Design

Desktop Friendly

Tablet Responsive

Mobile Responsive

🔄 Restaurant Workflow

Customer

    │

    ▼

Select Table

    │

    ▼

Browse Menu

    │

    ▼

Add Food to Cart

    │

    ▼

Place Order

    │

    ▼

Waiter Dashboard

(Confirm Order)

    │

    ▼

Chef Dashboard

(Start Preparing)

    │

    ▼

Mark Ready

    │

    ▼

Waiter Dashboard

(Serve Food)

    │

    ▼

Generate Bill

    │

    ▼

Customer Bill

🛠️ Tech Stack

Frontend

HTML5

CSS3

Bootstrap 5

JavaScript

Chart.js

Backend

Python

Django

Database

SQLite

Deployment

Render

Version Control

Git

GitHub

📂 Project Structure

Tastebite-Restaurant-Website

│

├── restapp/

├── restaurant/

├── media/

├── templates/

├── manage.py

├── requirements.txt

├── Procfile

├── runtime.txt

└── README.md

⚙️ Installation

Clone Repository

git clone https://github.com/Mathan495/Tastebite-Restaurant-Website.git

Go to Project

cd Tastebite-Restaurant-Website

Create Virtual Environment

python -m venv env

Activate Environment

Windows
\

env\Scripts\activate

Linux / Mac
\

source env/bin/activate

Install Dependencies

pip install -r requirements.txt

Run Migrations

python manage.py makemigrations

python manage.py migrate

Create Superuser

python manage.py createsuperuser

Start Server

python manage.py runserver

🔑 User Roles

Customer

Book Table

Browse Menu

Add to Cart

Place Order

View Bill

Waiter

Confirm Orders

Serve Food

Generate Bill

Monitor Orders

Chef

View Confirmed Orders

Prepare Food

Mark Orders Ready

📈 Order Status Flow

Pending

   │

   ▼

Confirmed

   │

   ▼

Preparing

   │

   ▼

Ready

   │

   ▼

Completed

   │

   ▼

Bill Generated

🔮 Future Enhancements

Online Payment Integration

QR Code Menu

Customer Order Tracking

Email Notifications

SMS Notifications

AI Food Recommendation

AI Customer Chatbot

Online Table Reservation

Cloudinary Image Storage

PostgreSQL Database

Docker Deployment

🎯 Learning Outcomes

Django Authentication

Role-Based Access Control

CRUD Operations

Database Relationships

Order Management Workflow

Dashboard Analytics

Responsive Web Design

Bill Generation System

Deployment on Render

📧 Contact

Mathan Kumar G
\

💻 GitHub: https://github.com/Mathan495
\

⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.
\

📄 License

This project is developed for educational purposes and portfolio demonstration.
give this format this project to  anlyze this projects flow and give correct readme professionally





Show more

 






I analyzed the live deployed TasteBite application at tastebite-app.onrender.com, including the login/register flow, About page, menu structure, food availability, table selection, cart entry points, and the customer-facing workflow. The live application currently presents Morning, Afternoon, and Night menus, food pricing/stock availability, quantity controls, and table selection. TasteBite
Based on that flow, this is a more accurate and professional README for your project. I have also included the Live Demo, which is important for recruiters.
README.md
# 🍽️ TasteBite – Restaurant Management System

<p align="center">
  <b>Full-Stack Restaurant Management System built with Python and Django</b>
</p>

<p align="center">
  <a href="https://tastebite-app.onrender.com/">
    <img src="https://img.shields.io/badge/Live%20Demo-TasteBite-success?style=for-the-badge" alt="Live Demo">
  </a>
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Django-5.x-green?style=for-the-badge&logo=django" alt="Django">
  <img src="https://img.shields.io/badge/Bootstrap-5-purple?style=for-the-badge&logo=bootstrap" alt="Bootstrap">
  <img src="https://img.shields.io/badge/JavaScript-ES6-yellow?style=for-the-badge&logo=javascript" alt="JavaScript">
  <img src="https://img.shields.io/badge/SQLite-Database-blue?style=for-the-badge&logo=sqlite" alt="SQLite">
</p>

---

## 🌐 Live Demo

🔗 **Live Application:**  
https://tastebite-app.onrender.com/

> The application is deployed using Render.

---

# 📌 Project Overview

**TasteBite Restaurant Management System** is a full-stack web application developed using **Python, Django, HTML, CSS, JavaScript, Bootstrap, and SQLite**.

The system digitizes restaurant operations by connecting **Customers, Waiters, and Chefs** through role-based workflows.

Customers can create an account, select a restaurant table, browse food items, manage their cart, and place orders.

Waiters manage incoming orders, confirm orders, serve prepared food, and generate customer bills.

Chefs manage kitchen orders by viewing confirmed orders, starting food preparation, and marking orders as ready.

The application provides a structured restaurant workflow from **table selection and food ordering to kitchen preparation, serving, and billing**.

---

# 🎯 Project Objectives

The main objectives of TasteBite are:

- Digitize restaurant ordering operations
- Simplify table selection and food ordering
- Provide role-based access for restaurant staff
- Manage food availability and stock
- Track orders throughout the preparation process
- Connect waiter and chef workflows
- Automate restaurant billing
- Provide responsive and user-friendly interfaces
- Reduce manual restaurant order management

---

# 🚀 Features

## 👤 Customer Module

Customers can:

- User Registration
- User Login
- Role-Based Authentication
- Select Restaurant Table
- Browse Food Menu
- Search Food Items
- View Food Prices
- View Food Availability
- Manage Food Quantity
- Add Food to Cart
- Increase Cart Quantity
- Decrease Cart Quantity
- Remove Cart Items
- Place Orders
- Provide Customer Details
- View Order Confirmation
- View Order Status
- View Generated Bill

---

## 🍴 Food Menu

The menu is organized according to meal time:

### 🌅 Morning Menu

Breakfast items such as:

- Idli
- Dosa
- Pongal
- Poori Masala
- Upma
- Vada

### ☀️ Afternoon Menu

Lunch items such as:

- Chicken Biryani
- Veg Meals
- Fried Rice
- Chicken Fried Rice
- Fish Curry Meals
- Paneer Butter Masala

### 🌙 Night Menu

Dinner items such as:

- Butter Naan
- Chicken Curry
- Tandoori Chicken
- Margherita Pizza
- Chicken Burger
- Alfredo Pasta
- Chocolate Brownie
- Vanilla Ice Cream
- Gulab Jamun

The menu displays **food price, meal time, stock availability, quantity controls, and table selection**. 

---

# 🪑 Table Selection

Customers can select a restaurant table before placing their order.

```text
Customer
    │
    ▼
Select Table
    │
    ▼
Browse Menu
    │
    ▼
Select Food
    │
    ▼
Add to Cart

This connects the customer's selected table with the ordering workflow.
🛒 Cart Management
The cart module allows customers to manage their selected food items before placing an order.
Features include:
- Add food items
- Increase quantity
- Decrease quantity
- Remove food items
- Calculate item totals
- Calculate cart total
- Check food availability
- Review selected items before ordering
👨‍🍳 Chef Dashboard
The Chef Dashboard manages kitchen operations.
Features
- View confirmed customer orders
- View kitchen order queue
- Start preparing orders
- Track preparing orders
- Mark orders as ready
- Manage order preparation status
- Monitor kitchen workload
Chef Workflow
Confirmed Order
      │
      ▼
Start Preparing
      │
      ▼
Preparing
      │
      ▼
Mark as Ready
      │
      ▼
Ready for Serving

👨‍💼 Waiter Dashboard
The Waiter Dashboard manages customer orders and serving operations.
Features
- View incoming orders
- View pending orders
- Confirm customer orders
- Monitor order status
- View ready orders
- Serve food
- Generate customer bills
- Monitor restaurant order statistics
Waiter Workflow
Pending Order
      │
      ▼
Confirm Order
      │
      ▼
Chef Preparation
      │
      ▼
Ready
      │
      ▼
Serve Food
      │
      ▼
Generate Bill

📄 Billing System
TasteBite includes a dedicated billing workflow.
The billing system provides:
- Customer bill generation
- Food item calculation
- Quantity calculation
- Subtotal calculation
- GST calculation
- Grand total calculation
- Professional invoice layout
- Print-friendly bill
Billing Flow
Order
  │
  ▼
Order Items
  │
  ▼
Subtotal
  │
  ▼
GST
  │
  ▼
Grand Total
  │
  ▼
Customer Bill

📊 Dashboard Analytics
The application provides dashboard statistics for restaurant staff.
Important metrics include:
- Total Orders
- Pending Orders
- Confirmed Orders
- Preparing Orders
- Ready Orders
- Completed Orders
- Bill Generated Orders
Interactive order-status visualization can be implemented using Chart.js.
🔄 Complete Restaurant Workflow
                         CUSTOMER
                            │
                            ▼
                    Register / Login
                            │
                            ▼
                      Select Table
                            │
                            ▼
                      Browse Menu
                            │
                            ▼
                     Select Food
                            │
                            ▼
                       Add Cart
                            │
                            ▼
                      Place Order
                            │
                            ▼
                   ┌────────────────┐
                   │     WAITER     │
                   │ Confirm Order  │
                   └───────┬────────┘
                           │
                           ▼
                   ┌────────────────┐
                   │      CHEF      │
                   │ Prepare Order  │
                   └───────┬────────┘
                           │
                           ▼
                      Mark Ready
                           │
                           ▼
                   ┌────────────────┐
                   │     WAITER     │
                   │   Serve Food   │
                   └───────┬────────┘
                           │
                           ▼
                     Generate Bill
                           │
                           ▼
                       CUSTOMER
                           │
                           ▼
                          BILL

📈 Order Status Flow
Pending
   │
   ▼
Confirmed
   │
   ▼
Preparing
   │
   ▼
Ready
   │
   ▼
Completed
   │
   ▼
Bill Generated

🔐 Authentication & Role-Based Access
TasteBite provides role-based access for different types of users.
                       LOGIN
                         │
                         ▼
                  AUTHENTICATION
                         │
             ┌───────────┼───────────┐
             │           │           │
             ▼           ▼           ▼
         CUSTOMER      WAITER       CHEF
             │           │           │
             ▼           ▼           ▼
         Customer      Waiter       Chef
         Dashboard    Dashboard    Dashboard

Customer
Register
   ↓
Login
   ↓
Select Table
   ↓
Browse Menu
   ↓
Order Food
   ↓
View Bill

Waiter
Login
   ↓
View Orders
   ↓
Confirm Orders
   ↓
Serve Food
   ↓
Generate Bill

Chef
Login
   ↓
View Confirmed Orders
   ↓
Prepare Food
   ↓
Mark Order Ready

🏗️ Application Architecture
                 ┌─────────────────────┐
                 │      Customer       │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │    Django Web App   │
                 │                     │
                 │ Authentication      │
                 │ Business Logic      │
                 │ Cart Management     │
                 │ Order Management    │
                 │ Billing             │
                 └──────────┬──────────┘
                            │
              ┌─────────────┼─────────────┐
              │             │             │
              ▼             ▼             ▼
       ┌────────────┐ ┌────────────┐ ┌────────────┐
       │  Customer  │ │   Waiter   │ │    Chef    │
       │  Module    │ │  Dashboard │ │  Dashboard │
       └────────────┘ └────────────┘ └────────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │     Django ORM      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │       SQLite        │
                 └─────────────────────┘

🗄️ Database Design
The application uses Django ORM for database operations and relational data management.
Major entities include:
User
 │
 └── UserProfile
       │
       └── Role

Food
 │
 ├── Name
 ├── Category
 ├── Meal Time
 ├── Price
 ├── Stock
 └── Availability

RestaurantTable
 │
 ├── Table Number
 ├── Seats
 └── Status

Cart
 │
 ├── Customer
 └── Food

Order
 │
 ├── Customer
 ├── Table
 ├── Status
 └── OrderItem
       │
       └── Food

🛠️ Tech Stack
Frontend
- HTML5
- CSS3
- Bootstrap 5
- JavaScript
- Chart.js
Backend
- Python
- Django
- Django ORM
Database
- SQLite
Deployment
- Render
Version Control
- Git
- GitHub
Development Environment
- Visual Studio Code
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

⚙️ Installation & Setup
1. Clone Repository
git clone https://github.com/Mathan495/Tastebite-Restaurant-Application.git

2. Navigate to Project
cd Tastebite-Restaurant-Application

3. Create Virtual Environment
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

8. Run Development Server
python manage.py runserver

Open the application:
http://127.0.0.1:8000/

🔑 Django Admin
The Django administration panel is available at:
http://127.0.0.1:8000/admin/

The admin panel can be used to manage:
- Food items
- Restaurant tables
- Users
- Orders
- User profiles
- Application data
📱 Responsive Design
TasteBite is designed to provide a responsive user experience across:
- 💻 Desktop
- 💻 Laptop
- 📱 Mobile
- 📱 Tablet
The interface uses Bootstrap responsive utilities and custom CSS for different screen sizes.
🚀 Deployment
TasteBite is deployed as a Django web application on Render.
Production Components
GitHub
   │
   ▼
Render
   │
   ▼
Django Application
   │
   ├── Gunicorn
   │
   ├── Static Files
   │
   └── Database

Production Configuration
The deployment uses:
- Django
- Gunicorn
- Render
- Environment-based configuration
- Static file handling
- Production WSGI configuration
Example Procfile:
web: gunicorn restaurant.wsgi

🔮 Future Enhancements
Planned improvements include:
- 💳 Online Payment Integration
- 📱 QR Code Digital Menu
- 🔔 Real-Time Order Notifications
- 📧 Email Notifications
- 📱 SMS Notifications
- 🤖 AI-Based Food Recommendations
- 💬 AI Restaurant Chatbot
- 🪑 Advanced Online Table Reservation
- ☁️ Cloudinary Image Storage
- 🐘 PostgreSQL Database
- 🐳 Docker Deployment
- 📈 Advanced Sales Analytics
- 📊 Restaurant Revenue Reports
- 🔐 Advanced Permission Management
🎓 Learning Outcomes
This project provided practical experience in:
- Python Web Development
- Django Framework
- Django ORM
- Authentication
- Role-Based Access Control
- CRUD Operations
- Database Relationships
- Cart Management
- Order Management
- Inventory / Stock Management
- Restaurant Workflow Design
- Billing System Development
- Dashboard Development
- Chart.js Integration
- Responsive Web Design
- Git & GitHub
- Django Deployment
- Render Deployment
📸 Screenshots
Add screenshots of the actual application here.
🏠 Login
 
📝 Registration
 
🍴 Menu
 
🛒 Cart
 
👨‍💼 Waiter Dashboard
 
👨‍🍳 Chef Dashboard
 
🧾 Bill
 
Create a screenshots folder in the repository and add the actual screenshots before committing the README.

👨‍💻 Developer
Mathan Kumar G
Computer Science Engineering Student
GitHub
https://github.com/Mathan495
Live Project
https://tastebite-app.onrender.com/
⭐ Support
If you find this project useful or interesting, consider giving the repository a ⭐ on GitHub.
📄 License
This project is developed for educational purposes and portfolio demonstration.

### Recommended GitHub repository description

For the **About → Description** field, use:

> **Full-stack Django restaurant management system with role-based customer, waiter, and chef workflows, table selection, food ordering, cart management, kitchen operations, order tracking, and automated billing.**

And add these GitHub topics:

```text
python
django
restaurant-management
django-orm
full-stack-development
bootstrap
javascript
sqlite
food-ordering
order-management
billing-system
role-based-access
web-application
render
role-based-access
web-application
render
