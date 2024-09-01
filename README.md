# Ethereum Event Listener with Redis Cache

## Table of Contents
- [Description](#description)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [How to Run](#how-to-run)
- [Contributions](#contributions)
- [License](#license)

## Description

This repository demonstrates how performance can be improved by using Redis as a cache to reduce database queries. The project is developed in Go and is designed to listen to specific events generated by a smart contract on the Ethereum network. The application checks if the wallets registered in our database are mentioned in any of these events. If a wallet is found, the corresponding log is stored.

## Features

- **Ethereum Event Monitoring**: Listens to and processes events from a smart contract on the Ethereum network.
- **Wallet Verification**: Automatically checks if the wallets registered in the database are mentioned in the events.
- **Redis Cache**: Utilizes Redis to store information temporarily, reducing the need for frequent database queries and improving overall performance.

## Technologies Used

- **Go**: Programming language used to develop the project.
- **Ethereum**: Blockchain network where the smart contract is executed.
- **Redis**: In-memory cache system to enhance query efficiency.
- **PostgreSQL/MySQL** (or the database you are using): Stores wallet information and event logs.

## How to Run

1. **Clone the Repository**
   ```sh
   git clone https://github.com/devworlds/eventlistener-redis-performance.git
   cd your-repository
2. **Install Dependencies**
    ```sh
    go mod tidy
3. **Configure Redis and the Database**
    - Ensure Redis is running locally or provide the Redis URL in the configuration file.
    - Set up the database credentials. 
4. **Run the Docker Compose**
    ```sh
    docker compose up
5. **Run the Application**
    ```sh
    go run main.go