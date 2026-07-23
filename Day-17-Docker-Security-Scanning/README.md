# 🛡️ Day 17 – Docker Security Scanning with Trivy

## 📌 Objective

Learn how to scan Docker images for vulnerabilities using **Trivy**, identify security issues by severity, generate scan reports, and improve container security before deployment.

---

## 🛠 Technologies Used

- Docker Desktop
- Docker CLI
- Trivy
- Nginx
- Ubuntu Docker Image
- Windows PowerShell

---

## 📚 Concepts Learned

- Container Security
- Vulnerability Scanning
- CVEs (Common Vulnerabilities and Exposures)
- Image Security Assessment
- Severity Levels
- Security Reports
- Trivy Scanner
- Docker Image Analysis

---

## 🔐 Why Scan Docker Images?

Docker images may contain:

- Outdated packages
- Known vulnerabilities (CVEs)
- High-risk libraries
- Critical security flaws

Scanning images before deployment helps reduce security risks and improves container hardening.

---

# 🧰 Installing and Verifying Trivy

Verified the installed version:

```
trivy --version
```

Example output:

- Trivy Version: 0.72.0
- Vulnerability Database
- Java Database
- Database Update Information

---

# 📥 Pull Docker Image

Downloaded the latest Nginx image.

```
docker pull nginx:latest
```

---

# 🔍 Scan Nginx Image

Performed a full vulnerability scan.

```
trivy image nginx:latest
```

The scan reported:

- OS detection
- Debian packages
- Vulnerability summary
- Severity breakdown
- Installed package versions
- Fixed versions (where available)

---

# 🐳 Scan Custom Docker Image

Scanned a locally created Docker image.

```
trivy image my-first-image
```

The report included:

- Ubuntu packages
- Vulnerability count
- Gobinary analysis
- Package details
- Severity levels

---

# 📄 Save Scan Report

Saved the scan results to a text file.

```
trivy image nginx:latest > nginx-scan-report.txt
```

Useful for:

- Documentation
- Auditing
- Security reviews
- CI/CD pipelines

---

# 🚨 Scan Only High and Critical Vulnerabilities

Filtered scan output.

```
trivy image --severity HIGH,CRITICAL nginx:latest
```

This displays only the most important security findings.

---

# 🧹 Clean Up Unused Images

Removed unused Docker images.

```
docker image prune -f
```

---

# ⚡ Commands Used

## Verify Trivy

```
trivy --version
```

---

## Pull Image

```l
docker pull nginx:latest
```

---

## Scan Docker Image

```
trivy image nginx:latest
```

---

## Scan Custom Image

```
trivy image my-first-image
```

---

## Export Scan Report

```
trivy image nginx:latest > nginx-scan-report.txt
```

---

## Show Only HIGH and CRITICAL Findings

```
trivy image --severity HIGH,CRITICAL nginx:latest
```

---

## Remove Unused Images

```
docker image prune -f
```

---

# 🧪 What I Practised

- Installed and verified Trivy.
- Pulled the latest Nginx Docker image.
- Scanned official Docker images.
- Scanned a custom Docker image.
- Reviewed vulnerability reports.
- Understood severity levels.
- Generated a scan report.
- Filtered HIGH and CRITICAL vulnerabilities.
- Cleaned unused Docker images.

---

# 📸 Screenshots

### Screenshot 1

- Verified Trivy installation
- Pulled Nginx image
- Started vulnerability scan

---

### Screenshot 2

- Reviewed Nginx vulnerability report
- Examined CVE details

---

### Screenshot 3

- Scanned custom Docker image
- Reviewed Ubuntu vulnerability summary

---

### Screenshot 4

- Reviewed vulnerability details for custom image

---

### Screenshot 5

- Exported scan report
- Filtered HIGH and CRITICAL vulnerabilities

---

### Screenshot 6

- Reviewed HIGH and CRITICAL findings

---

### Screenshot 7

- Removed unused Docker images

---

# 🎯 Skills Practised

- Docker Security
- Trivy
- Vulnerability Scanning
- CVE Analysis
- Container Hardening
- Docker Image Inspection
- Security Reporting
- Risk Assessment
- Image Cleanup
- Docker CLI

---

# 📖 Key Security Concepts

## Severity Levels

- 🟢 LOW – Minor security issues
- 🟡 MEDIUM – Moderate security risks
- 🟠 HIGH – Serious vulnerabilities requiring attention
- 🔴 CRITICAL – Immediate action recommended

---

# ✅ Outcome

Successfully used **Trivy** to scan Docker images for security vulnerabilities, analysed vulnerability reports, filtered high-risk issues, exported scan results for documentation, and learned best practices for improving container security before deployment.
