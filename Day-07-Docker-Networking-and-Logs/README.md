# 🐳 Day 7 – Docker Networking and Container Logs

## 📌 Objective

Learn how Docker maps container ports to the host machine, monitor container logs, follow live log output, inspect port mappings, and verify open network ports.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Windows PowerShell
- Nginx Docker Image
- Windows Netstat

---

## 📚 Concepts Learned

- Docker Port Mapping
- Container Networking
- Container Logs
- Live Log Monitoring
- Docker Port Inspection
- Host-to-Container Communication
- Network Verification

---

## ⚡ Commands Used

### List Running Containers

```
docker ps
```

Displays all running Docker containers along with their IDs, images, status, and exposed ports.

---

### Stop a Running Container

```
docker stop <container-id>
```

Stops a running Docker container.

Example:

```
docker stop 2b72c3c6f8c2
```

---

### Remove a Container

```
docker rm <container-id>
```

Deletes a stopped container.

Example:

```
docker rm 2b72c3c6f8c2
```

---

### Run an Nginx Container on a Custom Port

```
docker run -d -p 8084:80 nginx
```

Starts an Nginx container in detached mode and maps:

- Host Port → **8084**
- Container Port → **80**

---

### View Running Containers

```
docker ps
```

Confirms the container is running and verifies the port mapping.

---

### View Container Logs

```
docker logs <container-id>
```

Displays startup logs and initialisation messages from the container.

Example:

```
docker logs 5ba83b115744
```

---

### View Port Mapping

```
docker port <container-id>
```

Shows which host port is mapped to the container port.

Example:

```
docker port 5ba83b115744
```

Output:

```
80/tcp -> 0.0.0.0:8084
80/tcp -> [::]:8084
```

---

### Follow Logs in Real Time

```
docker logs -f <container-id>
```

Continuously streams container logs until interrupted.

Example:

```
docker logs -f 5ba83b115744
```

---

### Verify Open Port on Windows

```
netstat -ano | findstr :8084
```

Checks whether the mapped port is listening on the host machine.

---

## 🧪 What I Practised

- Listed running Docker containers.
- Stopped and removed an existing container.
- Created a new Nginx container with custom port mapping.
- Verified container status using `docker ps`.
- Viewed startup logs.
- Followed live logs using `docker logs -f`.
- Inspected Docker port mappings.
- Verified the host port using `netstat`.
- Observed HTTP requests appearing in the container logs.

---

## 📸 Screenshots

### Screenshot 1 – Managing Containers

- Listed running containers.
- Stopped and removed a container.
- Started a new Nginx container on port **8084**.

---

### Screenshot 2 – Viewing Container Logs

- Displayed Nginx startup logs.
- Verified successful server initialisation.
- Checked Docker port mapping.

---

### Screenshot 3 – Live Log Monitoring

- Followed container logs in real time.
- Observed HTTP requests generated from the browser.
- Noticed a missing `favicon.ico` request, which is a normal browser behaviour.

---

### Screenshot 4 – Verifying Network Port

- Used `netstat` to confirm port **8084** is actively listening.
- Verified successful communication between the host machine and the Docker container.

---

## 🔒 Key Learning

Docker enables applications inside containers to be accessed from the host system using port mapping.

Container logs provide valuable information for:

- Monitoring application startup
- Debugging issues
- Tracking incoming requests
- Troubleshooting container behaviour

The `docker logs -f` command is especially useful for observing live application activity.

---

## 🎯 Skills Practiced

- Docker Networking
- Port Mapping
- Container Monitoring
- Docker Logs
- Live Log Streaming
- Network Verification
- Windows Networking Tools
- Docker CLI

---

## ✅ Outcome

Successfully learned how to expose Docker containers using port mapping, inspect and monitor container logs, stream logs in real time, verify host-to-container communication, and validate open ports using Windows networking tools. These skills are essential for Docker administration, DevOps, cloud deployments, and troubleshooting containerised applications.
