# ecommerce-app
```markdown
# E-Commerce Platform (React + Spring Boot + PostgreSQL)

## Overview
This project is a basic e-commerce platform that allows managing products, users, and orders. It is built using:
- **Frontend**: React with Vite for fast development and responsive UI.
- **Backend**: Spring Boot for RESTful APIs and business logic.
- **Database**: PostgreSQL to store and manage data.

The platform supports basic e-commerce functionalities such as product listing, user authentication, and order management. This README provides setup instructions and explains how to run the project locally.

---

## Features
1. User authentication and authorization (e.g., login, signup).
2. Product management (CRUD operations).
3. Order management (place and view orders).
4. Responsive user interface built with React.
5. RESTful APIs to handle backend logic.

---

## Prerequisites
Ensure you have the following installed:
- **Node.js** (for React frontend)
- **Java (JDK 17 or higher)**
- **PostgreSQL** (database)
- **Maven** (for Spring Boot backend)
- **Git** (to clone the repository)

---

## Project Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-repository/ecommerce.git
cd ecommerce
```

---

### 2. Backend Setup (Spring Boot)

1. **Navigate to the backend directory:**
   ```bash
   cd backend
   ```

2. **Configure PostgreSQL:**
   - Create a PostgreSQL database:
     ```sql
     CREATE DATABASE ecommerce_db;
     ```
   - Open `application.properties` or `application.yml` in the `src/main/resources/` folder and update the following:
     ```properties
     spring.datasource.url=jdbc:postgresql://localhost:5432/ecommerce_db
     spring.datasource.username=your_postgres_username
     spring.datasource.password=your_postgres_password
     spring.jpa.hibernate.ddl-auto=update
     spring.jpa.show-sql=true
     ```

3. **Build and run the backend:**
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```
   The backend server will run on `http://localhost:8080`.

---

### 3. Frontend Setup (React + Vite)

1. **Navigate to the frontend directory:**
   ```bash
   cd ../frontend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   ```
   The frontend will run on `http://localhost:5173`.

4. **API Integration:**
   - Open the `src/config/apiConfig.js` file and ensure the API URL points to the backend:
     ```javascript
     const API_BASE_URL = 'http://localhost:8080/api';
     export default API_BASE_URL;
     ```

---

## How to Run the Project

1. **Start PostgreSQL:**
   - Ensure your database server is running.

2. **Run the Backend:**
   - Navigate to the `backend` folder and start the Spring Boot application.

3. **Run the Frontend:**
   - Navigate to the `frontend` folder and start the React app.

4. Open your browser and visit:
   - Frontend: `http://localhost:5173`
   - Backend API: `http://localhost:8080`

---

## Folder Structure
```
ecommerce/
├── backend/        # Spring Boot backend
│   ├── src/main/   # Main Java source files
│   ├── pom.xml     # Maven configuration
│   └── ...
├── frontend/       # React frontend
│   ├── src/        # React source files
│   ├── vite.config.js
│   └── package.json
└── README.md       # Project documentation
```

---

## API Endpoints
### Product APIs
- **GET /api/products**: Fetch all products
- **POST /api/products**: Add a new product
- **PUT /api/products/{id}**: Update a product
- **DELETE /api/products/{id}**: Delete a product

### User APIs
- **POST /api/auth/signup**: Register a new user
- **POST /api/auth/login**: Authenticate a user

### Order APIs
- **POST /api/orders**: Place a new order
- **GET /api/orders/{userId}**: Fetch orders for a user

---

## Technologies Used
- **Frontend**: React, Vite, JavaScript, CSS
- **Backend**: Spring Boot, REST API
- **Database**: PostgreSQL
- **Tools**: Maven, npm, Git

---

## Future Enhancements
1. Add payment gateway integration.
2. Implement advanced user roles (admin, user, etc.).
3. Add a search and filtering feature for products.
4. Create a mobile-friendly version of the app.

---

## Troubleshooting
- **Frontend not connecting to backend:** Ensure the backend server is running on `http://localhost:8080`.
- **Database connection issues:** Verify the `application.properties` file and ensure PostgreSQL is running.
- **CORS issues:** Ensure CORS is configured correctly in the backend.

---

## Contributors
(https://github.com/christo975)

---

## License


