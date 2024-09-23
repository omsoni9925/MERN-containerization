# MERN App Containerization with Docker Compose

This project containerizes a MERN (MongoDB, Express, React, Node.js) stack using Docker Compose, with custom networks and persistent MongoDB data.

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Docker Compose Configuration](#docker-compose-configuration)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project demonstrates how to containerize a MERN application using Docker Compose, utilizing a custom bridge network (`mern_network`) to allow seamless communication between the services and persistent storage for MongoDB.

### Services

1. **MongoDB** - NoSQL database service, data is persisted locally using Docker volumes.
2. **Backend (Express.js)** - Node.js backend that connects to MongoDB and serves API endpoints.
3. **Frontend (React.js)** - A React app that consumes the backend APIs.

## Technologies Used

- **MongoDB** - NoSQL database.
- **Express.js (Node.js)** - Backend framework.
- **React.js** - Frontend framework.
- **Docker** - Containerization platform.
- **Docker Compose** - Tool for defining and running multi-container Docker applications.

## Setup Instructions

### Prerequisites

- Install Docker and Docker Compose on your system.

### Clone the Repository

```bash
git clone https://github.com/omsoni9925/MERN-containerization.git
cd MERN-containerization
