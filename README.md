# 🚀 Static Website Hosting on AWS (S3 + CloudFront + ACM + Namecheap DNS)

## 👨‍💻 Author

Akshaykumar Patil
Aspiring Cloud Architect | AWS and DevOps Enthusiast

---

## 📌 Project Overview

This project demonstrates how to deploy a **secure, scalable, and highly available static website** using AWS cloud-native services and external DNS management.

The website is hosted on **Amazon S3**, distributed globally via **Amazon CloudFront**, secured using **AWS Certificate Manager (ACM)**, and connected to a custom domain managed through **Namecheap DNS**.

This project reflects real-world cloud architecture practices including CDN optimization, HTTPS enforcement, and secure origin access.

---

## 🏗 Architecture Diagram

![Architecture Diagram](architecture/architecture-diagram.png)

### Architecture Flow

User → DNS (Namecheap) → CloudFront CDN → S3 Origin
                ↑
               ACM SSL Certificate

---

## 🧰 Technologies Used

* Amazon S3 — Static Website Storage
* Amazon CloudFront — Content Delivery Network (CDN)
* AWS Certificate Manager (ACM) — SSL/TLS Certificate
* Namecheap — Domain & DNS Management
* HTML / CSS — Website Content

---

## ✨ Key Features

* 🌍 Global content delivery using CDN
* 🔐 HTTPS enabled with SSL certificate
* 🌐 Custom domain integration
* 🚫 Private S3 bucket (no public exposure)
* ⚡ Improved performance via caching
* 💰 Low-cost serverless architecture

---

## 📂 Repository Structure

```
static-website-aws/
│
├── website/              # Static website files
├── architecture/         # Architecture diagram & explanation
├── infrastructure/       # Deployment documentation
├── security/             # Security configurations
├── troubleshooting/      # Common issues & fixes
└── screenshots/          # Deployment proof
```

---

## 🚀 Deployment Steps

### 1️⃣ Create S3 Bucket

* Create S3 bucket
* Disable public access
* Upload static website files
* Configure bucket for static hosting

👉 Detailed Guide: `infrastructure/s3-config.md`

---

### 2️⃣ Request SSL Certificate (ACM)

* Request certificate in **us-east-1**
* Add domain name
* Validate ownership via DNS

👉 Guide: `infrastructure/acm-config.md`

---

### 3️⃣ Configure CloudFront Distribution

* Origin → S3 bucket
* Enable HTTPS redirect
* Attach ACM certificate
* Configure default root object

👉 Guide: `infrastructure/cloudfront-config.md`

---

### 4️⃣ Configure Namecheap DNS

Add DNS records pointing domain to CloudFront distribution.

👉 Guide: `infrastructure/dns-config.md`

---

## 🔐 Security Implementation

* S3 public access blocked
* CloudFront Origin Access Control (OAC)
* HTTPS enforced
* TLS encryption via ACM
* Principle of Least Privilege applied

See: `security/security-best-practices.md`

---

## 📸 Screenshots

Deployment proof:

* S3 Bucket Configuration
* CloudFront Distribution
* ACM Certificate Validation
* DNS Records
* HTTPS Website Working

Location: `/screenshots`

---

## 🌐 Live Demo

👉 https://shayverse.space

---

## 💰 Cost Estimation

Approximate monthly cost (low traffic):

| Service       | Estimated Cost |
| ------------- | -------------- |
| S3 Storage    | ~$0.50         |
| CloudFront    | ~$1            |
| ACM           | Free           |
| Data Transfer | Minimal        |

**Total:** ~$1–3/month

---

## 📈 Performance Optimization

* CloudFront edge caching reduces latency
* Static assets cached globally
* Reduced origin requests to S3

---

## 🧠 Key Learnings

* Understanding CDN architecture
* DNS propagation behavior
* SSL certificate validation process
* Secure S3 access using CloudFront
* Importance of regional services (ACM in us-east-1)

---

## ⚠️ Challenges Faced

* DNS propagation delays
* HTTPS configuration troubleshooting
* CloudFront cache invalidation behavior

---

## 🚀 Future Improvements

* CI/CD deployment using GitHub Actions
* Infrastructure as Code (Terraform)
* AWS WAF integration
* Route53 migration
* Automated cache invalidation

---

## 📚 References

* AWS Documentation
* Cloud Architecture Best Practices
* AWS Well-Architected Framework

---

## ⭐ Why This Project Matters

This project demonstrates foundational cloud architecture concepts:

* Serverless design
* High availability
* Secure access patterns
* Global scalability
* Cost optimization

---

## 🤝 Connect With Me

GitHub: https://github.com/shayvers

---

⭐ If you found this useful, feel free to star the repository!
