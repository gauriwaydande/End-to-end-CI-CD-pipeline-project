# 🚀 End-to-End CI/CD Pipeline using Jenkins, Docker, GitHub & Docker Hub

## 📌 Project Overview

This project demonstrates an **End-to-End Continuous Integration and Continuous Deployment (CI/CD) Pipeline** for a React.js application using **Jenkins, Docker, GitHub, Docker Hub, and AWS EC2**.

The application source code is hosted on GitHub. Jenkins automatically clones the repository, builds a Docker image, runs the application inside a Docker container, and pushes the Docker image to Docker Hub whenever changes are made.

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

```
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

Jenkins clones the latest source code from the GitHub repository.

```bash
git clone https://github.com/Jiya-del302/<repository-name>.git
```

---

## 2️⃣ Build Docker Image

Jenkins builds a Docker image using the project's Dockerfile.

```bash
docker build -t react-cicd-app .
```

---

## 3️⃣ Run Docker Container

Jenkins runs the Docker container.

```bash
docker run -d -p 7000:80 react-cicd-app
```

The application becomes available at:

```
http://<EC2-PUBLIC-IP>:7000
```

---

## 4️⃣ Push Image to Docker Hub

Jenkins logs in to Docker Hub, tags the Docker image, and pushes it to your Docker Hub repository.

```bash
docker tag react-cicd-app jiyapardeshi/react-cicd-app:latest

docker push jiyapardeshi/react-cicd-app:latest
```

---

# 📁 Project Structure

```
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

An **Ubuntu EC2 Instance** was used to host Jenkins and Docker.

### Installed Software

- Java
- Jenkins
- Docker
- Git

---

# ▶️ Running the Project Locally

### Clone the Repository

```bash
git clone https://github.com/Jiya-del302/<repository-name>.git
```

### Navigate to the Project

```bash
cd <repository-name>
```

### Install Dependencies

```bash
npm install
```

### Start the React Application

```bash
npm start
```

The application will run at:

```
http://localhost:3000
```

---

# 🐳 Docker Commands

### Build Docker Image

```bash
docker build -t react-cicd-app .
```

### Run Docker Container

```bash
docker run -d -p 3000:80 react-cicd-app
```

### Stop Running Container

```bash
docker stop react-container
docker rm react-container
```

---

# 📦 Docker Hub Repository

### Docker Hub Username

```
jiyapardeshi
```

### Docker Image

```
jiyapardeshi/react-cicd-app:latest
```

Pull the image:

```bash
docker pull jiyapardeshi/react-cicd-app:latest
```

---

# 🔄 Jenkins Pipeline Stages

- ✅ Clone GitHub Repository
- ✅ Build Docker Image
- ✅ Stop Existing Container (if running)
- ✅ Run New Docker Container
- ✅ Authenticate with Docker Hub
- ✅ Push Docker Image
- ✅ Deployment Completed

---

# 📸 Pipeline Flow

```
Developer
    │
    ▼
Git Push
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins Pipeline
    │
    ├── Checkout Source Code
    ├── Build Docker Image
    ├── Run Docker Container
    ├── Tag Docker Image
    └── Push to Docker Hub
            │
            ▼
       Docker Hub
```

---

# 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Building a React.js application
- Version control using Git and GitHub
- Installing and configuring Jenkins on AWS EC2
- Writing Declarative Jenkins Pipelines
- Creating Docker images
- Running Docker containers
- Managing Docker Hub repositories
- Implementing an End-to-End CI/CD Pipeline
- Automating application deployment

---

# 👩‍💻 Author

**Jiya Pardeshi**

Cloud & DevOps Enthusiast 🚀

- GitHub: https://github.com/Jiya-del302
- Docker Hub: https://hub.docker.com/u/jiyapardeshi

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.

---

## 📄 License

This project is licensed under the MIT License.