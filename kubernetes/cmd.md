### Setup Alias
```shell
code ~/.zshrc 
alias k="kubectl"
```

### Version
```shell
kubectl version
```

### Apply
```shell
kubectl apply -f <file>.yml
```

### Show Pods
```shell
kubectl get pods
```

### Delete Pod
```shell
kubectl delete pod <pod-name>
```

### Show Logs
```shell
kubectl logs <pod-name>
```

### Create Deployment
```shell
kubectl create deployment <deployment-name> --image=<image-name>
```

### Show Deployment
```shell
kubectl get deployments
```

### Delete  Deployment
```shell
kubectl delete deployments <deployment-name>
```

### Restart Deployment
```shell
kubectl rollout restart deployment <deployment-name>
```

### Show Services
```shell
kubectl get services
```