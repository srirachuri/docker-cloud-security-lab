# 🐳 Day 4 – Docker Images & Docker Hub

## 📌 Objective

Learn how to manage Docker images by downloading images from Docker Hub, listing locally stored images, and understanding why Docker prevents the deletion of images that are currently in use by running containers.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Windows PowerShell
- Docker Hub
- Nginx
- Ubuntu
- Hello World Image

---

## 📚 Concepts Learned

- Docker Hub
- Docker Images
- Pulling Images
- Listing Images
- Image Tags
- Image IDs
- Image Removal
- Image Dependency
- Official Docker Images

---

## ⚡ Commands Used

### Pull the Official Nginx Image

```
docker pull nginx
```

Downloads the latest official Nginx image from Docker Hub.

---

### List Local Images

```
docker images
```

Displays all Docker images stored on the local machine.

---

### Remove an Image

```
docker rmi nginx
```

Attempts to remove the Nginx image.

---

## 🧪 What I Practised

- Downloaded the official Nginx image.
- Listed all locally available Docker images.
- Identified image names, tags, IDs, and sizes.
- Attempted to remove the Nginx image.
- Observed Docker's protection mechanism when an image is still being used by a running container.

---

## 📸 Screenshot

### Docker Images and Docker Hub

The screenshot demonstrates:

- Successfully pulling the official **Nginx** image.
- Listing all locally stored Docker images.
- Viewing image details such as Repository, Tag, Image ID, and Size.
- Attempting to remove the Nginx image.
- Docker prevented image deletion because a running container was still using that image.

---

## 🔒 Security Notes

- Used the official Nginx image from Docker Hub.
- Docker prevents accidental deletion of images that are required by active containers.
- Official images are recommended because they are maintained and regularly updated.
- Verify whether an image is in use before attempting to remove it.

---

## 🎯 Skills Practiced

- Docker CLI
- Docker Hub
- Image Management
- Docker Images
- Image Inspection
- Docker Administration
- Basic Container Management

---

## ⚠️ Error Encountered

While attempting to remove the Nginx image, Docker returned the following error:

```
Error response from daemon:
conflict: unable to delete nginx:latest
container <container_id> is using its referenced image
```

### Reason

The Nginx image could not be removed because one or more running containers were still using it.

### Resolution

Before removing an image:

1. View running containers.

```
docker ps
```

2. Stop the container.

```
docker stop <container_id>
```

3. Remove the container.

```
docker rm <container_id>
```

4. Remove the image.

```
docker rmi nginx
```

---

## ✅ Outcome

Successfully learned how Docker images are managed, how to download images from Docker Hub, inspect locally stored images, and understand Docker's safety mechanism that prevents the deletion of images currently used by running containers.

This exercise strengthened my understanding of Docker image management, an essential skill for Cloud Engineering, DevOps, and Cloud Security.
