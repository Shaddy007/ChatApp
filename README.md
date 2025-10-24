# Chat Application on Kubernetes

This repository contains a full-stack chat application deployed on Kubernetes. It includes:

- **Frontend:** Vite-based UI
- **Backend:** Node.js server
- **Database:** MongoDB
- **Admin Panel:** Mongo Express

## Deployment Namespace
All resources are deployed under the Kubernetes namespace: `shaddy`.

## Kubernetes Setup
- YAML manifests are provided for all components:
  - MongoDB & Service
  - Mongo Express & Service
  - Backend & Service
  - Frontend & Service
- Optional Ingress configuration can be used to expose services.

## How to Run Locally
1. Start a local Kubernetes cluster (e.g., Minikube with Docker driver).
2. Apply all manifests:
   ```bash
   kubectl apply -f .
