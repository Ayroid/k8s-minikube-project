# k8s-minikube-project

This project demonstrates the setup and deployment of a Kubernetes cluster using Minikube. It includes various Kubernetes resources and configurations to help you get started with Kubernetes development and testing on your local machine.

## Table of Contents

- Introduction
- Prerequisites
- Installation
- Usage
- Project Structure
- Screenshots
- Cleaning Up

## Introduction

This project provides a simple example of using Minikube to create a local Kubernetes cluster. It includes sample Kubernetes manifests for deploying applications and services. The goal is to help you understand the basics of Kubernetes and how to use Minikube for local development and testing.

### Prerequisites

Before you begin, ensure you have the following installed on your local machine:

- Minikube
- kubectl
- Docker

### Installation

1. **Start Minikube:**

   ```sh
   minikube start
   ```

2. **Clone the Repository:**

   ```sh
   git clone https://github.com/Ayroid/k8s-minikube-project.git
   cd k8s-minikube-project
   ```

3. **Deploy Kubernetes Resources:**

   Apply the Kubernetes manifests provided in the config directory.

   ```sh
   kubectl apply -f config/
   ```

### Usage

After deploying the resources, you can interact with your local Kubernetes cluster using kubectl commands. Here are a few examples:

1. **List all pods:**

   ```sh
   kubectl get pods
   ```

2. **Get details of a specific pod:**

   ```sh
   kubectl describe pod <pod-name>
   ```

3. **Access a service:**

   If you have a service exposed, you can access it via Minikube's service command:

   ```sh
   minikube service <service-name>
   ```

### Project Structure

The project structure is as follows:

```
k8s-minikube-project/
├── config/
│ ├── mongo-config.yaml
│ ├── mongo-secret.yaml
│ ├── mongo.yaml
│ ├── webapp.yaml
├── README.md
└── ...
```

- **config/**: Contains Kubernetes manifests for deployments, services, and other resources.

### Screenshots

1. **Setup**

   ![Setup](images/1.setup.png)

2. **Starting Minikube**

   ![Starting Minikube](images/2.minikubestart.png)

3. **Deploying Resources**

   ![Deploying Resources](images/3.kubectlapply.png)

4. **Check Pods and Services**

   ![Check Services](images/4.kubectlget.png)

5. **Getting Minikube IP**

   ![Getting Minikube IP](images/5.minikubeip.png)

6. **Accessing Web Application**

   ![Accessing Web Application](images/6.testing.png)

7. **Deleting Pods and Services**

   ![Deleting Pods and Services](images/7.deleteall.png)

8. **Stopping Minikube**

   ![Stopping Minikube](images/8.minikubestop.png)

9. **Deleting Minikube Cluster**

   ![Deleting Minikube Cluster](images/9.minikubedelete.png)

### Cleaning Up

To remove all Kubernetes resources and stop Minikube, follow these steps:

1. **Delete all resources:**

   ```sh
   kubectl delete -f manifests/
   ```

2. **Stop Minikube:**

   ```sh
   minikube stop
   ```

3. **Delete Minikube cluster:**

   ```sh
   minikube delete
   ```

## Conclusion

This project provides a simple example of setting up a local Kubernetes cluster using Minikube. It includes sample Kubernetes manifests for deploying applications and services. You can use this project as a starting point for learning Kubernetes and testing your applications locally.
