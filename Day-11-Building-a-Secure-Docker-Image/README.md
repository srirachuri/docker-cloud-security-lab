# 🔐 Day 11 – Building a Secure Docker Image

## 📌 Objective

Learn Docker image hardening by creating a secure Docker image using Dockerfile best practices. This includes using a version-pinned base image, minimising installed packages, creating a non-root user, inspecting image layers, scanning for vulnerabilities, and cleaning up unused images.

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

- Docker Image Hardening
- Version-Pinned Base Images
- Non-Root Containers
- Package Cache Cleanup
- Least Privilege Principle
- Docker Image Inspection
- Docker Image History
- Vulnerability Scanning
- Image Cleanup

---

## 📄 Dockerfile Used

```
# Use a trusted and version-pinned base image
FROM ubuntu:24.04

# Avoid interactive prompts
ENV DEBIAN_FRONTEND=noninteractive

# Install only the required package and clean up package cache
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl && \
    rm -rf /var/lib/apt/lists/*

# Create a non-root user
RUN useradd -m appuser

# Run the container with least privilege
USER appuser

# Default command
CMD ["bash"]
```

---

## 📝 Dockerfile Explanation

### FROM ubuntu:24.04

Uses a trusted Ubuntu 24.04 image instead of the floating `latest` tag for consistent and predictable builds.

---

### ENV DEBIAN_FRONTEND=noninteractive

Disables interactive installation prompts during package installation.

---

### RUN apt-get update

Updates the package index.

---

### apt-get install --no-install-recommends curl

Installs only the required package (`curl`) without unnecessary recommended packages.

---

### rm -rf /var/lib/apt/lists/*

Deletes cached package lists to reduce image size.

---

### RUN useradd -m appuser

Creates a dedicated non-root user for improved container security.

---

### USER appuser

Runs the container as a non-root user instead of the root user.

---

### CMD ["bash"]

Starts an interactive Bash shell when the container runs.

---

# ⚡ Commands Used

## Create Project Directory

```
mkdir secure_docker_image
cd secure_docker_image
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

## Build Secure Docker Image

```
docker build -t secure-ubuntu:v1 .
```

Builds the Docker image using the secure Dockerfile.

---

## Run the Container

```
docker run -it secure-ubuntu:v1
```

Starts the container.

---

## Verify Installed Package

```
curl --version
```

Confirms that curl is installed.

---

## Verify Current User

```
whoami
```

Output:

```
appuser
```

Confirms that the container is running as a non-root user.

---

## Inspect Image

```
docker inspect secure-ubuntu:v1
```

Displays image metadata including:

- Environment variables
- Default user
- Image layers
- Architecture
- Commands

---

## View Image History

```
docker history secure-ubuntu:v1
```

Shows the build history and image layers.

---

## Scan Image for Vulnerabilities

```
trivy image secure-ubuntu:v1
```

Scans the image for known security vulnerabilities and reports affected packages.

---

## View Containers

```
docker ps -a
```

Lists all running and stopped containers.

---

## Remove Old Containers

```
docker rm <container_id>
```

Deletes unused containers.

---

## Remove Old Image

```
docker rmi my-first-image
```

Deletes an unused Docker image.

---

# 🧪 What I Practised

- Created a secure Docker project.
- Wrote a secure Dockerfile.
- Used a version-pinned Ubuntu base image.
- Installed only required packages.
- Cleaned package cache to reduce image size.
- Created a non-root user.
- Ran the container using least privilege.
- Verified installed packages.
- Verified the current container user.
- Inspected Docker image metadata.
- Reviewed Docker image history.
- Scanned the image using Trivy.
- Removed unused containers.
- Removed unused Docker images.

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

- Built secure Docker image
- Ran the container
- Verified `curl`
- Verified a non-root user using `whoami`

---

### Screenshot 4

- Inspected Docker image metadata

---

### Screenshot 5

- Viewed image history

---

### Screenshot 6

- Scanned image with Trivy
- Displayed vulnerability summary

---

### Screenshot 7

- Reviewed detailed vulnerability report

---

### Screenshot 8

- Listed containers
- Removed unused containers
- Removed unused image
- Verified remaining containers

---

# 🔒 Security Best Practices Learned

- Pin image versions instead of using `latest`.
- Install only necessary packages.
- Remove package cache after installation.
- Use a dedicated non-root user.
- Follow the Principle of Least Privilege.
- Scan images regularly for vulnerabilities.
- Remove unused images and containers to maintain a clean environment.

---

# 🎯 Skills Practised

- Docker Security
- Secure Dockerfile Design
- Docker Image Hardening
- Non-Root Containers
- Trivy Security Scanning
- Docker Image Inspection
- Docker Image History
- Docker Cleanup
- Linux User Management

---

# ✅ Outcome

Successfully built and tested a secure Docker image using Dockerfile security best practices. Verified that the container runs as a non-root user, inspected the image configuration, reviewed image layers, scanned for vulnerabilities using Trivy, and cleaned up unused Docker resources. This exercise strengthened practical knowledge of Docker security and secure container image creation.
