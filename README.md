# 🚀 End-to-End CI/CD Pipeline using Jenkins, Docker, GitHub & Docker Hub

## 📌 Project Overview

This project demonstrates an **End-to-End Continuous Integration and Continuous Deployment (CI/CD) Pipeline** for a React.js application using **Jenkins, Docker, GitHub, Docker Hub, and AWS EC2**.

The application source code is hosted on GitHub. Jenkins automatically clones the repository, builds a Docker image, runs the application inside a Docker container, and pushes the Docker image to Docker Hub.

---

## 🛠️ Technologies Used

- ⚛️ React.js
- 🐙 Git
- 📂 GitHub
- 🤖 Jenkins
- 🐳 Docker
- 📦 Docker Hub
- ☁️ AWS EC2 (Ubuntu)

---

## 📂 Project Architecture

```text
                 Developer
                     │
                     ▼
            GitHub Repository
                     │
                     ▼
              Jenkins Pipeline
                     │
     ┌───────────────┼────────────────┐
     │               │                │
     ▼               ▼                ▼
 Clone Code    Build Docker Image   Run Container
                     │
                     ▼
          Push Image to Docker Hub
                     │
                     ▼
               Docker Hub Repository
```

---

# ⚙️ CI/CD Pipeline Workflow

## 1️⃣ Clone Source Code

Jenkins automatically clones the latest source code from GitHub.

```bash
git clone https://github.com/gauriwaydande/End-to-end-CI-CD-pipeline-project.git
```

---

## 2️⃣ Build Docker Image

```bash
docker build -t react-cicd-app .
```

---

## 3️⃣ Run Docker Container

```bash
docker run -d -p 7000:80 react-cicd-app
```

Application URL:

```
http://<EC2-PUBLIC-IP>:7000
```

---

## 4️⃣ Push Docker Image to Docker Hub

```bash
docker tag react-cicd-app gauriwaydande/react-cicd-app:latest

docker push gauriwaydande/react-cicd-app:latest
```

---

# 📁 Project Structure

```text
.
├── public/
├── src/
├── Dockerfile
├── Jenkinsfile
├── package.json
├── package-lock.json
└── README.md
```

---

# ☁️ AWS EC2 Setup

Ubuntu EC2 Instance was used to host Jenkins and Docker.

### Installed Software

- Java
- Jenkins
- Docker
- Git

---

# ▶️ Running the Project Locally

### Clone Repository

```bash
git clone https://github.com/gauriwaydande/End-to-end-CI-CD-pipeline-project.git
```

### Navigate to Project

```bash
cd End-to-end-CI-CD-pipeline-project
```

### Install Dependencies

```bash
npm install
```

### Start Application

```bash
npm start
```

Open:

```
http://localhost:3000
```

---

# 🐳 Docker Commands

### Build Image

```bash
docker build -t react-cicd-app .
```

### Run Container

```bash
docker run -d -p 3000:80 react-cicd-app
```

### Stop Container

```bash
docker stop react-container
docker rm react-container
```

---

# 📦 Docker Hub Repository

### Docker Hub Username

```
gauriwaydande
```

### Docker Image

```
gauriwaydande/react-cicd-app:latest
```

Pull Image

```bash
docker pull gauriwaydande/react-cicd-app:latest
```

---

# 🔄 Jenkins Pipeline Stages

- ✅ Clone GitHub Repository
- ✅ Build Docker Image
- ✅ Run Docker Container
- ✅ Tag Docker Image
- ✅ Push Docker Image to Docker Hub

---

# 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Building a React.js application
- Git & GitHub Version Control
- Installing and Configuring Jenkins on AWS EC2
- Writing Jenkins Declarative Pipelines
- Building Docker Images
- Running Docker Containers
- Pushing Images to Docker Hub
- Implementing an End-to-End CI/CD Pipeline

---

# 👩‍💻 Author

## Gauri Waydande

**Cloud & DevOps Enthusiast 🚀**

### GitHub

https://github.com/gauriwaydande

### Docker Hub

https://hub.docker.com/u/gauriwaydande

---

## ⭐ Support

If you found this project helpful, please give it a ⭐ on GitHub.

---

## 📄 License

This project is licensed under the MIT License.