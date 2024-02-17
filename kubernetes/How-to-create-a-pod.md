## How to create a pod


### Step1

- create a docker image

```docker
docker build -t <image-name> .
```

---

### Step2

- push the image to docker hub

```docker 
docker push <image-name>
```

---

### Step3

- create deployment

```docker 
kubectl create deployment <deployment-name> --image=<image-name>
```

---

### Step4

- create service

```docker
kubectl expose deployment <deployment-name> --type=LoadBalancer --port=8080
```

---

### Step5

- access [http://localhost:8080](http://localhost:8080)