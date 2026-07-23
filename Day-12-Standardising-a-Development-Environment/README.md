# 🐳 Day 12 – Standardising a Development Environment with Docker

## 📌 Objective

Learn how Docker helps standardise development environments by creating a reusable Docker image that provides the same software and configuration across different systems. This ensures consistency, portability, and reproducible builds.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Dockerfile
- Ubuntu 24.04
- Trivy Vulnerability Scanner
- Windows PowerShell

---

## 📚 Concepts Learned

- Development Environment Standardisation
- Docker Images
- Dockerfile
- Version-Pinned Base Images
- Minimal Package Installation
- Docker Image Build Process
- Docker Image Inspection
- Docker Image History
- Vulnerability Scanning

---

## 📄 Dockerfile Used

```
# Use a trusted, version-pinned Ubuntu base image
FROM ubuntu:24.04

# Avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Install only the required package and clean up the package cache
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl && \
    rm -rf /var/lib/apt/lists/*

# Default command
CMD ["bash"]
```

---

## 📝 Dockerfile Explanation

### FROM ubuntu:24.04

Uses Ubuntu 24.04 as the base image with a fixed version for consistent builds.

---

### ENV DEBIAN_FRONTEND=noninteractive

Disables interactive prompts during package installation.

---

### RUN apt-get update

Updates the package repository.

---

### apt-get install --no-install-recommends curl

Installs only the required package (`curl`) while avoiding unnecessary dependencies.

---

### rm -rf /var/lib/apt/lists/*

Removes cached package lists to reduce image size.

---

### CMD ["bash"]

Starts a Bash shell when the container runs.

---

# ⚡ Commands Used

## Create Project Directory

```
mkdir standard-dev-env
cd standard-dev-env
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
docker build -t developer-base:v1 .
```

Builds the Docker image from the Dockerfile.

---

## List Docker Images

```
docker images
```

Displays all locally available Docker images.

---

## Run the Container

```
docker run -it developer-base:v1
```

Starts an interactive container.

---

## Verify Installed Package

```
curl --version
```

Confirms that curl is installed inside the container.

---

## Verify Current User

```
whoami
```

Displays the current user.

Output:

```
root
```

Since no custom user was created in this Dockerfile, the container runs as the default root user.

---

## Inspect Docker Image

```
docker inspect developer-base:v1
```

Displays metadata such as:

- Image ID
- Environment variables
- Default command
- Image layers
- Architecture

---

## View Image History

```
docker history developer-base:v1
```

Shows every layer created while building the image.

---

## Scan Image for Vulnerabilities

```
trivy image developer-base:v1
```

Scans the Docker image for known security vulnerabilities and reports affected packages.

---

# 🧪 What I Practised

- Created a standardised Docker development environment.
- Wrote a reusable Dockerfile.
- Used a version-pinned Ubuntu image.
- Installed only the required packages.
- Cleaned the package cache to reduce image size.
- Built a Docker image.
- Listed available Docker images.
- Ran a Docker container.
- Verified installed software.
- Checked the default container user.
- Inspected Docker image metadata.
- Reviewed Docker image history.
- Performed vulnerability scanning using Trivy.

---

# 📸 Screenshots

### Screenshot 1

- Created project directory
- Created Dockerfile
- Renamed Dockerfile

---

### Screenshot 2

- Dockerfile contents

---

### Screenshot 3

- Built Docker image
- Listed Docker images
- Ran the container
- Verified `curl`
- Verified current user

---

### Screenshot 4

- Inspected Docker image metadata

---

### Screenshot 5

- Viewed Docker image history

---

### Screenshot 6

- Performed Trivy vulnerability scan
- Viewed vulnerability summary

---

### Screenshot 7

- Reviewed detailed vulnerability report

---

# 🌟 Benefits of Standardised Development Environments

- Consistent development setup across machines.
- Eliminates "works on my machine" issues.
- Simplifies onboarding for new developers.
- Improves portability between development and production.
- Supports reproducible builds.
- Makes collaboration easier within teams.

---

# 🎯 Skills Practised

- Docker
- Dockerfile Creation
- Docker Image Building
- Docker Image Inspection
- Docker Image History
- Docker Development Environment
- Package Management
- Linux Commands
- Trivy Security Scanning

---

# ✅ Outcome

Successfully created a standardised Docker-based development environment using Ubuntu 24.04. Built and tested the Docker image, verified installed tools, inspected image metadata, reviewed image layers, and scanned the image with Trivy for vulnerabilities. This exercise demonstrated how Docker provides consistent and portable development environments across different systems.
