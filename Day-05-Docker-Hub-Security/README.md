# 🔒 Day 5 – Docker Hub Security

## 📌 Objective

Learn Docker image security by downloading trusted images, inspecting image metadata, scanning images for vulnerabilities using Trivy, comparing official and community images, and safely removing unused images.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Windows PowerShell
- Docker Hub
- Trivy
- Nginx
- Bitnami Nginx

---

## 📚 Concepts Learned

- Docker Hub
- Official Images
- Community Images
- Image Inspection
- Image Metadata
- Vulnerability Scanning
- CVEs
- Docker Image Security
- Secure Image Management

---

## ⚡ Commands Used

### Pull the Official Nginx Image

```
docker pull nginx
```

Downloads the official Nginx image from Docker Hub.

---

### Pull a Community Image

```
docker pull bitnami/nginx
```

Downloads the Bitnami community-maintained Nginx image.

---

### List Local Images

```
docker images
```

Displays all Docker images stored locally.

---

### Inspect Image Metadata

```
docker image inspect nginx
```

Displays detailed image information including:

- Image ID
- Repository Tags
- Environment Variables
- Labels
- Entrypoint
- Operating System
- Architecture

---

### Scan Official Image

```
trivy image nginx
```

Scans the official Nginx image for vulnerabilities.

---

### Scan Community Image

```
trivy image bitnami/nginx
```

Scans the Bitnami Nginx image for vulnerabilities.

---

### Remove an Unused Image

```
docker rmi bitnami/nginx
```

Deletes the Bitnami Nginx image after verification.

---

## 🧪 What I Practised

- Pulled official Docker images.
- Pulled community Docker images.
- Compared image sizes.
- Inspected Docker image metadata.
- Examined environment variables and image configuration.
- Scanned images using Trivy.
- Reviewed vulnerability reports.
- Removed an unused Docker image.

---

## 📸 Screenshots

### Downloading Docker Images

- Pulled the official Nginx image.
- Pulled the Bitnami Nginx image.
- Listed all local Docker images.

---

### Inspecting the Official Image

- Viewed image metadata.
- Checked environment variables.
- Reviewed labels and entrypoint.
- Verified operating system and architecture.

---

### Trivy Scan (Official Nginx)

- Performed a vulnerability scan.
- Reviewed vulnerability summary.
- Identified HIGH and CRITICAL security findings.

---

### Trivy Scan (Bitnami Nginx)

- Compared scan results with the official image.
- Observed significantly fewer vulnerabilities.

---

### Vulnerability Details

- Reviewed CVE information.
- Examined affected packages.
- Checked installed and fixed versions.

---

### Image Cleanup

- Successfully removed the unused Bitnami Nginx image.
- Verified safe image management.

---

## 🔒 Security Best Practices Learned

- Use official or trusted Docker images.
- Verify image metadata before deployment.
- Scan images regularly with Trivy.
- Review CVEs before using images in production.
- Remove unused images.
- Keep images updated.
- Avoid deploying vulnerable images.
- Compare multiple image sources before selecting one.

---

## 🎯 Skills Practiced

- Docker Hub
- Docker Image Management
- Image Inspection
- Vulnerability Assessment
- Trivy Security Scanner
- Container Security
- Security Analysis
- Docker Administration

---

## 📊 Key Observation

During testing:

- The official **Nginx** image contained significantly more reported vulnerabilities.
- The **Bitnami Nginx** image showed considerably fewer security findings.

This demonstrates why security scanning should be part of every container deployment workflow instead of assuming an image is secure.

---

## ✅ Outcome

Completed the Docker Hub Security lab by:

- Downloading trusted Docker images.
- Inspecting image metadata.
- Comparing official and community images.
- Performing vulnerability scans using Trivy.
- Reviewing CVEs and security findings.
- Safely removing unused images.

This project strengthened my understanding of Docker image security and vulnerability management, which are essential skills for Cloud Security, DevSecOps, and Container Security roles.
