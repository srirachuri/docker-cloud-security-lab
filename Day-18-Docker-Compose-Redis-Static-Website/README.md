# 🚀 Day 18 – Docker Compose Project: Nginx + Redis

## 📌 Objective

Build a simple multi-container application using **Docker Compose** by running:

- An Nginx web server
- A Redis container
- A custom HTML page
- A shared Docker network

The project also includes container inspection, log analysis, security scanning with Trivy, and cleanup.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker Compose
- Nginx (stable-alpine)
- Redis (7-alpine)
- HTML
- Trivy
- Windows PowerShell

---

## 📚 Concepts Learned

- Docker Compose
- Multi-container Applications
- Docker Networking
- Volume Mounts
- Container Logs
- Container Inspection
- Docker Security Scanning
- Alpine Linux Images
- Docker Cleanup

---

# 📁 Project Structure

```
docker-nginx-redis-project/
│
├── docker-compose.yaml
└── index.html
```

---

# 🌐 Project Overview

Created a Docker Compose project consisting of:

- Nginx container
- Redis container
- Custom HTML webpage
- Custom Docker network

Docker Compose automatically created the required containers and network.

---

# 📄 Custom Web Page

Created an **index.html** file containing:

- Hello from Docker
- Nginx Container Running Successfully
- Redis Container Running Successfully
- Junior Cloud Security Engineer Portfolio Project

The webpage was mounted into the Nginx container using a bind mount.

---

# 🚀 Start the Project

Created the project folder and started all services.

```
mkdir docker-nginx-redis-project

cd docker-nginx-redis-project

docker compose up -d
```

Docker Compose created:

- Network
- Nginx container
- Redis container

---

# 📦 Verify Running Containers

Checked running containers.

```
docker ps
```

Verified:

- Nginx running
- Redis running
- Port mappings
- Container names
- Images

---

# 🌍 Test the Website

Opened:

```
http://localhost:8081
```

Confirmed the Nginx web server was running successfully.

---

# 📋 View Redis Logs

Displayed Redis startup logs.

```
docker compose logs redis
```

Verified:

- Redis initialised successfully
- Server ready to accept connections
- Database loaded correctly

---

# 🔍 Inspect Container

Inspected the Nginx container.

```
docker inspect mywebsite
```

Observed:

- Container ID
- Image details
- Mounts
- Network configuration
- Running state
- Port bindings
- Restart policy

---

# 🛡 Scan Nginx Image

Scanned the Nginx Alpine image for vulnerabilities.

```
trivy image nginx:stable-alpine
```

The report included:

- Vulnerability summary
- Severity levels
- Installed package versions
- Fixed versions
- CVE details

---

# 🛡 Scan Redis Image

Scanned the Redis Alpine image.

```
trivy image redis:7-alpine
```

Result:

- No security vulnerabilities detected

---

# 🧹 Stop the Project

Stopped and removed containers.

```
docker compose down
```

---

# 🧹 Clean Docker Resources

Removed unused Docker resources.

```
docker system prune
```

---

# ⚡ Commands Used

## Create Project Folder

```
mkdir docker-nginx-redis-project
```

---

## Start Docker Compose

```
docker compose up -d
```

---

## View Running Containers

```
docker ps
```

---

## View Redis Logs

```
docker compose logs redis
```

---

## Inspect Container

```
docker inspect mywebsite
```

---

## Scan Nginx Image

```
trivy image nginx:stable-alpine
```

---

## Scan Redis Image

```
trivy image redis:7-alpine
```

---

## Stop Containers

```
docker compose down
```

---

## Remove Unused Docker Resources

```
docker system prune
```

---

# 🧪 What I Practised

- Created a Docker Compose project.
- Built a multi-container application.
- Used Docker networking.
- Mounted a custom HTML file into Nginx.
- Started services with Docker Compose.
- Verified running containers.
- Viewed Redis logs.
- Inspected container configuration.
- Performed vulnerability scans using Trivy.
- Cleaned Docker resources after testing.

---

# 📸 Screenshots

### Screenshot 1

- Created project directory
- Started Docker Compose
- Verified running containers

---

### Screenshot 2

- Created custom `index.html`

---

### Screenshot 3

- Created `docker-compose.yaml`

---

### Screenshot 4

- Verified the Nginx website in the browser

---

### Screenshot 5

- Viewed Redis logs
- Inspected the Nginx container

---

### Screenshot 6

- Continued container inspection
- Reviewed bind mounts and networking

---

### Screenshot 7

- Scanned the Nginx Alpine image with Trivy

---

### Screenshot 8

- Reviewed Nginx vulnerability details

---

### Screenshot 9

- Scanned the Redis Alpine image
- Stopped Docker Compose services

---

### Screenshot 10

- Cleaned unused Docker resources

---

# 🎯 Skills Practised

- Docker Compose
- Docker Networking
- Multi-container Applications
- Nginx
- Redis
- HTML Deployment
- Bind Mounts
- Container Inspection
- Docker Logs
- Docker Security
- Trivy
- Vulnerability Scanning
- Docker Cleanup

---

# 📖 Key Learnings

- Docker Compose simplifies managing multiple containers.
- Containers can communicate over a custom Docker network.
- Bind mounts allow serving local files from containers.
- Container logs help monitor application health.
- Docker Inspect provides detailed container metadata.
- Trivy helps identify vulnerabilities before deployment.
- Alpine-based images are lightweight and often have fewer vulnerabilities.

---

# ✅ Outcome

Successfully built a multi-container Docker Compose project using **Nginx** and **Redis**, deployed a custom HTML webpage, verified container networking and logs, inspected container configuration, performed security scans using Trivy, and cleaned up Docker resources after completing the project.
