# Advanced E-Commerce Project

This is a comprehensive e-commerce platform built using Flask, SQLAlchemy, and PostgreSQL. The application supports essential e-commerce functionalities such as managing customers, orders, products, and customer accounts.

## Table of Contents
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
  - [Customer Endpoints](#customer-endpoints)
  - [Order Endpoints](#order-endpoints)
  - [Product Endpoints](#product-endpoints)
  - [Customer Account Endpoints](#customer-account-endpoints)
- [Testing](#testing)
- [Technologies Used](#technologies-used)
- [License](#license)

## Features
- **Customer Management**: Create, update, delete, and retrieve customer information.
- **Order Management**: Create and manage customer orders, including product association.
- **Product Management**: Add, update, delete, and retrieve products.
- **Customer Account Management**: Manage customer account details.
- **Role-based Access**: Assign roles to customers and handle role-based authentication.

## Project Structure
Advanced_E_Commerce/
│
├── app.py # Main application entry point
├── database.py # Database setup and initialization
├── models/ # ORM models for Customer, Order, Product, CustomerAccount
│ ├── customer.py
│ ├── order.py
│ ├── product.py
│ └── customeraccount.py
├── services/ # Service layer for business logic
│ ├── customerService.py
│ ├── orderService.py
│ └── productService.py
├── controllers/ # Controllers for handling API requests
│ ├── customerController.py
│ ├── orderController.py
│ ├── productController.py
│ └── customeraccountController.py
├── routes/ # Blueprint routes for the application
│ ├── customerBP.py
│ ├── orderBP.py
│ ├── productBP.py
│ └── customeraccntBP.py
└── utils/ # Utility functions
└── util.py

## Installation

1. **Clone the Repository**:
    git clone https://github.com/yourusername/Advanced_E_Commerce.git

2. **Create and Activate Virtual Environment**:
   
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. **Install Dependencies**:
  
    pip install -r requirements.txt

4. **Set Up the Database**:
    - Configure your PostgreSQL database in the `database.py` file.
    - Run migrations if applicable.

5. **Run the Application**:

    flask run

## Usage

The API can be tested using tools like [Postman](https://www.postman.com/) or [cURL](https://curl.se/). The application supports CRUD operations for customers, orders, products, and customer accounts.

## API Endpoints

### Customer Endpoints

- **POST /customers**: Create a new customer.
- **GET /customers**: Retrieve all customers.
- **PUT /customers/:id**: Update customer details by ID.
- **DELETE /customers/:id**: Delete a customer by ID.
- **POST /customers/login**: Authenticate a customer and get a token.

### Order Endpoints

- **POST /orders**: Create a new order.
- **GET /orders**: Retrieve all orders.
- **PUT /orders/:id**: Update an order by ID.
- **DELETE /orders/:id**: Delete an order by ID.

### Product Endpoints

- **POST /products**: Create a new product.
- **GET /products**: Retrieve all products.
- **PUT /products/:id**: Update a product by ID.
- **DELETE /products/:id**: Delete a product by ID.

### Customer Account Endpoints

- **POST /customer-accounts**: Create a new customer account.
- **GET /customer-accounts**: Retrieve all customer accounts.
- **PUT /customer-accounts/:id**: Update a customer account by ID.
- **DELETE /customer-accounts/:id**: Delete a customer account by ID.

## Testing

Unit tests are implemented using the `unittest` framework. The `Faker` library is used to generate test data.

Technologies Used

Flask: Web framework
SQLAlchemy: ORM for database management
PostgreSQL: Database
Faker: Library for generating test data
Python: Backend logic
Git: Version control
