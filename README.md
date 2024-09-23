# MERN Containerization with Docker Compose

This project demonstrates how to containerize a full-stack MERN (MongoDB, Express, React, Node.js) application using Docker Compose. The application is separated into multiple containers for each service: MongoDB, Express (Node.js), and React.

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Docker Compose Configuration](#docker-compose-configuration)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This is a simple MERN app that runs on Docker containers using Docker Compose. The goal is to showcase how to containerize each layer of the MERN stack and manage dependencies and networking using Docker Compose.

### Components

1. **MongoDB** - The database.
2. **Express.js (Node.js)** - Backend service.
3. **React.js** - Frontend service.

## Technologies Used

- **MongoDB** - NoSQL database for data storage.
- **Express.js** - Backend framework for building APIs.
- **React.js** - Frontend framework for building the user interface.
- **Node.js** - Server-side JavaScript runtime.
- **Docker** - For containerization.
- **Docker Compose** - For multi-container orchestration.

## Setup Instructions

### Prerequisites

- Ensure you have Docker and Docker Compose installed on your system.

### Clone the Repository

```bash
git clone https://github.com/omsoni9925/MERN-containerization.git
cd MERN-containerization
