# 🔐 Day 14 – Secure Application Configuration with Environment Variables

## 📌 Objective

Learn how to securely configure Docker applications using environment variables defined in a Dockerfile. This practice demonstrates how configuration values can be separated from application logic, making containers easier to manage and deploy across different environments.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Dockerfile
- Ubuntu 24.04
- Windows PowerShell

---

## 📚 Concepts Learned

- Docker Environment Variables
- Dockerfile `ENV` Instruction
- Application Configuration
- Docker Image Build
- Docker Container Execution
- Docker Image Inspection
- Secure Configuration Management

---

## 📄 Dockerfile Used

```
FROM ubuntu:24.04

ENV APP_ENV=production
ENV APP_NAME=SecurityLab

CMD ["env"]
```

---

## 📝 Dockerfile Explanation

### FROM ubuntu:24.04

Uses Ubuntu 24.04 as the base image.

---

### ENV APP_ENV=production

Defines the default application environment as **production**.

---

### ENV APP_NAME=SecurityLab

Defines the application name inside the container.

---

### CMD ["env"]

Runs the `env` command when the container starts, displaying all configured environment variables.

---

# ⚡ Commands Used

## Create Project Directory

```
mkdir Day-14-Secure-Application-Configuration-with-Environment-Variables
cd Day-14-Secure-Application-Configuration-with-Environment-Variables
```

---

## Create Dockerfile

```
notepad Dockerfile
```

---

## Rename Dockerfile

```
ren Dockerfile.txt Dockerfile
```

---

## Build Docker Image

```
docker build -t env.demo .
```

Builds a Docker image named **env.demo**.

---

## Run Docker Container

```
docker run --rm env.demo
```

Displays all environment variables stored inside the image.

---

## Inspect Docker Image

```
docker inspect env.demo
```

Displays detailed image metadata, including:

- Image ID
- Environment Variables
- Default Command
- Architecture
- Layers
- Labels

---

# 🧪 What I Practised

- Created a Docker project directory.
- Wrote a Dockerfile using the `ENV` instruction.
- Built a Docker image.
- Ran the Docker container.
- Displayed configured environment variables.
- Verified environment variables using `docker inspect`.
- Learned how Docker stores application configuration.

---

# 📸 Screenshots

### Screenshot 1

- Created project directory
- Created Dockerfile
- Built Docker image successfully

---

### Screenshot 2

- Dockerfile source code

---

### Screenshot 3

- Executed Docker container
- Displayed configured environment variables
- Began Docker image inspection

---

### Screenshot 4

- Docker inspect output showing image metadata and configured environment variables

---

# 🔐 Why Environment Variables Are Important

- Separate configuration from application code.
- Support different deployment environments.
- Avoid hard-coded configuration values.
- Simplify application deployment.
- Follow Docker and cloud-native best practices.

---

# 🎯 Skills Practised

- Docker
- Dockerfile
- Docker ENV Instruction
- Docker Build
- Docker Run
- Docker Inspect
- Environment Variables
- Application Configuration

---

# ✅ Outcome

Successfully created a Docker image with predefined environment variables, executed the container to verify the configuration, and inspected the image metadata to understand how Docker stores environment variables for secure and flexible application configuration.
