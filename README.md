
# E-Commerce with Integrated Payment Services

This project is a Node.js-based E-Commerce platform that integrates payment services using PayPal and offers user authentication, product browsing, shopping cart management, and order tracking features. The project leverages MongoDB as the database and integrates with Cloudinary for image management.

## Features

- User authentication with hashed passwords (bcryptjs)
- Product browsing and filtering
- Shopping cart functionality
- Secure payment processing with PayPal
- Order tracking and management
- Image handling via Cloudinary
- Cross-Origin Resource Sharing (CORS) enabled

## Tech Stack

### Backend:
- **Node.js**: JavaScript runtime for building the backend.
- **Express.js**: Web framework for Node.js.
- **MongoDB**: Database for storing user, product, and order data.
- **Mongoose**: MongoDB object modeling for Node.js.
- **JWT (jsonwebtoken)**: For secure user authentication and authorization.
- **PayPal REST SDK**: For handling payment processing.
- **Cloudinary**: For image upload and storage.
- **Multer**: For handling file uploads.

## Setup Instructions

### Prerequisites

Ensure you have the following installed on your machine:

- **Node.js** (v14 or higher)
- **MongoDB** (for database storage)
- **PayPal Developer Account** (for payment integration)
- **Cloudinary Account** (for image storage)

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yashwanth1011/E-Commerce-with-Integrated-Payment-Services.git
   cd E-Commerce-with-Integrated-Payment-Services
   ```

2. **Install backend dependencies:**
   Navigate to the backend directory:
   ```bash
   cd server
   npm install
   ```

3. **Configure the environment variables:**
   Create a `.env` file in the root of the `server` directory and add the following variables:
   ```bash
   MONGO_URI=your_mongodb_connection_string
   PAYPAL_CLIENT_ID=your_paypal_client_id
   PAYPAL_CLIENT_SECRET=your_paypal_client_secret
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   JWT_SECRET=your_jwt_secret
   ```

4. **Run the backend server:**
   To run the server in development mode using nodemon:
   ```bash
   npm run dev
   ```

   Or to run the server normally:
   ```bash
   npm start
   ```

## API Endpoints

### Authentication:
- **POST** `/api/auth/register`: Register a new user.
- **POST** `/api/auth/login`: Log in a user and get a JWT token.

### Products:
- **GET** `/api/products`: Get a list of all products.
- **GET** `/api/products/:id`: Get details for a specific product.

### Cart:
- **POST** `/api/cart/add`: Add a product to the user's shopping cart.
- **DELETE** `/api/cart/remove/:id`: Remove a product from the cart.

### Orders:
- **POST** `/api/orders/create`: Create an order for the products in the cart.
- **GET** `/api/orders/:id`: Get details for a specific order.

## Environment Variables

You will need to set the following environment variables in your `.env` file:

- `MONGO_URI`: MongoDB connection string for your database.
- `PAYPAL_CLIENT_ID`: PayPal API client ID for payment processing.
- `PAYPAL_CLIENT_SECRET`: PayPal API client secret for payment processing.
- `CLOUDINARY_CLOUD_NAME`: Cloudinary cloud name for image handling.
- `CLOUDINARY_API_KEY`: Cloudinary API key.
- `CLOUDINARY_API_SECRET`: Cloudinary API secret.
- `JWT_SECRET`: Secret for signing JWT tokens.
