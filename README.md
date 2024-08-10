# Notification System

## Overview

The **Notification System** is a web-based application designed to send notifications to users based on their subscribed categories and preferred channels (SMS, Email, Push Notifications). The system is composed of two main components:

- **Backend**: Built with NestJS, it handles the business logic, manages user subscriptions, and sends notifications.
- **Frontend**: Developed with Next.js, it provides a user interface for submitting notifications and viewing logs.

This repository serves as the parent repository that organizes the project structure using Git submodules. It includes both the backend and frontend as well as the Docker Compose configuration to orchestrate the entire system.

## Project Structure

- **frontend/**: Contains the Next.js project for the frontend.
- **backend/**: Contains the NestJS project for the backend.
- **docker-compose.yml**: Configuration file to run the frontend, backend, and database services using Docker.

## Technologies Used

### Backend

- **NestJS**: A progressive Node.js framework for building efficient and scalable server-side applications.
- **TypeORM**: An ORM for TypeScript and JavaScript that can run on various databases such as PostgreSQL.
- **PostgreSQL**: A powerful, open-source object-relational database system.
- **Docker**: To containerize the backend service.

### Frontend

- **Next.js**: A React framework with hybrid static & server rendering, and route pre-fetching for building highly optimized web applications.
- **TypeScript**: A strongly typed programming language that builds on JavaScript, giving you better tooling at any scale.
- **Axios**: A promise-based HTTP client for the browser and Node.js.
- **Docker**: To containerize the frontend service.

### Infrastructure

- **Docker Compose**: A tool for defining and running multi-container Docker applications. It simplifies the setup of the development environment by managing the backend, frontend, and database services.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Docker**: To run the application containers.
- **Git**: To clone the repository and manage submodules.

### Cloning the Repository

To clone this repository and initialize the submodules (frontend and backend), run:

```bash
git clone --recurse-submodules https://github.com/cvelazqueze/notification-system.git
cd notification-system
```
If you already cloned the repository without initializing submodules, you can initialize and update them with:

```bash
git submodule update --init --recursive
```
Running the Application
The application can be started using Docker Compose. This will spin up the backend, frontend, and PostgreSQL database services.

```bash
docker-compose up --build
```
- The **frontend** will be accessible at http://localhost:3000.
- The **backend API** will be accessible at http://localhost:3001.
- The **PostgreSQL** database will run in the background, accessible within the Docker network.

### Accessing the Application
Open your browser and go to http://localhost:3000.
Use the UI to send notifications and view the log of sent notifications.

### Project Status
The current implementation is fully functional with the ability to send notifications to users based on their subscribed categories and preferred channels. Further enhancements and features can be added in future iterations.

### Contributing
Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new feature branch: git checkout -b feature-name.
3. Commit your changes: git commit -m 'Add some feature'.
4. Push to the branch: git push origin feature-name.
4. Open a pull request.
