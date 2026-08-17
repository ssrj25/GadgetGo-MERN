# 🛒 GadgetGo — MERN E-Commerce Platform

> A full-stack e-commerce platform built with the MERN stack for browsing gadgets, managing shopping carts, authenticating users, processing orders, and handling payments.

🌐 **Live Demo:** https://webecommerce.onrender.com/

---

## 📸 Screenshots

### Homepage
<img width="1898" height="945" alt="Screenshot 2026-08-17 231829" src="https://github.com/user-attachments/assets/0ff05adf-d5e7-4669-9898-5eed19120a2f" />

### Register Page

<img width="1891" height="944" alt="Screenshot 2026-08-17 232012" src="https://github.com/user-attachments/assets/0999e23f-885f-4307-bd3d-a1cde976bb3f" />

### Filter Product Listing

<img width="1887" height="941" alt="Screenshot 2026-08-17 231913" src="https://github.com/user-attachments/assets/5bd6f2ef-6fcd-467c-a79c-1a81ce467e19" />

### Shopping Cart

<img width="1898" height="945" alt="Screenshot 2026-08-17 231829" src="https://github.com/user-attachments/assets/f3b9ac29-96e6-45c7-9ed1-ebb2157ef3a1" />

---

## ✨ Features

### 👤 User Authentication

* User registration and login
* JWT-based authentication
* Protected routes
* Secure password hashing using bcrypt

### 🛍️ Product & Shopping

* Browse available gadgets
* View product details
* Add products to cart
* Update product quantities
* Remove products from cart
* Complete shopping workflow

### 📦 Orders

* Create orders
* Store order information
* View order details
* Manage order workflow

### 💳 Payments

* Integrated Braintree payment workflow
* Secure payment processing flow

### ⚙️ Backend

* RESTful API architecture
* Express.js backend
* MongoDB database
* Mongoose ODM
* Controller-based architecture
* Route-based API organization
* Authentication middleware

---

## 🏗️ System Architecture

```text
                    ┌───────────────────┐
                    │       User        │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │  React Frontend   │
                    │      /client      │
                    └─────────┬─────────┘
                              │
                         HTTP / REST
                              │
                              ▼
                    ┌───────────────────┐
                    │ Express.js Server │
                    │     server.js     │
                    └─────────┬─────────┘
                              │
              ┌───────────────┼────────────────┐
              │               │                │
              ▼               ▼                ▼
       ┌────────────┐  ┌────────────┐  ┌─────────────┐
       │   Routes   │  │ Middleware │  │ Controllers │
       └─────┬──────┘  └────────────┘  └──────┬──────┘
             │                                │
             └────────────────┬───────────────┘
                              ▼
                    ┌───────────────────┐
                    │     Mongoose      │
                    │      Models       │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │      MongoDB      │
                    └───────────────────┘

                              │
                              ▼
                    ┌───────────────────┐
                    │     Braintree     │
                    │ Payment Processing │
                    └───────────────────┘
```

---

## 🔄 Application Flow

### 1. Authentication Flow

```text
User
  ↓
React Login / Registration
  ↓
Express REST API
  ↓
Authentication & Validation
  ↓
Password Verification
  ↓
JWT Token
  ↓
Authenticated User
```

### 2. Product Browsing Flow

```text
User
  ↓
React Product Interface
  ↓
REST API Request
  ↓
Express Route
  ↓
Controller
  ↓
Mongoose
  ↓
MongoDB
  ↓
Product Data
  ↓
React UI
```

### 3. Shopping Cart Flow

```text
Browse Products
      ↓
Product Details
      ↓
Add to Cart
      ↓
Update Quantity
      ↓
Remove Items
      ↓
Checkout
```

### 4. Order & Payment Flow

```text
Shopping Cart
      ↓
Checkout
      ↓
Payment Request
      ↓
Braintree
      ↓
Payment Result
      ↓
Create Order
      ↓
MongoDB
      ↓
Order Confirmation
```

### 5. Backend Request Flow

```text
React Frontend
      ↓
HTTP Request
      ↓
Express Route
      ↓
Middleware
      ↓
Controller
      ↓
Mongoose Model
      ↓
MongoDB
      ↓
HTTP Response
      ↓
React Frontend
```

---

## 🧰 Tech Stack

| Category          | Technology             |
| ----------------- | ---------------------- |
| Frontend          | React, JavaScript      |
| Backend           | Node.js, Express.js    |
| Database          | MongoDB                |
| ODM               | Mongoose               |
| Authentication    | JWT                    |
| Password Security | bcrypt                 |
| Payments          | Braintree              |
| API               | REST                   |
| UI                | React Icons, HTML, CSS |
| Configuration     | dotenv                 |
| Development       | Nodemon, npm           |
| Deployment        | Render                 |

---

## 📁 Project Structure

```text
GadgetGo-MERN/
│
├── client/                 # React frontend
│
├── config/                 # Backend configuration
│
├── controllers/            # Business and request logic
│
├── helpers/                # Reusable helper functions
│
├── middlewares/            # Authentication and request middleware
│
├── models/                 # MongoDB/Mongoose models
│
├── routes/                 # REST API routes
│
├── server.js               # Express server entry point
│
├── package.json            # Project dependencies and scripts
├── package-lock.json       # Dependency lock file
└── README.md               # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

* Node.js
* npm
* MongoDB or MongoDB Atlas
* Git

---

### 1. Clone the repository

```bash
git clone https://github.com/ssrj25/GadgetGo-MERN.git

cd GadgetGo-MERN
```

---

### 2. Install backend dependencies

```bash
npm install
```

---

### 3. Install frontend dependencies

```bash
cd client
npm install
cd ..
```

---

### 4. Configure environment variables

Create a `.env` file in the project root and add the environment variables required by the application.

Example:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret

BRAINTREE_MERCHANT_ID=your_braintree_merchant_id
BRAINTREE_PUBLIC_KEY=your_braintree_public_key
BRAINTREE_PRIVATE_KEY=your_braintree_private_key
```

> Use the exact variable names expected by the application. Never commit real credentials or secrets to GitHub.

---

### 5. Run the application

Start the backend:

```bash
npm run server
```

Start the frontend:

```bash
npm run client
```

If the project provides a combined development script:

```bash
npm run dev
```

---

## 🔐 Security

GadgetGo implements several common web application security practices:

* JWT-based authentication
* Password hashing using bcrypt
* Protected routes
* Authentication middleware
* Environment variables for sensitive configuration
* Server-side API handling

---

## 🎯 Key Engineering Concepts

This project demonstrates practical experience with:

* Full-stack MERN development
* React frontend development
* Node.js backend development
* Express REST APIs
* MongoDB data modeling
* Mongoose ODM
* CRUD operations
* JWT authentication
* Authorization middleware
* Password hashing
* Client-server communication
* Shopping cart workflows
* Order management
* Payment integration
* Modular backend architecture
* Deployment

---

## 💡 What I Learned

Building GadgetGo helped me understand how the major layers of a full-stack application work together:

```text
React
  ↓
REST API
  ↓
Express
  ↓
Controllers
  ↓
Mongoose
  ↓
MongoDB
```

I also gained practical experience with authentication, protected routes, cart management, order processing, and payment integration.

---

## 🌐 Live Demo

**GadgetGo:**
https://webecommerce.onrender.com/

---

## 👩‍💻 Author

**Shreya Singh**

GitHub: https://github.com/ssrj25

---

## 📄 License

This project is licensed under the MIT License.
