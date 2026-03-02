# Univote Student Voting System

Welcome to **Univote**, a comprehensive university student voting system designed to streamline administrative tasks and enhance the voting experience. This guide will help you set up both the frontend and backend components of the project.

## Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Setup Instructions](#setup-instructions)
   - [Frontend](#frontend)
   - [Backend](#backend)
4. [Running the Project](#running-the-project)
   - [Frontend](#frontend-1)
   - [Backend](#backend-1)

---

## Introduction

Univote is built with a modern tech stack:
- **Frontend:** React with Vite
- **Backend:** Laravel (PHP >= 8.2)
- **Database:** PostgreSQL

This project enhances the student voting experience in university elections.

---

## Prerequisites

Ensure you have the following installed on your machine:

- **Node.js** (v18 or above)
- **npm** or **yarn** (for managing frontend packages)
- **PHP** (>= 8.2)
- **Composer** (for managing backend dependencies)
- **PostgreSQL** (running locally on port `5432`)

---

## Setup Instructions

### Clone the Repository

```bash
git clone https://github.com/S-Nathistan/Univote-system.git
cd Univote-system
```

---

### Frontend

```bash
cd univote_frontend
```

1. **Install Dependencies**

   ```bash
   npm install
   ```

2. **Configure Environment**

   Copy the `.env.example` file to `.env` and update if needed:

   ```bash
   cp .env.example .env
   ```

   Default values in `.env`:

   ```env
   VITE_BASE_URL=http://localhost:8000
   VITE_SECRET_KEY=your_secret_key
   ```

3. **Run the Development Server**

   ```bash
   npm run dev
   ```

   The frontend will be accessible at **http://localhost:5173**

---

### Backend

```bash
cd univote_backend
```

1. **Install Dependencies**

   ```bash
   composer install
   ```

2. **Configure Environment**

   Copy the `.env.example` file to `.env`:

   ```bash
   cp .env.example .env
   ```

   Update the following in `.env`:

   ```env
   APP_URL=http://localhost:8000

   DB_CONNECTION=pgsql
   DB_HOST=127.0.0.1
   DB_PORT=5432
   DB_DATABASE=univote
   DB_USERNAME=postgres
   DB_PASSWORD=your_password

   SANCTUM_STATEFUL_DOMAINS=localhost:5173
   SESSION_DOMAIN=localhost

   SECRET_KEY=your_secret_key
   ```

3. **Generate Application Key**

   ```bash
   php artisan key:generate
   ```

4. **Start PostgreSQL**

   Ensure PostgreSQL is running on port `5432` and the `univote` database exists.

5. **Run Migrations**

   ```bash
   php artisan migrate
   ```

6. **Run the Development Server**

   ```bash
   php artisan serve
   ```

   The backend will be accessible at **http://localhost:8000**

---

## Running The Project

> ⚠️ **Both frontend and backend must be running simultaneously for full functionality.**

### Frontend

```bash
cd univote_frontend
npm run dev
```

### Backend

```bash
cd univote_backend
php artisan serve
```

---

## Tech Stack

| Layer     | Technology         |
|-----------|--------------------|
| Frontend  | React + Vite       |
| Backend   | Laravel (PHP 8.2+) |
| Database  | PostgreSQL         |
| Auth      | Laravel Sanctum    |

---

GOOD LUCK! 🎉
