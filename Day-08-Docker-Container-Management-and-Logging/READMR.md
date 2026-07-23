# 🐳 Day 8 – Docker Container Management and Logging

## 📌 Objective

Learn how to manage Docker containers by assigning custom names, inspecting running containers, viewing container logs, following logs in real time, checking port mappings, and verifying active network ports.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Windows PowerShell
- Nginx Docker Image
- Windows Netstat

---

## 📚 Concepts Learned

- Creating Named Containers
- Detached Mode Containers
- Docker Port Mapping
- Container Logs
- Live Log Monitoring
- Docker Networking
- Host-to-Container Communication

---

## ⚡ Commands Used

### Pull the Latest Nginx Image

```
docker pull nginx
```

Downloads the latest Nginx image from Docker Hub.

---

### Run a Named Container

```
docker run -d -p 8080:80 --name myweb nginx
```

Options used:

- `-d` → Runs the container in detached mode.
- `-p 8080:80` → Maps host port 8080 to container port 80.
- `--name myweb` → Assigns the custom name **myweb**.

---

### View Running Containers

```
docker ps
```

Lists all running containers and displays:

- Container ID
- Image
- Status
- Port Mapping
- Container Name

---

### Inspect Port Mapping

```
docker port <container-id>
```

Example:

```
docker port d34fdbb3764d
```

Output:

```
80/tcp -> 0.0.0.0:8080
80/tcp -> [::]:8080
```

---

### View Container Logs

```
docker logs <container-id>
```

Displays container startup messages and application logs.

Example:

```
docker logs d34fdbb3764d
```

---

### Follow Logs in Real Time

```
docker logs -f <container-id>
```

Continuously streams live logs from the running container until interrupted.

Example:

```
docker logs -f d34fdbb3764d
```

---

### Verify Open Network Port

```
netstat -ano | findstr :8080
```

Confirms that the mapped port is actively listening on the Windows host.

---

## 🧪 What I Practised

- Pulled the latest Nginx image.
- Created a container with a custom name.
- Mapped host port **8080** to container port **80**.
- Verified the running container using `docker ps`.
- Checked Docker port mappings.
- Viewed startup logs.
- Followed logs in real time.
- Observed browser HTTP requests in the logs.
- Verified network connectivity using `netstat`.

---

## 📸 Screenshots

### Screenshot 1 – Creating a Named Container

- Pulled the latest Nginx image.
- Started a new container named **myweb**.
- Verified the running container with `docker ps`.

---

### Screenshot 2 – Viewing Container Logs

- Displayed Nginx startup logs.
- Observed server initialisation messages.
- Noticed the browser requesting `favicon.ico`, resulting in a normal **404** response.

---

### Screenshot 3 – Live Log Monitoring

- Used `docker logs -f` to stream logs.
- Observed incoming browser requests in real time.
- Verified that the web server responded successfully.

---

### Screenshot 4 – Network Verification

- Used `netstat` to verify port **8080**.
- Confirmed the port was listening.
- Observed active and established TCP connections between the browser and the container.

---

## 🔒 Key Learning

Giving containers meaningful names makes them easier to manage compared to using container IDs.

The `docker logs` command helps monitor application behaviour, while `docker logs -f` provides live log streaming for troubleshooting and debugging.

The `docker port` and `netstat` commands are useful for verifying that Docker port mappings are working correctly and that the application is accessible from the host machine.

---

## 🎯 Skills Practiced

- Docker Container Management
- Named Containers
- Docker Networking
- Port Mapping
- Container Logs
- Live Log Monitoring
- Network Verification
- Docker CLI
- Windows Networking Tools

---

## ✅ Outcome

Successfully created and managed a named Docker container, verified port mappings, monitored application logs, streamed live container logs, and confirmed network connectivity using Windows networking tools. These are essential skills for Docker administration, DevOps workflows, cloud deployments, and troubleshooting containerised applications.
