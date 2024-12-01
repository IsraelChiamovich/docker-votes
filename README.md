# Fullstack Dockerized Application

This project is a fullstack application with React as the frontend, Node.js as the backend, and MongoDB as the database. The application is fully containerized using Docker and Docker Compose.

---

## Prerequisites
- Install Docker: [Docker Installation Guide](https://docs.docker.com/get-docker/)
- Install Docker Compose: Included with Docker Desktop.

---

## Setup and Deployment

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Build Docker Images
Run the following command to build the images for the application:

```bash
docker-compose build
```

### 3. Create Secrets
Ensure sensitive information is securely stored. Create the following secret files in the project directory:

- `db_password.txt`: Contains the MongoDB password.
- `jwt_secret.txt`: Contains the JWT secret.

Example:

```bash
echo "your-db-password" > db_password.txt
echo "your-jwt-secret" > jwt_secret.txt
```

### 4. Run the Application
Start the containers using Docker Compose:

```bash
docker-compose up -d
```

### Application Access
- **Frontend**: [http://localhost:8080](http://localhost:8080)
- **Backend**: [http://localhost:3030](http://localhost:3030)

### Docker Hub Images
- **Frontend**: [docker.io/israelchaimovich/vote-client](https://hub.docker.com/r/israelchaimovich/vote-client)
- **Backend**: [docker.io/israelchaimovich/vote-server](https://hub.docker.com/r/israelchaimovich/vote-server)

---

## Environment Variables
These environment variables need to be set for the application to work:

- `PORT`: The port number for the backend service.
- `DB_URI`: MongoDB connection string.
- `JWT_SECRET`: Secret key for JSON Web Tokens.

---

## Project Structure
- **client**: Contains the React frontend application.
- **server**: Contains the Node.js backend.
- **docker-compose.yml**: Defines the services and their configurations.

---

## Useful Commands

### View Logs
```bash
docker-compose logs
```

### Stop the Application
```bash
docker-compose down
```

---

## Notes
- Ensure that `db_password.txt` and `jwt_secret.txt` are not included in your version control system.
- All services are connected via a Docker bridge network, allowing seamless communication.

---

## Troubleshooting

### Application not starting?
- Check the logs: `docker-compose logs`
- Ensure Docker is running properly.

### Database connection issues?
- Verify `DB_URI` is correctly set.

### Frontend not loading?
- Confirm that the backend is running and accessible on `localhost:3030`.

---

## Contact
If you encounter any issues or have questions, feel free to reach out!
