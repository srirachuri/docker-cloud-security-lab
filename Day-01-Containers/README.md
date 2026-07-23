# 🐳 Day 1 – Docker Containers (Core Concepts)

## 📌 Overview

On Day 1, I learned the fundamentals of Docker by working with containers and images. I installed Docker Desktop, downloaded the official Nginx image, created and managed a container, and accessed a web server running inside Docker.

This project helped me understand how containers work and why they are widely used in Cloud Computing and Cloud Security.

---

## 🎯 Learning Objectives

- Understand Docker containers
- Learn the difference between Images and Containers
- Download images from Docker Hub
- Run an Nginx container
- Access a containerised web application
- Stop and remove containers
- Practice basic Docker commands

---

## 🛠 Technologies

- Docker Desktop
- Docker CLI
- Nginx
- Windows PowerShell

---

## 📂 Commands Used

### Check Docker Installation

docker --version
docker info

---

### Pull the Official Nginx Image

```bash
docker pull nginx
```

---

### View Downloaded Images

docker images

---

### Run an Nginx Container

docker run -d -p 8080:80 nginx
```

Explanation:

- `-d` → Run the container in detached mode
- `-p 8080:80` → Map host port 8080 to container port 80

---

### View Running Containers

docker ps

---

### Stop the Container

docker stop <container_name>

Example

docker stop sad_grothendieck

---

### View All Containers

docker ps -a

---

### Remove the Container

docker rm <container_name>

Example

docker rm sad_grothendieck

---

## 🌐 Result

Successfully deployed the official **Nginx** web server inside a Docker container.

Accessed the application using:

http://localhost:8080

The browser displayed the default **"Welcome to nginx!"** page.

---

## 📸 Screenshots

### Docker Installation

- Verified Docker installation using:
  - `docker --version`
  - `docker info`

### Docker Image

- Pulled the official Nginx image from Docker Hub.
- Verified downloaded images using:

docker images

### Running Container

- Started the Nginx container.
- Verified the running container using:

docker ps

### Browser Output

Successfully accessed:

http://localhost:8080

and received the default **Welcome to nginx!** page.

### Container Cleanup

Stopped the container using:

docker stop sad_grothendieck

Removed the container using:

docker rm sad_grothendieck

Verified cleanup with:

docker ps -a


---

## 📚 Key Concepts Learned

- Docker Image
- Docker Container
- Docker Hub
- Docker CLI
- Port Mapping
- Detached Mode
- Container Lifecycle
- Host Port vs Container Port

---

## 🔒 Security Notes

- Used the official Nginx image from Docker Hub.
- Exposed only the required port (8080).
- Removed unused containers to keep the Docker environment clean.
- Verified Docker installation before deployment.

---

## 🎯 Outcome

By completing this lab, I learned how to:

- Install Docker Desktop
- Download Docker images
- Create containers
- Run web applications inside containers
- Access applications through port mapping
- Stop and remove containers
- Understand the basic Docker workflow

---
