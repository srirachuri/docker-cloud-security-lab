# 🔒 Day 16 – Secure Docker Compose with Environment Variables, Networks, and Volumes

## 📌 Objective

Learn how to create a more secure Docker Compose application by using environment variables stored in a `.env` file, persistent Docker volumes, custom bridge networks, and multiple services including Nginx, MySQL, and Redis.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker Compose
- Docker CLI
- Nginx
- MySQL 8.0
- Redis 7
- YAML
- Environment Variables (.env)
- Docker Networks
- Docker Volumes
- Windows PowerShell

---

## 📚 Concepts Learned

- Secure Docker Compose
- Environment Variables
- `.env` File
- Persistent Storage
- Docker Volumes
- Custom Bridge Networks
- Multi-Container Applications
- Service Isolation
- Container Logs
- Docker Lifecycle Management

---

## 📄 compose.yaml

```
services:
  web:
    image: nginx:latest
    container_name: web
    ports:
      - "8080:80"
    restart: unless-stopped
    networks:
      - backend

  db:
    image: mysql:8.0
    container_name: db
    restart: unless-stopped
    environment:
      MYSQL_ROOT_PASSWORD: ${MYSQL_ROOT_PASSWORD}
    volumes:
      - db_data:/var/lib/mysql
    networks:
      - backend

  cache:
    image: redis:7
    container_name: cache
    restart: unless-stopped
    networks:
      - backend

networks:
  backend:

volumes:
  db_data:
```

---

## 📄 .env File

```
MYSQL_ROOT_PASSWORD=StrongPassword123!
```

---

## 📝 Configuration Overview

### Web Service

- Uses the latest Nginx image.
- Publishes port **8080**.
- Automatically restarts if stopped.
- Connected to the backend network.

---

### Database Service

- Uses MySQL 8.0.
- Stores the root password in a `.env` file instead of hardcoding it.
- Uses a Docker volume for persistent data.
- Connected to the backend network.

---

### Cache Service

- Uses Redis 7.
- Shares the backend network with other services.
- Automatically restarts when required.

---

## 🔐 Security Improvements

- Sensitive credentials stored in a `.env` file.
- Password not hardcoded directly inside `compose.yaml`.
- Custom bridge network isolates services.
- Persistent volume protects database data.
- Restart policy improves service availability.

---

# ⚡ Commands Used

## Create Project

```
mkdir secure-docker-compose
cd secure-docker-compose
```

---

## Create Configuration Files

```
notepad compose.yaml
notepad .env
```

---

## Validate Compose Configuration

```
docker compose config
```

Checks whether the Compose configuration is valid and correctly resolves environment variables.

---

## Start All Services

```
docker compose up -d
```

Creates the network and volume, and starts all containers.

---

## View Running Containers

```
docker ps
```

Lists all active containers.

---

## Verify Nginx

Open:

```
http://localhost:8080
```

Displays the Nginx Welcome Page.

---

## View Web Logs

```
docker compose logs web
```

---

## View MySQL Logs

```
docker compose logs db
```

---

## View Redis Logs

```
docker compose logs cache
```

---

## List Docker Networks

```
docker network ls
```

---

## List Docker Volumes

```
docker volume ls
```

---

## View Compose Services

```
docker compose ps
```

---

## Remove Containers, Networks, and Volumes

```
docker compose down -v
```

Removes the complete Docker Compose environment.

---

# 🌐 Browser Verification

Successfully opened:

```
http://localhost:8080
```

The **Nginx Welcome Page** confirmed that the web service was running correctly.

---

# 🧪 What I Practised

- Created a secure Docker Compose project.
- Used environment variables through a `.env` file.
- Configured Nginx, MySQL, and Redis services.
- Created a custom Docker bridge network.
- Configured persistent Docker volumes.
- Validated the Compose configuration.
- Started multiple containers together.
- Viewed service logs.
- Verified running services.
- Removed the complete environment using Docker Compose.

---

# 📸 Screenshots

### Screenshot 1

- Created project directory
- Created `compose.yaml`
- Created `.env`
- Validated configuration

---

### Screenshot 2

- Docker Compose configuration file

---

### Screenshot 3

- Environment variable stored in `.env`

---

### Screenshot 4

- Started all services
- Verified running containers

---

### Screenshot 5

- Nginx Welcome Page opened successfully

---

### Screenshot 6

- Viewed Nginx and MySQL logs

---

### Screenshot 7

- Viewed Redis logs
- Listed Docker networks
- Listed Docker volumes
- Verified Compose services

---

### Screenshot 8

- Removed containers, network, and volume using `docker compose down -v`

---

# 🎯 Skills Practised

- Docker Compose
- Secure Configuration
- Environment Variables
- `.env` Files
- Docker Networks
- Docker Volumes
- Multi-Container Deployment
- Nginx
- MySQL
- Redis
- Docker CLI
- Container Lifecycle Management

---

# ✅ Outcome

Successfully built a secure multi-container Docker Compose application using Nginx, MySQL, and Redis. Learned how to protect sensitive information with environment variables, persist database data using Docker volumes, isolate services through custom networks, inspect container logs, and manage the complete application lifecycle using Docker Compose.
