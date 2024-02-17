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