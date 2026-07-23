# 🐳 Day 6 – Docker Image Management

## 📌 Objective

Learn how to inspect Docker images, view image layers, understand image metadata, scan images for vulnerabilities, and safely remove Docker images after stopping and deleting dependent containers.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Windows PowerShell
- Docker Hub
- Trivy

---

## 📚 Concepts Learned

- Docker Images
- Image Metadata
- Image Layers
- Docker History
- Image Inspection
- Vulnerability Scanning
- Container Dependencies
- Image Cleanup

---

## ⚡ Commands Used

### View Available Images

```
docker images
```

Lists all Docker images stored on the local machine.

---

### Inspect Docker Image

```
docker image inspect nginx
```

Displays detailed information about the Docker image, including:

- Image ID
- Repository Tags
- Environment Variables
- Labels
- Entrypoint
- Architecture
- Operating System
- Root Filesystem

---

### View Image History

```
docker history nginx
```

Shows all image layers used to build the Docker image.

---

### Scan Image with Trivy

```
trivy image nginx
```

Scans the image for known vulnerabilities and security issues.

---

### Remove Docker Image

```
docker rmi nginx
```

Attempts to remove the Docker image.

If containers are still using the image, Docker prevents deletion.

---

### View All Containers

```
docker ps -a
```

Lists both running and stopped containers.

---

### Stop Running Containers

```
docker stop <container-id>
```

Stops containers that are currently running.

Example:

```
docker stop 1be0cc0bec8f 07de158128c3 3a3dcd50e3f0 bee9b4100a3e
```

---

### Remove Containers

```
docker rm <container-id>
```

Deletes stopped containers.

Example:

```
docker rm 1be0cc0bec8f 07de158128c3 3a3dcd50e3f0 bee9b4100a3e
```

---

### Remove Image Successfully

```
docker rmi nginx
```

Removes the image after all dependent containers have been deleted.

---

## 🧪 What I Practised

- Listed local Docker images.
- Inspected image metadata.
- Viewed Docker image layers.
- Examined environment variables and labels.
- Performed vulnerability scanning using Trivy.
- Identified why Docker prevents image deletion.
- Stopped running containers.
- Removed stopped containers.
- Successfully deleted the Docker image.

---

## 📸 Screenshots

### Screenshot 1 – Listing Images and Inspecting Image

- Displayed local Docker images.
- Inspected the Nginx image metadata.

---

### Screenshot 2 – Viewing Image History

- Displayed all image layers.
- Understood how the Docker image was built.

---

### Screenshot 3 – Trivy Vulnerability Scan

- Scanned the Nginx image.
- Reviewed vulnerability detection.

---

### Screenshot 4 – Image Deletion Conflict

- Attempted to remove the image.
- Observed Docker preventing deletion because containers were using the image.

---

### Screenshot 5 – Container Cleanup and Image Removal

- Listed containers.
- Stopped running containers.
- Removed stopped containers.
- Successfully removed the Docker image.

---

## 🔒 Key Learning

Docker protects images from accidental deletion.

An image cannot be removed while one or more containers (running or stopped) depend on it.

The correct cleanup sequence is:

1. Stop running containers.
2. Remove containers.
3. Remove the Docker image.

---

## 🎯 Skills Practiced

- Docker Image Management
- Image Inspection
- Docker History
- Container Management
- Vulnerability Scanning
- Image Cleanup
- Docker CLI
- Container Security Basics

---

## ✅ Outcome

Successfully learned how Docker manages image dependencies, inspected Docker image metadata and layers, scanned images for vulnerabilities using Trivy, resolved image deletion conflicts by removing dependent containers, and safely cleaned up Docker images. These are essential skills for Docker administration, DevOps, and Cloud Security.
