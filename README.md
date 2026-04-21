# Secure-CI-CD-Pipeline-for-React-Application-Deployment-on-AWS-S3-using-GitHub-Actions-OIDC-Based-

# 🚀 Secure CI/CD Pipeline for React Deployment on AWS S3

## 📌 Project Overview

This project demonstrates an end-to-end **CI/CD pipeline** for deploying a React application to **Amazon S3** using **GitHub Actions** with secure **OIDC-based authentication**.

The pipeline automatically builds and deploys the application whenever code is pushed to the `main` branch.

---

## 🏗️ Architecture

* Frontend: React.js
* CI/CD: GitHub Actions
* Cloud Storage & Hosting: AWS S3 (Static Website Hosting)
* Authentication: OIDC (OpenID Connect) via IAM Role
* Deployment Tool: AWS CLI

---

## ⚙️ Features

* ✅ Automated build and deployment
* 🔐 Secure authentication (No AWS access keys used)
* 📦 Optimized production build
* 🔄 Sync deployment with cleanup (`--delete`)
* 🌐 Static website hosting on S3

---

## 📁 Project Structure

```
.
├── public/
├── src/
├── build/        # Generated after build
├── package.json
└── .github/workflows/deploy.yml
```

---

## 🚀 CI/CD Workflow

### Trigger

* Runs on push to `main` branch

### Steps

1. Checkout source code
2. Setup Node.js environment
3. Install dependencies (`npm install`)
4. Build project (`npm run build`)
5. Configure AWS credentials using OIDC
6. Deploy to S3 using:

   ```
   aws s3 sync build/ s3://YOUR_BUCKET_NAME --delete
   ```

---

## 🔐 IAM Permissions (Least Privilege)

The deployment uses a restricted IAM policy with:

* `s3:PutObject`
* `s3:DeleteObject`
* `s3:ListBucket`

This ensures secure and minimal access.

---

## 🛠️ Setup Instructions

### 1. Clone Repository

```
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. Install Dependencies

```
npm install
```

### 3. Run Locally

```
npm start
```

---

## ☁️ AWS Setup

1. Create an S3 bucket
2. Enable static website hosting
3. Set:

   * Index document: `index.html`
4. Configure bucket policy (if public access required)

---

## 🔄 Deployment

Deployment is fully automated via GitHub Actions.

On every push to `main`, the app is:

* Built
* Deployed to S3
* Synced with latest changes

---

## 📸 Output

Your application will be available via the S3 static website endpoint.

---

## 🧠 Learnings

* CI/CD pipeline implementation
* Secure AWS authentication using OIDC
* Static website hosting on S3
* Automation using GitHub Actions

---

## 🔮 Future Improvements

* Add CloudFront CDN
* Enable HTTPS with custom domain
* Implement cache invalidation
* Add monitoring & logging

---
