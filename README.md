# Project Setup Guide

This guide provides step-by-step instructions to set up and run the React (frontend) and Laravel (backend) applications using XAMPP.

---

## Prerequisites

Before proceeding, ensure you have the following installed:

1. **XAMPP** (with PHP 8.1 or higher)  
   [Download and install XAMPP](https://www.apachefriends.org/index.html)

2. **Node.js** (v16 or higher)  
   [Download and install Node.js](https://nodejs.org/)

3. **npm or yarn**  
   `npm` comes with Node.js. To install `yarn`, run:

   ```bash
   npm install -g yarn
   ```

4. **Composer** (latest version)  
   [Download and install Composer](https://getcomposer.org/)

---

## 1. React Frontend Setup

### Steps to Run the React App:

1. **Extract the ZIP File**  
   Extract the React app's ZIP file into a directory of your choice.

2. **Navigate to the Project Directory**

   ```bash
   cd path/to/react-app
   ```

3. **Install Dependencies**  
   Run the following command to install the required packages:

   ```bash
   npm install
   ```

   _Or, if using `yarn`:_

   ```bash
   yarn install
   ```

4. **Start the Development Server**  
   Run the following command:

   ```bash
   npm start
   ```

   _Or, if using `yarn`:_

   ```bash
   yarn start
   ```

5. **Access the Application**  
   Open your web browser and navigate to:
   ```
   http://localhost:3000
   ```

---

## 2. Laravel Backend Setup (Using XAMPP)

### Steps to Run the Laravel App:

1. **Extract the ZIP File**  
   Extract the Laravel app's ZIP file into a directory under the XAMPP `htdocs` folder:

   ```
   C:/xampp/htdocs/project-management-api-laravel
   ```

2. **Start XAMPP Services**  
   Open the XAMPP Control Panel and start the **Apache** and **MySQL** services.

3. **Create a Database**

   - Open **phpMyAdmin** in your browser:
     ```
     http://localhost/phpmyadmin
     ```
   - Create a new database (e.g., `project_management`).

4. **Navigate to the Laravel Project Directory**

   ```bash
   cd C:/xampp/htdocs/project-management-api-laravel
   ```

5. **Install Dependencies**  
   Run the following command to install PHP packages:

   ```bash
   composer install
   ```

6. **Configure the Environment File**

   - Create a copy of `.env.example` and rename it to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Open `.env` and update the database configuration to match your XAMPP MySQL setup:
     ```env
     DB_CONNECTION=mysql
     DB_HOST=127.0.0.1
     DB_PORT=3306
     DB_DATABASE=project_management
     DB_USERNAME=root
     DB_PASSWORD=
     ```

7. **Generate the Application Key**

   ```bash
   php artisan key:generate
   ```

8. **Run Database Migrations**  
   Run the migrations to set up the database schema:

   ```bash
   php artisan migrate
   ```

9. **Start the Laravel Development Server**  
   Use the following command:
   ```bash
   php artisan serve
   ```
   By default, this will start the server at:
   ```
   http://127.0.0.1:8000
   ```
