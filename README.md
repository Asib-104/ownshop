# OwnShop - E-commerce Platform

A full-featured e-commerce platform built with the MERN stack (MongoDB, Express.js, React, Node.js).

## Features

- **Product Management**: Browse products with detailed views, ratings, and reviews
- **Shopping Cart**: Add items to cart and manage quantities
- **User Authentication**: Register, login, and user profile management
- **Order Management**: Place orders, payment processing, and order history
- **Admin Panel**: Manage products, users, and orders
- **Payment Integration**: PayPal integration for secure payments
- **Product Search & Pagination**: Search products and navigate through pages
- **Product Reviews & Ratings**: User reviews and rating system

## Tech Stack

### Frontend
- React.js
- Redux Toolkit for state management
- React Bootstrap for UI components
- React Router for navigation

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose ODM
- JWT for authentication
- Bcrypt for password hashing

### Additional Tools
- PayPal API for payments
- Multer for file uploads
- CORS for cross-origin requests

## Project Structure

```
proshop-v2/
├── backend/                 # Backend API
│   ├── config/             # Database configuration
│   ├── controllers/        # Route controllers
│   ├── data/              # Sample data
│   ├── middleware/        # Custom middleware
│   ├── models/            # Database models
│   ├── routes/            # API routes
│   └── utils/             # Utility functions
├── frontend/              # React frontend
│   ├── public/            # Static assets
│   └── src/
│       ├── components/    # Reusable components
│       ├── screens/       # Page components
│       ├── slices/        # Redux slices
│       └── utils/         # Utility functions
└── uploads/               # File uploads directory
```

## Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Asib-104/ownshop.git
   cd ownshop
   ```

2. **Install dependencies**
   ```bash
   # Install backend dependencies
   npm install
   
   # Install frontend dependencies
   cd frontend
   npm install
   ```

3. **Environment Variables**
   
   Create a `.env` file in the root directory and add the following:
   ```
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   PAYPAL_CLIENT_ID=your_paypal_client_id
   PAYPAL_APP_SECRET=your_paypal_secret
   PAYPAL_API_URL=https://api-m.sandbox.paypal.com
   ```

4. **Database Setup**
   
   Run the data seeder to populate the database:
   ```bash
   npm run data:import
   ```

5. **Run the Application**
   
   ```bash
   # Run backend and frontend concurrently
   npm run dev
   
   # Or run separately:
   npm run server    # Backend only
   npm run client    # Frontend only
   ```

## Available Scripts

- `npm run server` - Run backend server only
- `npm run client` - Run frontend only
- `npm run dev` - Run both frontend and backend concurrently
- `npm run data:import` - Import sample data to database
- `npm run data:destroy` - Delete all data from database

## API Endpoints

### Products
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Create product (Admin)
- `PUT /api/products/:id` - Update product (Admin)
- `DELETE /api/products/:id` - Delete product (Admin)

### Users
- `POST /api/users/register` - Register user
- `POST /api/users/login` - Login user
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

### Orders
- `POST /api/orders` - Create order
- `GET /api/orders/:id` - Get order by ID
- `PUT /api/orders/:id/pay` - Update order to paid
- `GET /api/orders/myorders` - Get logged in user orders

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.

## Author

[Asib-104](https://github.com/Asib-104)
