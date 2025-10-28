# Ostad-Docker Chat Application

## Overview
**Ostad-Docker** is a full-stack, real-time chat application that demonstrates a multi-component system using **Node.js**, **React (Vite)**, **MongoDB**, and **Mongo Express**, all deployed in **Kubernetes**.  
This project showcases containerization with Docker and orchestration with Kubernetes, making it a complete example for learning modern DevOps practices.

---

## Features

- Real-time chat messaging between multiple users.
- Persistent storage using MongoDB.
- Admin dashboard via Mongo Express.
- Frontend developed with Vite for fast development.
- Backend with Node.js and Express API.
- Kubernetes manifests for Deployment, Services, and Ingress.

---

## Project Architecture

+----------------+ +----------------+ +-------------+
| | HTTP | | TCP | |
| Frontend |------>| Backend |------>| MongoDB |
| (Vite/React) | | (Node.js API) | | Database |
| ostad-ui | | ostad-server | | mongo |
+----------------+ +----------------+ +-------------+
|
| HTTP
v
+----------------+
| Mongo Express |
| Admin Panel |
| mongo-express |
+----------------+


- **ostad-ui**: Serves the web application and communicates with the backend API.  
- **ostad-server**: Handles API requests and connects to MongoDB for storing and retrieving chat messages.  
- **mongo**: MongoDB database storing all chat data.  
- **mongo-express**: Optional admin UI for database management.

---

## Folder Structure

Ostad-Docker/
├── Dockerfile-server # Backend Dockerfile
├── Dockerfile-UI # Frontend Dockerfile
├── OstadServer/ # Node.js backend code
├── OstadUI/ # Frontend React/Vite code
├── YAMLs/ # Kubernetes manifests
├── ostad.yaml # Optional project config
└── readme.md # Project description


## Prerequisites

- Linux (Oracle Linux 10 tested)
- Docker
- Minikube (for local Kubernetes cluster)
- kubectl (Kubernetes CLI)
- Git

## Notes

All Kubernetes resources are inside the YAMLs/ folder.

You can change namespace name if required.

This project demonstrates Kubernetes Deployments, Services, and Ingress configuration for multi-component apps.
