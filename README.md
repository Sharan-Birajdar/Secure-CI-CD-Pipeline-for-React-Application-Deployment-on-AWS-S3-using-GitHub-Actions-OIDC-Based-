<<<<<<< HEAD
# 🚀 Secure CI/CD Pipeline for React Deployment on AWS S3 AS Static Website

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

=======
# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
>>>>>>> c777dc2 (Initial commit)
