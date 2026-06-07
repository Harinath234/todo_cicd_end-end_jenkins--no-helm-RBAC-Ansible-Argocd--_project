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
└── argocd
    └── application.yaml
```
    

## Project Flow

```

Developer Push
      ↓
GitHub
      ↓
Jenkins
      ↓
Build Docker Image
      ↓
Push Docker Image
      ↓
Update deployment.yaml (or Helm values.yaml)
      ↓
Git Commit & Push
      ↓
ArgoCD detects Git change
      ↓
ArgoCD deploys to Kubernetes

```
