# Ostad-Docker Chat Application

## Overview
**Ostad-Docker** is a full-stack, real-time chat application demonstrating a multi-component system using:  

- **Node.js** (Backend API)  
- **React (Vite)** (Frontend)  
- **MongoDB** (Database)  
- **Mongo Express** (Admin Dashboard)  

The application is fully containerized using **Docker** and orchestrated with **Kubernetes**, making it an ideal project for learning modern **DevOps** practices.

---

## Features

- Real-time chat between multiple users.  
- Persistent storage with MongoDB.  
- Admin dashboard using Mongo Express.  
- Fast frontend development with **Vite** and React.  
- RESTful API backend with **Node.js** and Express.  
- Kubernetes manifests for Deployments, Services, and Ingress.  

---

## Project Architecture

```text
+----------------+       +----------------+       +-------------+
|   Frontend     | HTTP  |    Backend     | TCP   |   MongoDB   |
|  (Vite/React)  |------>|  (Node.js API) |------>|   Database  |
|    ostad-ui    |       |  ostad-server  |       |    mongo    |
+----------------+       +----------------+       +-------------+
        |
        | HTTP
        v
+----------------+
| Mongo Express  |
| Admin Panel    |
| mongo-express  |
+----------------+


- **ostad-ui**: Serves the web application and communicates with the backend API.  
- **ostad-server**: Handles API requests and connects to MongoDB for storing and retrieving chat messages.  
- **mongo**: MongoDB database storing all chat data.  
- **mongo-express**: Optional admin UI for database management.

---

## Folder Structure


Ostad-Docker/
├── Dockerfile-server       # Backend Dockerfile
├── Dockerfile-UI           # Frontend Dockerfile
├── OstadServer/            # Node.js backend code
├── OstadUI/                # Frontend React/Vite code
├── YAMLs/                  # Kubernetes manifests
├── ostad.yaml              # Optional project config
└── README.md               # Project description


## Prerequisites

- Linux (Oracle Linux 10 tested)
- Docker
- Minikube (for local Kubernetes cluster)
- kubectl (Kubernetes CLI)
- Git


## Notes

- All Kubernetes manifests are inside the YAMLs/ folder.
- You can modify the namespace and other configurations as needed.
- Demonstrates Deployments, Services, and Ingress for multi-component applications.
