# 🛒 Store.G02

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Node](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen.svg)
![React](https://img.shields.io/badge/react-%5E18.0.0-61dafb.svg)
![Express](https://img.shields.io/badge/express-%5E4.18.0-lightgrey.svg)
![MongoDB](https://img.shields.io/badge/mongodb-%5E6.0.0-47A248.svg)

**A modern, full-stack e-commerce platform built with the MERN stack**

[Demo](#) · [Documentation](#) · [Report Bug](https://github.com/AbdullahM0hammed/Store.G02/issues) · [Request Feature](https://github.com/AbdullahM0hammed/Store.G02/issues)

</div>

---

## 📋 Table of Contents

- [About The Project](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
- [Usage](#-usage)
- [Project Architecture](#-project-architecture)
- [API Documentation](#-api-documentation)
- [Database Schema](#-database-schema)
- [Folder Structure](#-folder-structure)
- [Screenshots](#-screenshots)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 About The Project

Store.G02 is a comprehensive e-commerce solution designed to provide a seamless shopping experience for customers and powerful management tools for administrators. Built with modern web technologies, it offers a scalable, maintainable, and feature-rich platform for online retail operations.

### Why Store.G02?

- **🚀 Fast & Responsive**: Optimized performance with server-side rendering and lazy loading
- **🔒 Secure**: Industry-standard authentication and authorization with JWT
- **📱 Mobile-First**: Fully responsive design that works on all devices
- **⚡ Real-Time**: Live updates for inventory, orders, and notifications
- **🎨 Modern UI**: Clean, intuitive interface built with React and modern CSS
- **🛡️ Production-Ready**: Comprehensive error handling, logging, and monitoring

---

## ✨ Features

### Customer Features
- 🔐 **User Authentication & Authorization**
  - Secure registration and login
  - JWT-based session management
  - Password recovery and email verification
  - Social media authentication (Google, Facebook)

- 🛍️ **Product Browsing & Search**
  - Advanced filtering and sorting
  - Category-based navigation
  - Full-text search with autocomplete
  - Product recommendations

- 🛒 **Shopping Cart**
  - Persistent cart across sessions
  - Real-time price calculations
  - Quantity management
  - Save for later functionality

- 💳 **Checkout & Payment**
  - Multiple payment methods (Credit Card, PayPal, Stripe)
  - Guest checkout option
  - Order summary and validation
  - Secure payment processing

- 📦 **Order Management**
  - Order history and tracking
  - Order status updates
  - Invoice generation
  - Return and refund requests

- 👤 **User Profile**
  - Account settings management
  - Address book
  - Wishlist functionality
  - Order history

### Admin Features
- 📊 **Dashboard Analytics**
  - Sales statistics and charts
  - User activity metrics
  - Inventory insights
  - Revenue reports

- 📦 **Product Management**
  - CRUD operations for products
  - Bulk product upload
  - Inventory tracking
  - Category management

- 👥 **User Management**
  - View and manage customers
  - Role-based access control
  - User activity logs

- 🎫 **Order Processing**
  - Order fulfillment workflow
  - Status management
  - Shipping label generation
  - Refund processing

- 📧 **Communication**
  - Email notifications
  - Customer support chat
  - Promotional campaigns

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 18.x
- **State Management**: Redux Toolkit
- **Routing**: React Router v6
- **Styling**: 
  - Tailwind CSS / Material-UI
  - CSS Modules
  - Styled Components
- **Form Handling**: React Hook Form
- **HTTP Client**: Axios
- **Build Tool**: Vite / Create React App

### Backend
- **Runtime**: Node.js 14+
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT (JSON Web Tokens)
- **Validation**: Joi / Express Validator
- **File Upload**: Multer
- **Email**: Nodemailer

### DevOps & Tools
- **Version Control**: Git
- **Package Manager**: npm / yarn
- **API Testing**: Postman / Thunder Client
- **Code Quality**: ESLint, Prettier
- **Testing**: Jest, React Testing Library

### Third-Party Services
- **Payment Gateway**: Stripe / PayPal
- **Cloud Storage**: Cloudinary / AWS S3
- **Email Service**: SendGrid / Mailgun
- **Deployment**: Heroku / Vercel / AWS

---

## 🚀 Getting Started

### Prerequisites

Before running this project, make sure you have the following installed:

```bash
node --version  # v14.0.0 or higher
npm --version   # v6.0.0 or higher
```

You'll also need:
- MongoDB installed locally or a MongoDB Atlas account
- A code editor (VS Code recommended)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/AbdullahM0hammed/Store.G02.git
   cd Store.G02
   ```

2. **Install Backend Dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Set up Environment Variables**
   
   Create `.env` files in both `backend` and `frontend` directories (see [Environment Variables](#environment-variables) section below)

5. **Initialize Database**
   ```bash
   cd backend
   npm run seed  # Optional: seed database with sample data
   ```

6. **Run the Application**

   **Backend** (Terminal 1):
   ```bash
   cd backend
   npm run dev  # Runs on http://localhost:5000
   ```

   **Frontend** (Terminal 2):
   ```bash
   cd frontend
   npm start  # Runs on http://localhost:3000
   ```

7. **Access the Application**
   
   Open your browser and navigate to `http://localhost:3000`

### Environment Variables

#### Backend `.env`

Create a `.env` file in the `backend` directory:

```env
# Server Configuration
NODE_ENV=development
PORT=5000

# Database
MONGO_URI=mongodb://localhost:27017/store_g02
# Or for MongoDB Atlas:
# MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/store_g02

# JWT Configuration
JWT_SECRET=your_super_secret_jwt_key_change_this_in_production
JWT_EXPIRE=30d

# Email Configuration (SendGrid)
EMAIL_SERVICE=SendGrid
EMAIL_HOST=smtp.sendgrid.net
EMAIL_PORT=587
EMAIL_USERNAME=apikey
EMAIL_PASSWORD=your_sendgrid_api_key
EMAIL_FROM=noreply@storeg02.com

# Payment Gateway (Stripe)
STRIPE_SECRET_KEY=sk_test_your_stripe_secret_key
STRIPE_PUBLISHABLE_KEY=pk_test_your_stripe_publishable_key

# PayPal
PAYPAL_CLIENT_ID=your_paypal_client_id
PAYPAL_CLIENT_SECRET=your_paypal_client_secret

# Cloud Storage (Cloudinary)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# OAuth (Optional)
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
FACEBOOK_APP_ID=your_facebook_app_id
FACEBOOK_APP_SECRET=your_facebook_app_secret

# Other
CLIENT_URL=http://localhost:3000
ADMIN_EMAIL=admin@storeg02.com
```

#### Frontend `.env`

Create a `.env` file in the `frontend` directory:

```env
# API Configuration
REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_SOCKET_URL=http://localhost:5000

# Stripe
REACT_APP_STRIPE_PUBLISHABLE_KEY=pk_test_your_stripe_publishable_key

# PayPal
REACT_APP_PAYPAL_CLIENT_ID=your_paypal_client_id

# Google Maps (if used)
REACT_APP_GOOGLE_MAPS_API_KEY=your_google_maps_api_key

# Other
REACT_APP_ENV=development
```

---

## 📖 Usage

### For Customers

1. **Browse Products**: Navigate through categories or use the search bar
2. **Add to Cart**: Click "Add to Cart" on any product
3. **Checkout**: Review cart and proceed to checkout
4. **Payment**: Enter shipping details and payment information
5. **Track Order**: View order status in your profile

### For Administrators

1. **Login**: Access admin panel at `/admin/login`
2. **Dashboard**: View analytics and key metrics
3. **Manage Products**: Add, edit, or remove products
4. **Process Orders**: Update order statuses and manage fulfillment
5. **Customer Management**: View and manage user accounts

### Default Admin Credentials

```
Email: admin@storeg02.com
Password: Admin@123
```

**⚠️ Important**: Change these credentials immediately in production!

---

## 🏗️ Project Architecture

Store.G02 follows a **three-tier architecture** pattern:

```
┌─────────────────────────────────────────────────────────┐
│                     Client Layer                        │
│              (React + Redux Frontend)                   │
└──────────────────────┬──────────────────────────────────┘
                       │ HTTP/REST API
┌──────────────────────┴──────────────────────────────────┐
│                   Business Layer                        │
│         (Node.js + Express.js Backend)                  │
│                                                          │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐ │
│  │   Routes     │  │ Controllers  │  │  Middleware  │ │
│  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘ │
│         │                  │                  │          │
│  ┌──────┴──────────────────┴──────────────────┴──────┐ │
│  │              Service Layer                         │ │
│  └────────────────────────┬───────────────────────────┘ │
└───────────────────────────┴─────────────────────────────┘
                            │
┌───────────────────────────┴─────────────────────────────┐
│                    Data Layer                           │
│                (MongoDB Database)                       │
│                                                          │
│  Collections: Users, Products, Orders, Categories, etc. │
└─────────────────────────────────────────────────────────┘
```

### Key Design Patterns

- **MVC Architecture**: Separation of concerns between Model, View, and Controller
- **RESTful API**: Standardized HTTP methods and endpoints
- **Repository Pattern**: Data access abstraction layer
- **Middleware Chain**: Request processing pipeline
- **JWT Authentication**: Stateless authentication mechanism

---

## 📡 API Documentation

### Base URL
```
http://localhost:5000/api
```

### Authentication
Most endpoints require authentication. Include the JWT token in the Authorization header:
```
Authorization: Bearer <your_jwt_token>
```

### Endpoints Overview

#### Authentication
```http
POST   /api/auth/register          # Register new user
POST   /api/auth/login             # Login user
POST   /api/auth/logout            # Logout user
GET    /api/auth/me                # Get current user
PUT    /api/auth/update-details    # Update user details
PUT    /api/auth/update-password   # Update password
POST   /api/auth/forgot-password   # Request password reset
PUT    /api/auth/reset-password/:token  # Reset password
```

#### Products
```http
GET    /api/products               # Get all products
GET    /api/products/:id           # Get single product
POST   /api/products               # Create product (Admin)
PUT    /api/products/:id           # Update product (Admin)
DELETE /api/products/:id           # Delete product (Admin)
GET    /api/products/search        # Search products
```

#### Categories
```http
GET    /api/categories             # Get all categories
GET    /api/categories/:id         # Get category by ID
POST   /api/categories             # Create category (Admin)
PUT    /api/categories/:id         # Update category (Admin)
DELETE /api/categories/:id         # Delete category (Admin)
```

#### Cart
```http
GET    /api/cart                   # Get user's cart
POST   /api/cart/add               # Add item to cart
PUT    /api/cart/update/:itemId    # Update cart item
DELETE /api/cart/remove/:itemId    # Remove item from cart
DELETE /api/cart/clear             # Clear entire cart
```

#### Orders
```http
GET    /api/orders                 # Get user's orders
GET    /api/orders/:id             # Get order by ID
POST   /api/orders                 # Create new order
PUT    /api/orders/:id             # Update order status (Admin)
GET    /api/orders/admin/all       # Get all orders (Admin)
```

#### Users (Admin)
```http
GET    /api/users                  # Get all users
GET    /api/users/:id              # Get user by ID
PUT    /api/users/:id              # Update user
DELETE /api/users/:id              # Delete user
```

### Example Request

**Login User**
```bash
curl -X POST http://localhost:5000/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "user@example.com",
    "password": "password123"
  }'
```

**Response**
```json
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "user": {
    "id": "60d5ec49f1b2c72b8c8e4f1a",
    "name": "John Doe",
    "email": "user@example.com",
    "role": "user"
  }
}
```

For detailed API documentation with request/response examples, visit `/api/docs` when running the server.

---

## 🗄️ Database Schema

### Entity Relationship Diagram

```
┌─────────────────┐         ┌─────────────────┐
│      User       │         │    Category     │
├─────────────────┤         ├─────────────────┤
│ _id             │         │ _id             │
│ name            │         │ name            │
│ email           │◄───┐    │ description     │
│ password        │    │    │ image           │
│ role            │    │    │ createdAt       │
│ phone           │    │    └─────────────────┘
│ address         │    │              │
│ createdAt       │    │              │ belongs to
│ updatedAt       │    │              ▼
└─────────────────┘    │    ┌─────────────────┐
         │             │    │    Product      │
         │ places      │    ├─────────────────┤
         ▼             │    │ _id             │
┌─────────────────┐   │    │ name            │
│     Order       │   │    │ description     │
├─────────────────┤   │    │ price           │
│ _id             │   │    │ category        │
│ user            │───┘    │ images[]        │
│ items[]         │        │ stock           │
│  - product      │───┐    │ rating          │
│  - quantity     │   │    │ reviews[]       │
│  - price        │   │    │ createdAt       │
│ totalPrice      │   │    │ updatedAt       │
│ status          │   │    └─────────────────┘
│ paymentInfo     │   │              ▲
│  - method       │   │              │
│  - status       │   └──────────────┘
│  - transactionId│         references
│ shippingAddress │
│ createdAt       │
│ updatedAt       │
└─────────────────┘
         │
         │ contains
         ▼
┌─────────────────┐
│     Review      │
├─────────────────┤
│ _id             │
│ user            │───┐
│ product         │   │
│ rating          │   │
│ comment         │   │
│ createdAt       │   │
└─────────────────┘   │
                      │
         ┌────────────┘
         │ wrote
         ▼
   (back to User)
```

### Collections

#### Users Collection
```javascript
{
  _id: ObjectId,
  name: String (required),
  email: String (required, unique),
  password: String (required, hashed),
  role: String (enum: ['user', 'admin'], default: 'user'),
  phone: String,
  avatar: String (URL),
  addresses: [{
    street: String,
    city: String,
    state: String,
    country: String,
    zipCode: String,
    isDefault: Boolean
  }],
  wishlist: [ObjectId] (ref: 'Product'),
  resetPasswordToken: String,
  resetPasswordExpire: Date,
  createdAt: Date,
  updatedAt: Date
}
```

#### Products Collection
```javascript
{
  _id: ObjectId,
  name: String (required),
  description: String (required),
  price: Number (required),
  category: ObjectId (ref: 'Category'),
  images: [String] (URLs),
  stock: Number (default: 0),
  sold: Number (default: 0),
  rating: Number (default: 0),
  numReviews: Number (default: 0),
  reviews: [{
    user: ObjectId (ref: 'User'),
    name: String,
    rating: Number,
    comment: String,
    createdAt: Date
  }],
  featured: Boolean (default: false),
  createdAt: Date,
  updatedAt: Date
}
```

#### Orders Collection
```javascript
{
  _id: ObjectId,
  user: ObjectId (ref: 'User'),
  orderItems: [{
    product: ObjectId (ref: 'Product'),
    name: String,
    quantity: Number,
    image: String,
    price: Number
  }],
  shippingAddress: {
    street: String,
    city: String,
    state: String,
    country: String,
    zipCode: String
  },
  paymentMethod: String (enum: ['card', 'paypal', 'cash']),
  paymentResult: {
    id: String,
    status: String,
    update_time: String,
    email_address: String
  },
  taxPrice: Number,
  shippingPrice: Number,
  totalPrice: Number,
  isPaid: Boolean (default: false),
  paidAt: Date,
  isDelivered: Boolean (default: false),
  deliveredAt: Date,
  status: String (enum: ['pending', 'processing', 'shipped', 'delivered', 'cancelled']),
  createdAt: Date,
  updatedAt: Date
}
```

---

## 📁 Folder Structure

```
Store.G02/
│
├── backend/
│   ├── config/
│   │   ├── db.js                 # Database connection
│   │   └── config.env            # Environment variables
│   │
│   ├── controllers/
│   │   ├── authController.js     # Authentication logic
│   │   ├── productController.js  # Product operations
│   │   ├── orderController.js    # Order management
│   │   ├── userController.js     # User management
│   │   └── categoryController.js # Category operations
│   │
│   ├── middleware/
│   │   ├── auth.js               # JWT authentication
│   │   ├── error.js              # Error handling
│   │   ├── async.js              # Async handler
│   │   └── validate.js           # Input validation
│   │
│   ├── models/
│   │   ├── User.js               # User schema
│   │   ├── Product.js            # Product schema
│   │   ├── Order.js              # Order schema
│   │   ├── Category.js           # Category schema
│   │   └── Review.js             # Review schema
│   │
│   ├── routes/
│   │   ├── auth.js               # Auth routes
│   │   ├── products.js           # Product routes
│   │   ├── orders.js             # Order routes
│   │   ├── users.js              # User routes
│   │   └── categories.js         # Category routes
│   │
│   ├── utils/
│   │   ├── sendEmail.js          # Email utility
│   │   ├── generateToken.js      # JWT generator
│   │   └── errorResponse.js      # Custom error class
│   │
│   ├── seeds/
│   │   └── seed.js               # Database seeder
│   │
│   ├── server.js                 # Entry point
│   ├── package.json
│   └── .env
│
├── frontend/
│   ├── public/
│   │   ├── index.html
│   │   └── favicon.ico
│   │
│   ├── src/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   │   ├── Header.jsx
│   │   │   │   ├── Footer.jsx
│   │   │   │   ├── Navbar.jsx
│   │   │   │   └── Loader.jsx
│   │   │   │
│   │   │   ├── product/
│   │   │   │   ├── ProductCard.jsx
│   │   │   │   ├── ProductList.jsx
│   │   │   │   └── ProductFilter.jsx
│   │   │   │
│   │   │   ├── cart/
│   │   │   │   ├── CartItem.jsx
│   │   │   │   └── CartSummary.jsx
│   │   │   │
│   │   │   └── admin/
│   │   │       ├── AdminSidebar.jsx
│   │   │       └── AdminDashboard.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── ProductDetails.jsx
│   │   │   ├── Cart.jsx
│   │   │   ├── Checkout.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── Profile.jsx
│   │   │   ├── Orders.jsx
│   │   │   └── admin/
│   │   │       ├── Dashboard.jsx
│   │   │       ├── ProductManagement.jsx
│   │   │       └── OrderManagement.jsx
│   │   │
│   │   ├── redux/
│   │   │   ├── store.js
│   │   │   ├── slices/
│   │   │   │   ├── authSlice.js
│   │   │   │   ├── productSlice.js
│   │   │   │   ├── cartSlice.js
│   │   │   │   └── orderSlice.js
│   │   │   └── actions/
│   │   │
│   │   ├── services/
│   │   │   ├── api.js            # Axios configuration
│   │   │   ├── authService.js
│   │   │   ├── productService.js
│   │   │   └── orderService.js
│   │   │
│   │   ├── hooks/
│   │   │   ├── useAuth.js
│   │   │   └── useCart.js
│   │   │
│   │   ├── utils/
│   │   │   ├── constants.js
│   │   │   ├── helpers.js
│   │   │   └── validators.js
│   │   │
│   │   ├── styles/
│   │   │   ├── global.css
│   │   │   └── variables.css
│   │   │
│   │   ├── App.jsx
│   │   ├── index.js
│   │   └── routes.js
│   │
│   ├── package.json
│   └── .env
│
├── .gitignore
├── README.md
└── LICENSE
```

---

## 📸 Screenshots

### Homepage
![Homepage](./screenshots/homepage.png)
*Modern, responsive landing page with featured products*

### Product Catalog
![Product Catalog](./screenshots/catalog.png)
*Advanced filtering and search functionality*

### Product Details
![Product Details](./screenshots/product-details.png)
*Detailed product view with reviews and recommendations*

### Shopping Cart
![Shopping Cart](./screenshots/cart.png)
*Intuitive cart management with real-time updates*

### Checkout Process
![Checkout](./screenshots/checkout.png)
*Seamless multi-step checkout experience*

### Admin Dashboard
![Admin Dashboard](./screenshots/admin-dashboard.png)
*Comprehensive analytics and management tools*

### Order Management
![Order Management](./screenshots/orders.png)
*Efficient order tracking and fulfillment*

> **Note**: Screenshots are placeholders. Replace with actual images by creating a `screenshots/` folder and adding your application screenshots.

---

## 🗺️ Roadmap

### Current Version (v1.0.0)
- ✅ User authentication and authorization
- ✅ Product catalog with search and filtering
- ✅ Shopping cart functionality
- ✅ Checkout and payment processing
- ✅ Order management
- ✅ Admin dashboard

### Upcoming Features (v1.1.0)
- [ ] Multi-language support (i18n)
- [ ] Dark mode theme
- [ ] Advanced analytics dashboard
- [ ] Real-time chat support
- [ ] Product comparison feature
- [ ] Customer reviews and ratings system

### Future Enhancements (v2.0.0)
- [ ] Mobile application (React Native)
- [ ] Progressive Web App (PWA) support
- [ ] AI-powered product recommendations
- [ ] Inventory management system
- [ ] Multi-vendor marketplace support
- [ ] Subscription and recurring payments
- [ ] Social media integration
- [ ] Advanced SEO optimization
- [ ] GraphQL API implementation
- [ ] Microservices architecture migration

### Long-term Goals
- [ ] Blockchain-based payment options
- [ ] AR/VR product visualization
- [ ] Voice commerce integration
- [ ] Predictive analytics for inventory

See the [open issues](https://github.com/AbdullahM0hammed/Store.G02/issues) for a full list of proposed features and known issues.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

### How to Contribute

1. **Fork the Project**
   ```bash
   # Click the 'Fork' button at the top right of this page
   ```

2. **Clone Your Fork**
   ```bash
   git clone https://github.com/your-username/Store.G02.git
   cd Store.G02
   ```

3. **Create a Feature Branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

4. **Make Your Changes**
   - Write clean, documented code
   - Follow the existing code style
   - Add tests if applicable

5. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "Add some AmazingFeature"
   ```

6. **Push to Your Fork**
   ```bash
   git push origin feature/AmazingFeature
   ```

7. **Open a Pull Request**
   - Go to the original repository
   - Click "New Pull Request"
   - Select your fork and branch
   - Describe your changes in detail

### Contribution Guidelines

- **Code Style**: Follow the existing code style and conventions
- **Commits**: Write clear, concise commit messages
- **Documentation**: Update README.md if you add new features
- **Testing**: Ensure all tests pass before submitting PR
- **Issues**: Check existing issues before creating new ones

### Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` file for more information.

```
MIT License

Copyright (c) 2024 Abdullah Mohammed

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📞 Contact

**Abdullah Mohammed**

- GitHub: [@AbdullahM0hammed](https://github.com/AbdullahM0hammed)
- Email: contactabdullah.mohammed.mahmoud.emam@gmail.com

**Project Link**: [https://github.com/AbdullahM0hammed/Store.G02](https://github.com/AbdullahM0hammed/Store.G02)

---

## 🙏 Acknowledgments

### Technologies & Libraries
- [React](https://reactjs.org/) - A JavaScript library for building user interfaces
- [Node.js](https://nodejs.org/) - JavaScript runtime built on Chrome's V8 engine
- [Express.js](https://expressjs.com/) - Fast, unopinionated, minimalist web framework
- [MongoDB](https://www.mongodb.com/) - NoSQL database for modern applications
- [Redux Toolkit](https://redux-toolkit.js.org/) - The official, opinionated, batteries-included toolset for Redux
- [Tailwind CSS](https://tailwindcss.com/) - A utility-first CSS framework
- [Stripe](https://stripe.com/) - Online payment processing platform
- [JWT](https://jwt.io/) - JSON Web Tokens for secure authentication

### Resources & Inspiration
- [MDN Web Docs](https://developer.mozilla.org/) - Comprehensive web development documentation
- [Stack Overflow](https://stackoverflow.com/) - Community-driven Q&A platform
- [GitHub](https://github.com/) - Version control and collaboration platform
- Design inspiration from [Dribbble](https://dribbble.com/) and [Behance](https://behance.net/)

### Special Thanks
- All contributors who have helped improve this project
- The open-source community for their invaluable tools and libraries
- Beta testers who provided feedback during development
- Everyone who has starred or forked this repository

### Educational Resources
- [freeCodeCamp](https://www.freecodecamp.org/) - Learn to code for free
- [Traversy Media](https://www.traversymedia.com/) - Web development tutorials
- [The Net Ninja](https://www.thenetninja.co.uk/) - Programming tutorials
- [Academind](https://academind.com/) - Online courses for developers

---

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/AbdullahM0hammed/Store.G02?style=social)
![GitHub forks](https://img.shields.io/github/forks/AbdullahM0hammed/Store.G02?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/AbdullahM0hammed/Store.G02?style=social)
![GitHub issues](https://img.shields.io/github/issues/AbdullahM0hammed/Store.G02)
![GitHub pull requests](https://img.shields.io/github/issues-pr/AbdullahM0hammed/Store.G02)
![GitHub last commit](https://img.shields.io/github/last-commit/AbdullahM0hammed/Store.G02)

---

## 🔒 Security

If you discover a security vulnerability within Store.G02, please send an email to security@abdullahmohammed.dev. All security vulnerabilities will be promptly addressed.

### Security Best Practices Implemented

- ✅ Password hashing with bcrypt
- ✅ JWT-based authentication
- ✅ Input validation and sanitization
- ✅ Protection against SQL injection and NoSQL injection
- ✅ XSS (Cross-Site Scripting) prevention
- ✅ CSRF (Cross-Site Request Forgery) protection
- ✅ Rate limiting on API endpoints
- ✅ HTTPS enforcement in production
- ✅ Secure HTTP headers (Helmet.js)
- ✅ Environment variables for sensitive data

---

## 🧪 Testing

### Running Tests

**Backend Tests**
```bash
cd backend
npm test                 # Run all tests
npm run test:watch      # Run tests in watch mode
npm run test:coverage   # Generate coverage report
```

**Frontend Tests**
```bash
cd frontend
npm test                # Run all tests
npm run test:coverage   # Generate coverage report
```

### Test Coverage

The project maintains a minimum of 80% test coverage across all modules.

```
Backend Coverage:
- Controllers: 85%
- Models: 90%
- Routes: 88%
- Utils: 92%

Frontend Coverage:
- Components: 82%
- Redux: 86%
- Services: 89%
- Utils: 91%
```

---

## 🚀 Deployment

### Production Deployment Guide

#### Backend Deployment (Heroku)

1. **Create Heroku App**
   ```bash
   heroku create store-g02-api
   ```

2. **Set Environment Variables**
   ```bash
   heroku config:set NODE_ENV=production
   heroku config:set MONGO_URI=your_mongodb_atlas_uri
   heroku config:set JWT_SECRET=your_production_jwt_secret
   # Add all other environment variables
   ```

3. **Deploy**
   ```bash
   git push heroku main
   ```

#### Frontend Deployment (Vercel)

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Deploy**
   ```bash
   cd frontend
   vercel --prod
   ```

3. **Configure Environment Variables**
   - Go to Vercel Dashboard → Project Settings → Environment Variables
   - Add all required environment variables

#### Alternative: Docker Deployment

```dockerfile
# Use the Dockerfile provided in the repository
docker-compose up -d
```

---

## 💡 Tips & Troubleshooting

### Common Issues

**Problem**: MongoDB connection failed
```
Solution: Ensure MongoDB is running and the connection string is correct
```

**Problem**: CORS errors in development
```
Solution: Check that the CLIENT_URL in backend .env matches your frontend URL
```

**Problem**: Payment processing fails
```
Solution: Verify Stripe API keys are correctly configured in both backend and frontend
```

**Problem**: Images not uploading
```
Solution: Check Cloudinary credentials and ensure file size is within limits
```

### Performance Optimization

- Enable gzip compression in production
- Implement Redis caching for frequently accessed data
- Use CDN for static assets
- Optimize images before upload
- Implement lazy loading for React components
- Use MongoDB indexing for faster queries

---

## 📚 Additional Documentation

- [API Documentation](./docs/API.md) - Detailed API endpoint documentation
- [Database Schema](./docs/DATABASE.md) - Complete database schema reference
- [Deployment Guide](./docs/DEPLOYMENT.md) - Step-by-step deployment instructions
- [Contributing Guide](./docs/CONTRIBUTING.md) - How to contribute to the project
- [Changelog](./CHANGELOG.md) - Version history and updates

---

## 🌟 Show Your Support

Give a ⭐️ if this project helped you!

<div align="center">

[![Star History Chart](https://api.star-history.com/svg?repos=AbdullahM0hammed/Store.G02&type=Date)](https://star-history.com/#AbdullahM0hammed/Store.G02&Date)

</div>

---

## 📈 Version History

### v1.0.0 (Current)
- Initial release
- Core e-commerce functionality
- User authentication and authorization
- Product catalog and management
- Shopping cart and checkout
- Order processing and tracking
- Admin dashboard

### v0.9.0 (Beta)
- Beta testing phase
- Bug fixes and improvements
- Performance optimization
- Security enhancements

### v0.5.0 (Alpha)
- Alpha release
- Basic functionality implementation
- Initial testing

---

<div align="center">

### Made with ❤️ by [Abdullah Mohammed](https://github.com/AbdullahM0hammed)

**If you found this project useful, please consider giving it a star ⭐**

[Report Bug](https://github.com/AbdullahM0hammed/Store.G02/issues) · [Request Feature](https://github.com/AbdullahM0hammed/Store.G02/issues) · [Contribute](https://github.com/AbdullahM0hammed/Store.G02/pulls)

---

**© 2024 Store.G02. All Rights Reserved.**

</div>
