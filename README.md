


## Introduction
This project is a **Laravel React Starter Kit** that provides a foundation for building web applications with a React frontend and Laravel backend. It includes user authentication managed by **Laravel Sanctum** for secure stateful sessions. This guide outlines how to set up and run the project locally.

## Prerequisites
Ensure you have the following software installed on your system:
- **Node.js** (v14.x or higher)
- **npm** or **yarn**
- **PHP** (if using Laravel as the backend)
- **Composer** (for PHP dependencies)
- **Git**
- **Database Server** (MySQL, PostgreSQL, or any preferred database)

## Cloning the Project
1. Open your terminal and navigate to the directory where you want to clone the project.
2. Run the following command to clone the repository:
   ```bash
   git clone https://github.com/yourusername/yourproject.git
   cd yourproject
   ```

## Backend Setup
1. **Copy the environment variables file**:
   If you're using `bash`, run:
   ```bash
   cp .env.example .env
   ```
   Otherwise, manually copy `.env.example` to a new file named `.env`.

2. **Ensure the following values in your `.env` file**:
   ```env
   FRONTEND_URL=http://localhost:5173
   SANCTUM_STATEFUL_DOMAINS=localhost:5173
   SESSION_DOMAIN=localhost
   ```

3. **Install backend dependencies**:
   ```bash
   composer install
   ```

4. **Generate the application key** (Laravel specific):
   ```bash
   php artisan key:generate
   ```

## Frontend Setup
1. Navigate to the `client` directory:
   ```bash
   cd client
   ```

2. **Install the dependencies**:
   ```bash
   npm install
   ```
   

3. **Configure the frontend environment file**:
   Create a `.env` file in the `frontend` directory if it doesn't exist. You can base it on `.env.example` or manually set the following:
   ```env
   VITE_BACKEND_URL=http://localhost:8000
   ```

## Database Configuration
1. **Set up your database**:
   - Ensure your database server is running.
   - Create a new database (e.g., `my_project_db`).

2. **Configure database credentials** in the `.env` file:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=my_project_db
   DB_USERNAME=root
   DB_PASSWORD=yourpassword
   ```

3. **Run migrations** to set up the database schema:
   ```bash
   php artisan migrate
   ```

## Running the Project
1. **Start the backend server**:
   ```bash
   php artisan serve
   ```

2. **Start the frontend server**:
   Open a new terminal window and run:
   ```bash
   npm run dev
   ```
  

## Environment Variables
Ensure that the `.env` file in the backend root directory includes the following:
```env
FRONTEND_URL=http://localhost:5173
SANCTUM_STATEFUL_DOMAINS=localhost:5173
SESSION_DOMAIN=localhost
```


