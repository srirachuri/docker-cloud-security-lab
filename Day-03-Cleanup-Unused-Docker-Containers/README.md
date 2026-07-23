# 🧹 Day 3 Cleaning Up Unused Docker Containers

## 📌 Objective

Learn how to identify, remove, and verify unused Docker containers to keep the Docker environment clean and organized.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Windows PowerShell
- Nginx
- Ubuntu
- Hello World Image

---

## 📚 Concepts Learned

- Running containers
- Stopped containers
- Container IDs
- Removing containers
- Docker cleanup
- Container lifecycle management

---

## ⚡ Commands Used

### View All Containers

```
docker ps -a
```

Displays both running and stopped containers.

---

### Remove a Single Container

```
docker rm <container_id>
```

Example:

```
docker rm 6bc9525a069a
```

---

### Remove Multiple Containers

```
docker rm <container_id1> <container_id2>
```

Example:

```
docker rm c0728898b2ec a1b101057bea
```

---

### Verify Cleanup

```
docker ps -a
```

Confirms that only the required containers remain.

---

## 🧪 What I Practiced

- Listed all Docker containers.
- Identified stopped Ubuntu and Hello World containers.
- Removed unnecessary stopped containers.
- Removed multiple containers using a single command.
- Verified the cleanup process.
- Confirmed that running Nginx containers were not affected.

---

## 📸 Screenshots

### 1. Removing Stopped Containers

The screenshot demonstrates:

- Viewing all Docker containers.
- Removing stopped Ubuntu and Hello World containers.
- Removing multiple containers using the `docker rm` command.

---

### 2. Verifying Cleanup

The screenshot shows:

- Successfully removed unused containers.
- Verified that only active Nginx containers remained.
- Confirmed the Docker environment was clean and organised.

---

## 🔒 Security Notes

- Removed only stopped containers.
- Verified container status before deletion.
- Left running containers untouched.
- Practised safe Docker cleanup procedures.
- Reduced unnecessary resource usage by deleting unused containers.

---

## 🎯 Skills Practiced

- Docker CLI
- Container Lifecycle Management
- Docker Cleanup
- Container Administration
- Basic Docker Operations
- Cloud Infrastructure Maintenance

---

## ✅ Outcome

Completed the Docker cleanup exercise by:

- Identifying stopped containers.
- Removing single and multiple unused containers.
- Verifying cleanup using Docker CLI.
- Keeping the Docker environment clean and organised.

This exercise demonstrates good Docker housekeeping practices, an important skill for Cloud Engineers, DevOps Engineers, and Cloud Security professionals.
