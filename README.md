# Detoxifi Project

The **Detoxifi** project is a full-stack application consisting of a **frontend** and **backend**. The **frontend** is built with **React** and **Vite**, while the **backend** is powered by **Node.js** with **Express** and **MongoDB**. This system includes features like user authentication, payment integration via **PayPal** and **Stripe**, and email notifications using **Nodemailer**.

## Project Structure

This repository consists of the following projects:

1. **detoxifi-frontend**: A React application that serves as the user-facing frontend.
2. **backend**: A Node.js/Express backend that handles the server-side logic and database interactions.

---

## Prerequisites

Before running the application, ensure you have the following installed:

* **Node.js** (v16 or higher)
* **npm** (Node Package Manager, comes with Node.js)
* **git** (to clone the repository)
* **Yarn** (optional, but recommended for some projects)

---

## Getting Started

Follow these steps to set up the **Detoxifi** project on your local machine.

### 1. Clone the Repository

Clone the repository using the following command:

```bash
git clone <repository-url>
cd detoxifi
```

### 2. Install Dependencies

Each project has its own set of dependencies. Navigate to each project directory and install the required dependencies.

#### **Frontend Project (detoxifi-frontend)**

Navigate to the `detoxifi-frontend` directory and install the dependencies:

```bash
cd detoxifi-frontend
npm install
```

#### **Backend Project**

Navigate to the `backend` directory and install the dependencies:

```bash
cd backend
npm install
```

### 3. Set Up Environment Variables

Some of the services require environment variables for proper configuration. Please ensure that you create a `.env` file in both the `detoxifi-frontend` and `backend` directories and set the necessary values.

#### Example `.env` for **detoxifi-frontend**:

```env
VITE_API_URL=http://localhost:5000
```

#### Example `.env` for **backend**:

```env
MONGODB_URI=mongodb://localhost:27017/detoxifi
JWT_SECRET=your_jwt_secret
PAYPAL_CLIENT_ID=your_paypal_client_id
STRIPE_SECRET_KEY=your_stripe_secret_key
MAIL_HOST=smtp.your-email-provider.com
MAIL_PORT=587
MAIL_USER=your-email@example.com
MAIL_PASS=your-email-password
```

---

## Running the Projects

After installing the dependencies and setting up the environment variables, you can run the projects individually.

### 1. Run the Frontend

For the **frontend** project, navigate to the `detoxifi-frontend` directory and start the development server:

```bash
cd detoxifi-frontend
npm run dev
```

The frontend will be available at `http://localhost:3000`.

### 2. Run the Backend

For the **backend** project, navigate to the `backend` directory and start the server:

```bash
cd backend
npm run server
```

The backend will be available at `http://localhost:5000`.

---

## Running Tests

### 1. Frontend Tests (React)

To run the frontend tests, use the following command:

```bash
cd detoxifi-frontend
npm run test
```

### 2. Backend Tests (Node.js/Express)

For the backend, if you have any unit tests (e.g., using **Jest**), you can run them using:

```bash
cd backend
npm run test
```

---

## Building the Projects

Once you're done with development and want to create production-ready builds, you can build each project with the following commands.

### 1. Build the Frontend

For the frontend, run the following:

```bash
cd detoxifi-frontend
npm run build
```

This will create a production build of the frontend in the `dist/` directory.

### 2. Build the Backend

For the backend, the project is already set up to run in a production environment using Node.js. You can simply run it with:

```bash
cd backend
npm run start
```

---

## Payment Integrations

The backend is integrated with **PayPal** and **Stripe** for handling payments.

* **PayPal**: The PayPal SDK is used to process payments, and you will need to set your **PayPal Client ID** in the `.env` file.
* **Stripe**: The Stripe API is used for payment processing. Set your **Stripe Secret Key** in the `.env` file.

### Testing Payments

You can test PayPal and Stripe payments in development mode by using the sandbox/test keys provided by PayPal and Stripe.

---

## Email Notifications

The backend uses **Nodemailer** to send email notifications. Set your email provider’s SMTP details in the `.env` file to enable email functionality for user registration, password resets, or payment confirmations.

---

## Technologies Used

* **Frontend**:

  * React
  * Vite
  * TailwindCSS
  * Axios
  * React Router
  * React Toastify
  * Swiper

* **Backend**:

  * Node.js
  * Express
  * MongoDB (Mongoose)
  * JWT (JSON Web Token)
  * PayPal SDK
  * Stripe API
  * Nodemailer

* **Development Tools**:

  * ESLint
  * Prettier
  * Nodemon
  * TailwindCSS (for styling)
