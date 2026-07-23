# 🐳 Day 2 – Running First Containers

## 📌 Objective

Learn how to run, inspect, manage, and remove Docker containers using the Docker CLI. This lab covers creating temporary containers, interacting with an Ubuntu container, and managing the container lifecycle.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Windows PowerShell
- Ubuntu
- Hello-World Image

---

## 📚 Concepts Learned

- Running Docker containers
- Hello World container
- Interactive containers
- Docker Hub image download
- Viewing running containers
- Viewing stopped containers
- Container lifecycle
- Removing containers

---

## ⚡ Commands Used

### Run the Hello World Container

```
docker run hello-world
```

Downloads the image (if not available locally), creates a container, displays a welcome message, and exits automatically.

---

### View Running Containers

```
docker ps
```

Displays all currently running containers.

---

### View All Containers

```
docker ps -a
```

Displays both running and stopped containers.

---

### Run an Interactive Ubuntu Container

```
docker run -it ubuntu bash
```

Downloads the Ubuntu image (if required) and opens an interactive Bash shell inside the container.

---

### Explore the Container

```
pwd
ls
whoami
uname -a
cat /etc/os-release
```

These commands were used to inspect the Ubuntu container environment.

---

### Exit the Container

```
exit
```

Stops the running Ubuntu container.

---

### Remove the Ubuntu Container

```
docker rm <container_id>
```

Deletes the stopped Ubuntu container.

---

## 🧪 What I Practised

- Ran the `hello-world` container successfully.
- Verified Docker installation.
- Pulled the Ubuntu image automatically.
- Entered an interactive Ubuntu container.
- Explored the Linux filesystem.
- Checked the current user and operating system details.
- Exited the container safely.
- Viewed running and stopped containers.
- Removed the stopped Ubuntu container.

---

## 📸 Screenshots

### 1. Running the Hello World Container

- Successfully executed the `hello-world` container.
- Verified that Docker is working correctly.

---

### 2. Viewing Containers

- Listed running containers using `docker ps`.
- Listed all containers using `docker ps -a`.

---

### 3. Exploring the Ubuntu Container

Executed the following Linux commands:

- `pwd`
- `ls`
- `whoami`
- `uname -a`
- `cat /etc/os-release`

Verified that the container was running Ubuntu Linux.

---

### 4. Container Cleanup

- Exited the Ubuntu container.
- Removed the stopped Ubuntu container.
- Verified the cleanup using `docker ps -a`.

---

## 🔒 Security Notes

- Used official Docker Hub images (`hello-world` and `ubuntu`).
- Temporary containers were removed after testing.
- Verified container status before deletion.
- Practised good container housekeeping by removing unused containers.

---

## 🎯 Skills Practiced

- Docker CLI
- Interactive Containers
- Linux Commands
- Docker Images
- Container Lifecycle Management
- Docker Cleanup
- Ubuntu Basics

---

## ✅ Outcome

Completed the Day 2 Docker lab by:

- Running the Hello World container.
- Launching an interactive Ubuntu container.
- Exploring the Linux environment inside Docker.
- Managing running and stopped containers.
- Removing unused containers.

This lab strengthened my understanding of Docker container management and basic Linux administration, which are essential skills for Cloud and DevOps environments.

---

## 🚀 Next Step

Continue with **Day 3 – Docker Images & Docker Hub**, where I will learn how to inspect, manage, and secure Docker images.
