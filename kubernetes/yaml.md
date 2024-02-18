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

---

## Service

```yaml
apiVersion: v1
kind: Service
metadata:
  name: <service-name>

spec:
  selector:
    app: <deployment-name>

  ports:
    - protocol: TCP
      port: 80
      targetPort: <container-port>
  type: LoadBalancer
```