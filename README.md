# E-commerce Billing System

A full-stack e-commerce billing system built with Spring Boot, React, and MySQL. This project demonstrates modern enterprise application development with RESTful APIs, JWT authentication, and role-based access control.

## 🚀 Features

### Backend (Spring Boot)
- **Product Management**: CRUD operations for products with categories
- **Shopping Cart**: Add/remove items, update quantities
- **Order Processing**: Complete checkout flow with order history
- **User Authentication**: JWT-based authentication and authorization
- **Role-Based Access Control**: Admin and Customer roles with different permissions
- **RESTful APIs**: Well-structured REST endpoints
- **Exception Handling**: Global exception handling with custom error responses
- **Input Validation**: Request validation using Bean Validation

### Frontend (React)
- **Modern UI**: Responsive design with Material-UI/Bootstrap
- **Product Catalog**: Browse and search products
- **Shopping Cart**: Real-time cart updates
- **User Dashboard**: Order history and profile management
- **Admin Panel**: Product and order management
- **Protected Routes**: Route guards based on authentication

### Database (MySQL)
- **Normalized Schema**: Efficient database design
- **Relationships**: One-to-many and many-to-many relationships
- **Indexes**: Optimized queries with proper indexing

## 🛠️ Tech Stack

### Backend
- **Java 17+**
- **Spring Boot 3.x**
  - Spring Web
  - Spring Data JPA
  - Spring Security
  - Spring Validation
- **MySQL 8.0+**
- **Maven**
- **JWT (JSON Web Tokens)**
- **Lombok**

### Frontend
- **React 18+**
- **React Router** for navigation
- **Axios** for HTTP requests
- **Material-UI / Bootstrap** for styling
- **Context API / Redux** for state management

## 📋 Prerequisites

- JDK 17 or higher
- Node.js 16+ and npm
- MySQL 8.0+
- Maven 3.6+

## ⚙️ Installation & Setup

### Backend Setup

1. Clone the repository
```bash
git clone https://github.com/akhilgaddam5/ecommerce-billing-system.git
cd ecommerce-billing-system/backend
```

2. Configure MySQL database
```sql
CREATE DATABASE ecommerce_db;
```

3. Update `application.properties`
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
spring.datasource.username=your_username
spring.datasource.password=your_password
jwt.secret=your_secret_key
```

4. Build and run
```bash
mvn clean install
mvn spring-boot:run
```

Backend will start on `http://localhost:8080`

### Frontend Setup

1. Navigate to frontend directory
```bash
cd ../frontend
```

2. Install dependencies
```bash
npm install
```

3. Update API endpoint in `.env`
```
REACT_APP_API_URL=http://localhost:8080/api
```

4. Start the development server
```bash
npm start
```

Frontend will start on `http://localhost:3000`

## 📊 Database Schema

### Key Tables
- **users**: User authentication and profile data
- **roles**: User roles (ADMIN, CUSTOMER)
- **products**: Product catalog
- **categories**: Product categories
- **orders**: Order information
- **order_items**: Items in each order
- **cart_items**: Shopping cart entries

## 🔐 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Products
- `GET /api/products` - Get all products
- `GET /api/products/{id}` - Get product by ID
- `POST /api/products` - Create product (Admin only)
- `PUT /api/products/{id}` - Update product (Admin only)
- `DELETE /api/products/{id}` - Delete product (Admin only)

### Cart
- `GET /api/cart` - Get user's cart
- `POST /api/cart/add` - Add item to cart
- `PUT /api/cart/update` - Update cart item
- `DELETE /api/cart/{id}` - Remove item from cart

### Orders
- `GET /api/orders` - Get user's orders
- `POST /api/orders/checkout` - Complete checkout
- `GET /api/orders/{id}` - Get order details

## 🧪 Testing

### Backend Tests
```bash
mvn test
```

### Frontend Tests
```bash
npm test
```

## 🚀 Deployment

### Backend Deployment
- Package as JAR: `mvn clean package`
- Deploy to AWS/Azure/Heroku or use Docker

### Frontend Deployment
- Build for production: `npm run build`
- Deploy to Netlify/Vercel or serve with Nginx

## 🤝 Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Akhil Gaddam**
- GitHub: [@akhilgaddam5](https://github.com/akhilgaddam5)
- LinkedIn: [Connect on LinkedIn](https://www.linkedin.com/in/yourprofile)

## 🙏 Acknowledgments

- Spring Boot Documentation
- React Documentation
- Material-UI Components
- JWT Authentication Best Practices
