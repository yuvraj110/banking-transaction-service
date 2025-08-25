# Transaction Service

## Description
Handles deposits, withdrawals, and transfers between accounts.

## Technologies
- Java 17
- Spring Boot
- Spring Data JPA
- PostgreSQL
- RabbitMQ (optional for async notifications)
- Maven

## Features
- Deposit funds
- Withdraw funds
- Transfer funds between accounts
- Fetch transaction history
- Event publishing for notifications

## Endpoints
- `POST /transactions/deposit` → Deposit to account
- `POST /transactions/withdraw` → Withdraw from account
- `POST /transactions/transfer` → Transfer between accounts
- `GET /transactions/{accountId}` → Transaction history

## Database Schema
- **transactions**
    - id: UUID
    - accountId: UUID
    - type: ENUM (DEPOSIT, WITHDRAW, TRANSFER)
    - amount: Decimal
    - timestamp: DateTime
