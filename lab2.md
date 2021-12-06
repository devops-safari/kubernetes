# Lab2: Creating a Ghost-blog pod

## Lab scenario

your team decided to create a blog using Ghost, and you were tasked to deploy it to Kubernetes.

## Objectives

In this lab, you'll:

- Task 1: Create the manifest
- Task 2: Deploy the manifest

## Instructions

### Task 1: Create the manifest

In your workspace, create a `blog-pod.yaml` file and copy into it the following 

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: ghost-blog
  labels:
    app: ghost
spec:
  restartPolicy: OnFailure
  containers:
  - name: ghost-blog
    image: ghost:alpine
    ports:
    - name: http
      containerPort: 2368
```

The `labels` key contain user-defined keys/values, it's used to help Kubernetes identify a group of pod

### Task 2: Deploy the manifest

In your terminal, deploy the `blog-pod.yaml` file

```sh
kubectl apply -f blog-pod.yaml
```

To verify the creatin of pod, run

```sh
kubectl get pod ghost-blog
```

The status should be `Running` when the pod is successfully deployed.

---
Go to [Lab 3](./lab3.md)