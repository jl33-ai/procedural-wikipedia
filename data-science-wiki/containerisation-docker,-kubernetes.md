**Created by @jl33-ai 👦🏻**

---

## Table of Contents 

- [Introduction](#introduction)
- [What is Containerisation?](#what-is-containerisation)
- [What is Docker?](#what-is-docker)
- [What is Kubernetes?](#what-is-kubernetes)
- [Docker vs Kubernetes](#docker-vs-kubernetes)
- [Examples](#examples)

---

## Introduction <a name = "introduction"></a>

This document provides a brief overview of containerization with Docker and Kubernetes. It includes how these tools can be used to unravel the potential of containers and understand the difference between Docker and Kubernetes.

---

## What is Containerisation? <a name = "what-is-containerisation"></a>

- Containerisation is a lightweight, virtualized system at the OS level.
- It neatly packages up your application and all its dependencies to make sure it works seamlessly in any environment.
- This technology can visualise your entire software, applications, and services in a neat way. 

---

## What is Docker? 🐳 <a name = "what-is-docker"></a>

- Docker is an open-source platform that automates deploying, scaling, and running applications.
- It separates applications from infrastructure so you can deliver software quickly.
- Docker containers are lightweight and can run directly within the host machine's kernel, which makes it much more efficient than VMs.
- Dockerfile defines what goes on in the environment inside your container.
- Docker Compose allows you to use a YAML file to define multi-container applications.

```docker
# Sample Dockerfile
FROM node:10    
WORKDIR /usr/src/app    
COPY package*.json ./    
RUN npm install    
COPY . .    
EXPOSE 8080    
CMD [ "npm", "start" ]
```

---

## What is Kubernetes? ⚙️ <a name = "what-is-kubernetes"></a>

- Kubernetes, or K8s, is an open-source platform used to automate the deployment, scaling, and management of containerised applications.
- It groups containers together, which makes managing and discovering these services very easy, particularly in large and complex operational environments.
- Kubernetes coordinates a highly available cluster of computers to work as a single unit and provides desired state management to keep the environment consistent.

```yaml
# Sample Kubernetes Deployment 
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
```

---

## Docker vs Kubernetes <a name = "docker-vs-kubernetes"></a>

- Docker and Kubernetes are not exactly competitors. Docker is all about creating, running and managing containers, whereas Kubernetes is about managing clusters of distributed containers.
- Docker is excellent for local development while Kubernetes is perfect for scaling and distributing applications across clusters.
- Docker Swarm is Docker's orchestration solution, which has a much smaller market share than Kubernetes.

---

## Examples 📝 <a name = "examples"></a>

- You can run a simple hello world app in Docker with a Dockerfile like this:

```docker
# Use an official Python runtime as a parent image
FROM python:2.7-slim
# Set the working directory to /app
WORKDIR /app
# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt
# Make port 80 available to the world outside this container
EXPOSE 80
# Run app.py when the container launches
CMD ["python", "app.py"]
```
 
- You can run the same app in Kubernetes with a deployment like this:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: hello-pod
spec:
  containers:
  - name: hello-container
    image: my-python-app
    ports:
    - containerPort: 80
```

---

> To sum up, both Docker 🐳 and Kubernetes ⚙️ are powerful tools for modern software delivery processes. Docker allows for efficient application packaging while Kubernetes plays its strengths in managing complex container architectures.
