# Speedo Transfer - Transfer Service API

## Description
**Speedo Transfer** is a Java Spring Boot-based backend service that facilitates money transfers between accounts. This project provides a robust API for performing transfer operations, managing customer accounts, favorites, and transaction history. The API adheres to OpenAPI 3.0 standards, and full documentation is accessible via Swagger UI.

## Features
- **Account Transfers**: Transfer money between accounts using account numbers.
- **Favorites Management**: Add or remove favorite accounts for quick access.
- **Customer Management**: CRUD operations for customers, including login, registration, and updates.
- **Transaction History**: Retrieve the transaction history of the logged-in user.
- **Authentication**: JWT-based login and logout functionality.
- **Swagger UI**: Explore and test API endpoints through an interactive Swagger interface.

---

## API Endpoints

### Transfer API
- **POST** `/api/transfer/account`: Transfer money by account number.

### Favorites API
- **GET** `/api/favourites`: Get all favorite accounts for the logged-in user.
- **POST** `/api/favourites`: Add an account to favorites.
- **DELETE** `/api/favourites/{id}`: Delete a favorite account by ID.

### Customer API
- **GET** `/api/customer`: Get all customers.
- **GET** `/api/customer/{customerId}`: Get customer details by ID.
- **GET** `/api/customer/email/{email}`: Get customer by email.
- **PUT** `/api/customer/update`: Update customer details.
- **DELETE** `/api/customer/me`: Delete the current logged-in customer.

### Authentication API
- **POST** `/api/auth/register`: Register a new customer account.
- **POST** `/api/auth/login`: Login and generate a JWT.
- **POST** `/api/auth/logout`: Logout and invalidate the JWT.
- **POST** `/api/auth/updatePassword`: Allows authenticated users to update their password.

### Transaction API
- **GET** `/api/transactions/history`: Get the transaction history for the logged-in customer.

### Account API
- **POST** `/api/account`: Create a new sub-account for the customer.
- **GET** `/api/account/{accountNumber}/balance`: Retrieve the account balance.


---

## Swagger UI
To explore and interact with the API on your localhost, use the Swagger UI available at:
(http://localhost:8081/swagger-ui/)       
check the Doc 
https://drive.google.com/file/d/1ShyGqDDElrBCSEStmYf-AGVw6ftSIm9g/view?usp=sharing


---

## Requirements
- Java 11+
- Spring Boot
- Maven

---

## Running the Project

1. **Clone the repository**:
   ```bash
   git clone https://github.com/MoneyTransfer__BanqueMisr/speedo-transfer.git



## Deployment on Render
This application is deployed on Render. You can access it at the following link:

* **Website**: https://banquemisr-transfer-service.onrender.com/


## How to Test the API via Deployment Link

You can use the deployed link to directly test the API endpoints. Here are some examples:

### Login:

- **URL**: `https://banquemisr-transfer-service.onrender.com/api/auth/login`
  
  **Request Body**:
  ```json
  {
    "email": "user@example.com",
    "password": "yourPassword"
  }

### Transfer Money:

- **URL**: `https://banquemisr-transfer-service.onrender.com/api/transfer/account`

  **Request Body**:
  ```json
  {
    "fromAccount": "123456789",
    "toAccount": "987654321",
    "amount": 100.00
  }

   
