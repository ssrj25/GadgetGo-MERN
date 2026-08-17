# GadgetGo-MERN-Stack
Link to Project : https://webecommerce.onrender.com/

# 🛒 GadgetGo — MERN E-Commerce Platform

> A full-stack e-commerce platform for discovering and purchasing gadgets, built with the MERN stack.

🔗 **Live Demo:** https://webecommerce.onrender.com/

GadgetGo is a full-stack web application that demonstrates the development of an e-commerce platform using **React, Node.js, Express, and MongoDB**.

The application provides a complete shopping workflow including product browsing, user authentication, cart management, checkout, and order handling.

---

## ✨ Features

### 👤 User Features

- User registration and login
- JWT-based authentication
- Protected routes
- User account management
- Secure password hashing

### 🛍️ Shopping

- Browse available gadgets
- Product details
- Product search and navigation
- Add products to cart
- Update cart quantities
- Remove products from cart
- Checkout workflow

### 📦 Orders

- Place orders
- View order information
- Order management
- Order status handling

### 💳 Payments

- Integrated payment workflow using Braintree

### ⚙️ Backend

- RESTful API architecture
- Express.js server
- MongoDB database
- Mongoose ODM
- Authentication middleware
- Controller-based API structure
- Modular routes and models

---

## 🏗️ Architecture

```text
                    ┌────────────────────┐
                    │       User         │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │   React Frontend   │
                    │      /client       │
                    └─────────┬──────────┘
                              │
                         HTTP / REST
                              │
                              ▼
                    ┌────────────────────┐
                    │   Express Server   │
                    │     server.js      │
                    └─────────┬──────────┘
                              │
              ┌───────────────┼────────────────┐
              │               │                │
              ▼               ▼                ▼
        ┌──────────┐    ┌────────────┐   ┌────────────┐
        │  Routes  │    │ Middleware │   │ Controllers│
        └────┬─────┘    └────────────┘   └─────┬──────┘
             │                                  │
             └────────────────┬─────────────────┘
                              ▼
                    ┌────────────────────┐
                    │      Mongoose      │
                    │    Data Models     │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │      MongoDB       │
                    └────────────────────┘

                              │
                              ▼
                    ┌────────────────────┐
                    │     Braintree      │
                    │    Payment Flow    │
                    └────────────────────┘
