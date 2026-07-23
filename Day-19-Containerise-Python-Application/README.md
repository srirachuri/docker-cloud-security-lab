# 🐍 Day 19 – Containerise a Python Application with Docker

## 📌 Objective

Containerise a simple Python application using Docker by creating a secure Dockerfile, excluding unnecessary files with `.dockerignore`, building a custom image, and running the application inside a Docker container.

---

## 🛠 Technologies Used

- Docker Desktop
- Python 3.10
- Dockerfile
- .dockerignore
- Windows PowerShell

---

## 📚 Concepts Learned

- Docker Image Creation
- Dockerfile Instructions
- Python Containerization
- Non-Root Containers
- Docker Build Context
- .dockerignore
- Docker Images
- Running Containers

---

# 📁 Project Structure

```
python_docker/
│
├── app.py
├── Dockerfile
└── .dockerignore
```

---

# 🌐 Project Overview

Created a simple Python application and packaged it into a Docker image using a custom Dockerfile.

The application prints:

- Current timestamp
- Python version
- Application status
- Security best practices

The container runs as a **non-root user** to improve security.

---

# 🐍 Python Application

Created **app.py** containing:

- Current timestamp
- Python version
- Docker execution status
- Security reminders

Example output:

```
🔒 Python Log Parser

Timestamp : 2026-07-10

Python Version : 3.10.20

Application Status

✅ Running successfully inside Docker

Security Message

Do not hardcode passwords or API keys.
Use environment variables for sensitive data.
```

---

# 📄 Dockerfile

Created a Dockerfile using the official Python Slim image.

Key steps:

- Used `python:3.10-slim`
- Set the working directory
- Copied the application
- Created a non-root user
- Switched to the non-root user
- Executed the Python script

---

# 🚫 .dockerignore

Created a `.dockerignore` file to exclude unnecessary files from the build context.

Ignored:

- `__pycache__/`
- `*.pyc`
- `.git`
- `README.md`

This reduces image size and speeds up Docker builds.

---

# 🏗 Build Docker Image

Built the Docker image.

```
docker build -t log-parser .
```

Docker successfully:

- Loaded the Dockerfile
- Downloaded the Python base image
- Created image layers
- Built the custom image

---

# 📦 Verify Docker Images

Listed available Docker images.

```
docker images
```

Verified the custom image:

```
log-parser:latest
```

---

# ▶ Run the Container

Executed the container.

```
docker run --rm log-parser
```

The application displayed:

- Timestamp
- Python version
- Running status
- Security reminders

The `--rm` flag automatically removed the container after execution.

---

# 📋 Verify Containers

Checked container information.

```
docker ps -a
```

Confirmed that the temporary Python container had been removed after execution.

---

# ⚡ Commands Used

## Create Project Folder

```
mkdir python_docker
```

---

## Build Docker Image

```
docker build -t log-parser .
```

---

## View Docker Images

```
docker images
```

---

## Run Container

```
docker run --rm log-parser
```

---

## View Containers

```
docker ps -a
```

---

# 🧪 What I Practised

- Created a Python application.
- Wrote a Dockerfile.
- Created a `.dockerignore` file.
- Used the official Python Slim image.
- Built a custom Docker image.
- Ran a Python application inside Docker.
- Executed the container as a non-root user.
- Verified Docker images.
- Verified container lifecycle.
- Used `--rm` to automatically clean up containers.

---

# 📸 Screenshots

### Screenshot 1

- Created the project directory
- Built the Docker image

---

### Screenshot 2

- Created `app.py`

---

### Screenshot 3

- Created the `Dockerfile`

---

### Screenshot 4

- Created the `.dockerignore` file

---

### Screenshot 5

- Verified Docker images
- Ran the Python container

---

### Screenshot 6

- Displayed the application output
- Verified containers with `docker ps -a`

---

# 🎯 Skills Practised

- Docker
- Dockerfile
- Python
- Containerization
- Docker Images
- Docker Build
- Docker Run
- Non-Root Containers
- .dockerignore
- Docker CLI
- Secure Container Configuration

---

# 📖 Key Learnings

- Docker packages Python applications into portable containers.
- The `python:3.10-slim` image provides a lightweight runtime.
- Running containers as a non-root user improves security.
- `.dockerignore` reduces build context and speeds up image creation.
- The `--rm` option automatically removes temporary containers after execution.
- Docker images can be verified using `docker images`.
- Container execution can be verified with `docker ps -a`.

---

# ✅ Outcome

Successfully containerised a Python application using Docker, created a secure Dockerfile with a non-root user, optimised the build using `.dockerignore`, built a custom Docker image, executed the application inside a container, and verified the image and container lifecycle using Docker CLI commands.
