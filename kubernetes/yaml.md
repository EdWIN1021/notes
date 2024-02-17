## Deployment


```yaml
# https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
apiVersion: apps/v1

# deployment
kind: Deployment

metadata:
  name: <deployment-name>
  
spec:
  # number of pods
  replicas: 1

  selector:
    matchLabels:
      app: <app-name>

  template:
    metadata:
      labels:
        app: <app-name>

    spec:
      containers: 
        - name: <container-name>

          # image on docker hub
          image: <image-name>:<tag>

```