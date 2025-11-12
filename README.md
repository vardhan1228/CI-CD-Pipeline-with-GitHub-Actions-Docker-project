# CI-CD-Pipeline-with-GitHub-Actions-Docker-project

# Kubernetes Configuration

This repository contains Kubernetes configuration files for deploying and managing a service.

## Prerequisites for Windows

Before you begin, make sure you have the following tools installed on your Windows system:

1. **Docker Desktop for Windows**
   - Download and install from [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
   - Ensure Kubernetes is enabled in Docker Desktop settings

2. **Minikube**
   - Download and install from [Minikube Release](https://github.com/kubernetes/minikube/releases)
   - Run `minikube start` to initialize the cluster
   - Verify installation with `minikube status`

3. **kubectl**
   - Install using one of these methods:
     - Through Chocolatey: `choco install kubernetes-cli`
     - Direct download from [Kubernetes Release](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/)
   - Verify installation with `kubectl version`

4. **Windows Terminal (Optional but recommended)**
   - Install from Microsoft Store or [GitHub Releases](https://github.com/microsoft/terminal/releases)

5. **PowerShell 5.1 or later**
   - Comes pre-installed with Windows 10/11
   - Verify version with `$PSVersionTable.PSVersion`

## Files

- `deployment.yaml`: Contains the Kubernetes Deployment configuration that manages the application pods.
- `service.yaml`: Contains the Kubernetes Service configuration that exposes the application.

## Usage

To apply these configurations to your Kubernetes cluster:
### the configuratin in ```k8s-files path`1``

```bash
# Apply the deployment
kubectl apply -f deployment.yaml

# Apply the service
kubectl apply -f service.yaml
```
```bash
#  check the pods status
kubectl get pods
```
```bash
# check the service name and port 
kubectl get svc
```

```bash
#  Access the service on broswer with service name 
minikube service hotstar-service
```

## Structure

### Deployment
The `deployment.yaml` file defines how your application should be deployed, including:
- Number of replicas
- Container specifications
- Resource requirements
- Labels and selectors

### Service
The `service.yaml` file defines how your application is exposed, including:
- Service type
- Port configurations
- Selectors to target the deployment

## Maintenance

To update or modify the configurations:
1. Make changes to the respective YAML files
2. Apply the changes using `kubectl apply -f <filename>.yaml`

## Contributing

Feel free to submit issues and enhancement requests.

