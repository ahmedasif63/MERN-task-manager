# MERN Task Manager – Containerized with CI/CD

## Project Overview

This project is a **MERN Task Manager application** that has been fully containerized using **Docker** and integrated with a **CI/CD pipeline using GitHub Actions**. The goal of this project is to demonstrate practical implementation of **containerization, version control collaboration, and automated pipelines** as part of our semester DevOps project.

The application consists of:

* **Frontend**: React
* **Backend**: Node.js + Express
* **Database**: MongoDB

All services are orchestrated using **Docker Compose**, and the build + image publishing process is automated using **GitHub Actions CI/CD pipeline**.


## Team Information

| Name              | Registration Number |
| ----------------- | ------------------- |
| Ahmed Asif        | F2023-624           |
| Mirsab Ahmed khan | F2023-468           |



## Project Objectives

* Understand and implement **Docker containerization** for a multi-service MERN application
* Implement **CI/CD pipeline** using GitHub Actions
* Automate:

  * Dependency installation
  * Frontend build
  * Docker image build
  * Docker image push to DockerHub
* Practice **Git collaboration workflow** using branches and merges


## Containerization Approach

We containerized each component separately:

### 1. Backend Container

* Node.js base image
* Installs dependencies
* Exposes port **5000**
* Connects to MongoDB using environment variables

### 2. Frontend Container

* Node.js base image
* Builds React application
* Exposes port **3000**

### 3. MongoDB Container

* Official MongoDB image
* Uses **Docker volumes** for persistent data storage

### 4. Docker Compose

All services are orchestrated using `docker-compose.yml`:

* frontend
* backend
* mongo

This allows the entire system to be started with a single command:

```
docker compose up --build
```



## CI/CD Pipeline

We implemented a **GitHub Actions CI/CD pipeline** that runs automatically on every push or pull request to the `main` or `dev` branch.

### CI (Continuous Integration)

* Checkout code
* Setup Node.js
* Install backend dependencies
* Install frontend dependencies
* Build frontend

### CD (Continuous Delivery)

* Setup Docker Buildx
* Login to DockerHub using GitHub Secrets
* Build backend Docker image
* Push backend image to DockerHub
* Build frontend Docker image
* Push frontend image to DockerHub

This ensures that every code change is automatically built and converted into Docker images without manual intervention.



## Technologies Used

* Node.js
* Express.js
* React
* MongoDB
* Docker
* Docker Compose
* GitHub Actions
* Git & GitHub



## How to Run the Project Locally

1. Clone the repository
2. Navigate to the project root
3. Run:

```
docker compose up --build
```

4. Open browser:

   * Frontend: [http://localhost:3000](http://localhost:3000)
   * Backend: [http://localhost:5000](http://localhost:5000)



## Learning Outcomes

Through this project, we learned:

* Real-world Docker containerization
* Multi-service orchestration with Docker Compose
* CI/CD pipeline creation using GitHub Actions
* Docker image publishing to DockerHub
* Git branching, merging, and collaboration workflows



## Notes

* This project focuses on **Containerization + CI/CD** only.
* No cloud deployment or Kubernetes is included in this scope as per project requirements.



## Acknowledgment

This project was developed as part of our **Semester DevOps Project** to gain hands-on experience with modern DevOps tools and practices.