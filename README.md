# Angular Frontend

## Overview

This repository contains the Angular frontend application used in the CI/CD and GitOps project.

## Technology Stack

- Angular
- Node.js
- NPM
- Docker
- Kubernetes
- Tekton
- Kaniko

## CI Pipeline

The Angular Tekton pipeline performs the following steps:

1. Clone Repository
2. Install Dependencies
3. Build Angular Application
4. Build Docker Image using Kaniko
5. Push Image to Docker Hub

## Docker

Build image

```bash
docker build -t kafzal28/angular-frontend:v2 .
```

Run container

```bash
docker run -p 80:80 kafzal28/angular-frontend:v2
```

## Kubernetes

```bash
kubectl apply -f kubernetes/
```

## Verify

```bash
kubectl get pods
kubectl get deployment
```
