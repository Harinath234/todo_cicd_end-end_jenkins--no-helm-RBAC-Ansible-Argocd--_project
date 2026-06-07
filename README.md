## Project Structure

```text
todo-project
│
├── Jenkinsfile
├── Dockerfile
│
└── Kubernetes
    ├── deployment.yaml
    └── service.yaml
 ```  

## Project Flow

```

GitHub
  ↓
Jenkins
  ↓
Build Docker Image
  ↓
Push Docker Image
  ↓
Update deployment.yaml
  ↓
kubectl apply
  ↓
Kubernetes

```


## Jenkins Credentials Needed
docker-hub-creds (Username/Password)
kubeconfig (Secret File)

#This is the simplest production-style CI/CD project without Helm, RBAC, Ansible, or ArgoCD. Jenkins handles the entire deployment directly using kubectl apply.
