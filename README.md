## 💻 CityPortal Server (Backend)

## 🚀 Overview

This repository contains the server-side code for the **CityPortal** application. The server is built to handle all API requests, manage data persistence, enforce application rules (like user roles and issue limits), and integrate external services for authentication and payment.

## 🔗 Live Application URL

You can access the live version of the application here:

[https://public-reporting-system-server.vercel.app/](https://public-reporting-system-server.vercel.app/)

### Architecture

The backend follows a standard **Monolithic Architecture** using the **MEEN** stack (MongoDB, Express.js, environment variables, Node.js).

## 🛠️ Technology Stack

| Component          | Technology         | Role                                                           |
| :----------------- | :----------------- | :------------------------------------------------------------- |
| **Runtime**        | Node.js            | Executes JavaScript server-side.                               |
| **Framework**      | Express.js         | Provides robust routing and middleware capabilities.           |
| **Database**       | MongoDB            | Stores all persistent data (issues, users, staff, etc.).       |
| **Authentication** | Firebase Admin SDK | Handles secure user verification and authorization using JWTs. |
| **Payments**       | Stripe             | Processes subscriptions for premium citizen features.          |

## ✨ Core Responsibilities

The CityPortal Server is the engine for the application, responsible for:

- **API Management:** Defining and managing all RESTful endpoints for the client-side.
- **Data Persistence:** Connecting to and managing data within the MongoDB database.
- **Authentication & Authorization:**
  - Verifying the identity of every request using Firebase-issued JWTs.
  - Implementing **Role-Based Access Control (RBAC)** to ensure `Staff`, `Citizen`, and `Admin` users only access authorized routes.
- **Business Logic:** Enforcing application rules, such as limiting standard `Citizen` accounts to submitting **3 issues**.
- **Payment Processing:** Interacting with Stripe to manage user subscriptions.

## 📦 Dependencies

The following npm packages are essential for the server's operation:

| Package Name       | Category       | Functionality                                                                     |
| :----------------- | :------------- | :-------------------------------------------------------------------------------- |
| **express**        | Core Framework | Minimal and flexible Node.js web application framework.                           |
| **mongodb**        | Database       | Official driver for interacting with the MongoDB instance.                        |
| **firebase-admin** | Security/Auth  | Manages user verification and provides admin access to Firebase services.         |
| **stripe**         | Payments       | Facilitates secure creation and management of payments and subscriptions.         |
| **cors**           | Middleware     | Enables Cross-Origin Resource Sharing for secure communication with the frontend. |
| **dotenv**         | Utilities      | Loads sensitive environment variables from a `.env` file.                         |
