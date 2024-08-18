# JWT Authentication and Authorization

## Overview

This project implements a secure authentication and authorization system using JSON Web Tokens (JWT). The system is designed to handle user login, registration, and secure access to protected resources in a web application. It is built using **Spring Boot** for the backend and integrates **JWT** for token-based security.

## Features

- **User Registration**: New users can register by providing their details such as username, password, and role.
- **User Login**: Registered users can log in using their credentials to receive a JWT.
- **JWT Token Generation**: Upon successful authentication, a JWT is generated and returned to the client. This token is used to authenticate subsequent requests.
- **Role-Based Authorization**: Access to specific endpoints is restricted based on user roles (e.g., Admin, User).
- **Stateless Session**: The application does not store user sessions on the server. Instead, the JWT is used to maintain user state across requests.
- **Secure Endpoints**: Sensitive endpoints are protected, requiring a valid JWT for access.
- **Logout**: Users can securely log out by invalidating their token.

## Technologies Used

- **Spring Boot**: A powerful, easy-to-use framework for building Java applications.
- **Spring Security**: A comprehensive security framework for Java applications, providing authentication, authorization, and other security features.
- **JWT (JSON Web Tokens)**: A compact, URL-safe means of representing claims to be transferred between two parties. Used for securely transmitting information between client and server.
- **Hibernate/JPA**: For interacting with the database and managing user entities.
- **PostgreSQL**: A robust, open-source relational database system used to store user data.

## Project Structure

The project follows a standard layered architecture:

- **Model**: Defines the application's data structure (e.g., User, Role).
- **Repository**: Handles data access logic, interacting with the database.
- **Service**: Contains business logic, such as handling user authentication and JWT token management.
- **Controller**: Manages HTTP requests and responses, exposing endpoints for user actions.
- **Security**: Configures Spring Security and JWT integration, managing authentication and authorization processes.

## API EndPoints 

- **POST**: /api/v1/auth/register: Register a new user.
- **POST**: /api/v1/auth/authenticate: Authenticate a user and receive a JWT.
- **GET**: /api/v1/demo-controller: Access a protected resource (requires JWT).

## Setup and Installation

To run this project locally, follow these steps:

### Clone the Repository

```bash
git clone https://github.com/AhmedMosad255/Jwt-Authentication-and-Authorisation.git
cd Jwt-Authentication-and-Authorisation
