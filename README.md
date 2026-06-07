## Project Structure

```text
todo-project
│
├── Jenkinsfile
├── Dockerfile
│
├── Kubernetes
│   ├── deployment.yaml
│   └── service.yaml
│
├── rbac
│   ├── namespace.yaml
│   ├── serviceaccount.yaml
│   ├── role.yaml
│   └── rolebinding.yaml
│
└── ansible
    ├── inventory
    └── deploy.yml
```
    

## Project Flow

```

GitHub Checkout
   ↓
Jenkins
   ↓
Build Docker Image
   ↓
Push Docker Image
   ↓
Update deployment.yaml
   ↓
Git Commit & Push
   ↓
ansible-playbook deploy.yml        #### Kubernetes (RBAC + Deployment + Service)
   ↓
RBAC Applied
   ↓
Deployment Applied
   ↓
Service Applied
  
```
