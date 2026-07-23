# 🐳 Day 13 – Data Persistence & Environment Variables in Docker

## 📌 Objective

Learn how Docker environment variables work by passing variables at runtime and defining default environment variables inside a Docker image using a Dockerfile.

This exercise demonstrates how Docker containers can be configured without modifying application code, making deployments more flexible and portable.

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
- Runtime Environment Variables
- Dockerfile `ENV` Instruction
- Docker Image Build Process
- Docker Image Inspection
- Container Configuration
- Default Environment Variables

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

Creates a default environment variable named `APP_ENV` with the value `production`.

---

### ENV APP_NAME=SecurityLab

Creates another environment variable named `APP_NAME`.

---

### CMD ["env"]

Runs the `env` command when the container starts, displaying all environment variables.

---

# ⚡ Commands Used

## Pass Environment Variable at Runtime

```
docker run --rm -e APP_ENV=development ubuntu env
```

Displays the runtime environment variable.

---

## Pass Multiple Environment Variables

```
docker run --rm -e APP_ENV=production -e APP_NAME=SecurityLab ubuntu env
```

Creates multiple environment variables for the container.

---

## Display a Specific Environment Variable

```
docker run --rm -e USER_NAME=SRI ubuntu printenv USER_NAME
```

Outputs:

```
SRI
```

---

## Create Project Directory

```
mkdir data-persistence-and-environment-variables
cd data-persistence-and-environment-variables
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

Builds the Docker image.

---

## Run the Image

```
docker run --rm env.demo
```

Displays all environment variables configured inside the image.

---

## Inspect the Image

```
docker inspect env.demo
```

Shows Docker image metadata, including:

- Image ID
- Environment Variables
- Default Command
- Image Layers
- Architecture

---

# 🧪 What I Practised

- Passed environment variables at runtime.
- Used multiple environment variables.
- Retrieved a specific environment variable.
- Created a Dockerfile using the `ENV` instruction.
- Built a Docker image.
- Executed a Docker container.
- Verified environment variables inside the container.
- Inspected Docker image metadata.

---

# 📸 Screenshots

### Screenshot 1

- Passed runtime environment variables
- Created project directory
- Created Dockerfile
- Built Docker image

---

### Screenshot 2

- Dockerfile contents

---

### Screenshot 3

- Successfully built Docker image
- Ran the Docker container
- Displayed configured environment variables
- Started Docker image inspection

---

### Screenshot 4

- Docker inspect output (Image metadata)

---

### Screenshot 5

- Docker inspect output (Environment variables and image details)

---

# 🌟 Why Environment Variables Matter

- Store configuration separately from application code.
- Simplify deployment across development, testing, and production.
- Improve portability.
- Reduce hard-coded configuration.
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
- Container Configuration

---

# ✅ Outcome

Successfully learned how to use Docker environment variables by passing variables at runtime and defining default variables inside a Dockerfile. Built and executed a Docker image, verified environment variables, and inspected image metadata to understand how Docker stores container configuration.
