
# MERN App Containerization with Docker Compose

This project demonstrates how to containerize a full-stack MERN (MongoDB, Express, React, Node.js) application using Docker Compose. It includes a custom Docker network for internal communication and persistent MongoDB data storage using volumes.



## Installation

### Prerequisites
- Docker
- Docker Compose

### Clone the Repository
```bash
git clone https://github.com/omsoni9925/MERN-containerization.git
cd MERN-containerization
```

### Setup Environment Variables
- Create a .env file in the root directory with the following content:
```bash
MONGO_URI=mongodb://mongo:27017/mydatabase
REACT_APP_API_URL=http://backend:5050
```

### Build and Run the Conatiners
- To build and start the containers, run the following command:
```bash
docker-compose up -b
```
### Access the Application
- Frontend (React): http://localhost:5173
- Backend (Express): http://localhost:5050
- MongoDB: Accessible internally at mongodb://mongo:27017 and externally at localhost:27017.
## Usage

- The application consists of three services:
1. **Frontend (React)**: A React app that interacts with the backend API.
2. **Backend (Express)**: A Node.js Express server that connects to MongoDB and provides API endpoints.
3. **MongoDB**: NoSQL database for storing application data.

### Docker Compose Configuration
Here's an overview of the services defined in the `docker-compose.yml` file:

```yaml
version: '3'

services:
  backend:
    build: ./mern/backend
    ports:
      - "5050:5050" 
    networks:
      - mern_network
    environment:
      MONGO_URI: mongodb://mongo:27017/mydatabase  
    depends_on:
      - mongodb

  frontend:
    build: ./mern/frontend
    ports:
      - "5173:5173"  
    networks:
      - mern_network
    environment:
      REACT_APP_API_URL: http://backend:5050 

  mongodb:
    image: mongo:latest  
    ports:
      - "27017:27017"  
    networks:
      - mern_network
    volumes:
      - mongo-data:/data/db  

networks:
  mern_network:
    driver: bridge 

volumes:
  mongo-data:
    driver: local
```

## Docker Commands

- View running containers:
``` bash
docker ps 
```

- Stop the containers:
``` bash
docker-compose down
```

- Remove containers and volumes:
``` bash
docker-compose down --volumes
```


## Contributing

Feel free to fork this repository and submit pull requests. Contributions are welcome!



## Acknowledgements

Special thanks to [iam-veeramalla's MERN Docker Compose repository](https://github.com/iam-veeramalla/MERN-docker-compose) for inspiration and guidance in setting up this project.
