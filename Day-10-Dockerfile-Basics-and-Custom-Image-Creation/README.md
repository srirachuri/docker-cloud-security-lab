# 🐳 Day 10 – Dockerfile Basics and Custom Image Creation

## 📌 Objective

Learn how to create a custom Docker image using a Dockerfile, build the image, run a container from it, verify installed software, and inspect image metadata.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Ubuntu Base Image
- Dockerfile
- Windows PowerShell

---

## 📚 Concepts Learned

- Dockerfile Basics
- Base Images
- Image Building
- Custom Docker Images
- Docker Image Inspection
- Container Execution

---

## 📄 Dockerfile Used

```
FROM ubuntu

RUN apt update && apt install -y curl

CMD ["bash"]
```

### Explanation

- **FROM ubuntu**
  - Uses the latest Ubuntu image as the base image.

- **RUN apt update && apt install -y curl**
  - Updates package lists.
  - Installs the `curl` package.

- **CMD ["bash"]**
  - Starts the Bash shell when a container is launched.

---

## ⚡ Commands Used

### Create Project Directory

```
mkdir docker
cd docker
```

---

### Create Dockerfile

```
notepad Dockerfile
```

Created the Dockerfile containing the required instructions.

---

### Rename Dockerfile

```
Rename-Item Dockerfile.txt Dockerfile
```

Converted the text file into a valid Dockerfile.

---

### Build Docker Image

```
docker build -t my-first-image .
```

Builds a custom Docker image from the Dockerfile.

---

### View Docker Images

```
docker images
```

Verified that the custom image was successfully created.

---

### Run the Image

```
docker run -it my-first-image
```

Started an interactive Ubuntu container.

---

### Verify Installed Package

```
curl --version
```

Confirmed that **curl** was successfully installed during the image build.

---

### Exit Container

```
exit
```

Exited the running container.

---

### Inspect Image Metadata

```
docker inspect my-first-image
```

Displayed detailed information including:

- Image ID
- Repository Tags
- Environment Variables
- Architecture
- Operating System
- Layers
- Metadata

---

## 🧪 What I Practised

- Created a new Docker project directory.
- Created and configured a Dockerfile.
- Built a custom Docker image.
- Listed available Docker images.
- Ran an interactive container.
- Verified installed software using `curl --version`.
- Inspected image metadata using Docker Inspect.
- Understood Dockerfile instructions.

---

## 📸 Screenshots

### Screenshot 1 – Creating Dockerfile

- Created project directory.
- Created Dockerfile.
- Renamed Dockerfile correctly.

---

### Screenshot 2 – Building Docker Image

- Successfully built the custom image.
- Verified image using `docker images`.
- Started an interactive container.

---

### Screenshot 3 – Inspecting Image

- Displayed image metadata.
- Verified environment variables.
- Reviewed repository information.

---

### Screenshot 4 – Image Details

- Examined architecture.
- Reviewed image layers.
- Checked image descriptor information.

---

### Screenshot 5 – Dockerfile Content

Displayed the Dockerfile used to create the custom image.

---

## 🔒 Key Learning

A Dockerfile is a text file containing instructions used to build custom Docker images. Each instruction creates a new image layer, making Docker builds efficient through caching. Using Dockerfiles allows developers to create consistent, portable, and reusable environments.

---

## 🎯 Skills Practiced

- Dockerfile Creation
- Docker Image Building
- Docker Image Inspection
- Ubuntu Containers
- Package Installation
- Docker CLI
- Container Execution
- Custom Image Creation

---

## ✅ Outcome

Successfully created a custom Docker image from a Dockerfile, installed software during the build process, launched an interactive container, verified the installed package, and inspected the image metadata. This provides a solid foundation for creating reusable Docker images for development and deployment.
