# Money Tracker API

A RESTful API built with PHP Laravel that allows users to manage multiple wallets and track income and expense transactions.

## Features

- Create user accounts
- Create and manage multiple wallets per user
- Add income and expense transactions to wallets
- View user profile with all wallets and total balance
- View individual wallet with transaction history

## Requirements

- PHP >= 8.1
- Composer
- Laravel 10+
- MySQL or SQLite

## Setup Instructions

1. Clone the repository:
   git clone https://github.com/Veronicah-155/money-tracker-api.git
   cd money-tracker-api

2. Install dependencies:
   composer install

3. Copy the environment file and configure your database:
   cp .env.example .env

4. Generate the application key:
   php artisan key:generate

5. Run migrations:
   php artisan migrate

6. Start the development server:
   php artisan serve

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/users | Create a new user |
| GET | /api/users/{id} | Get user profile with wallets and total balance |
| POST | /api/wallets | Create a new wallet |
| GET | /api/wallets/{id} | Get wallet with transactions and balance |
| POST | /api/transactions | Add a transaction to a wallet |

## Transaction Types

- `income` — adds to wallet balance
- `expense` — subtracts from wallet balance
