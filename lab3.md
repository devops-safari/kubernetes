# Lab3: Using services to access Pods

## Lab scenario

Todo

## Objectives

In this lab, you'll:

- Task 1: Create the manifest
- Task 2: Deploy the manifest

## Instructions

### Task 1: Create the manifest

In your workspace, create a `blog-svc.yaml` file and copy into it the following 

```yaml
apiVersion: v1
kind: Service
metadata:
  name: ghost-blog
spec:
  ports:
  - targetPort: 2368
    protocol: TCP
  selector:
    app: ghost
  type: NodePort
```

Todo

### Task 2: Deploy the manifest

In your terminal, deploy the `blog-svc.yaml` file

```sh
kubectl apply -f blog-svc.yaml
```

Todo

---
Go to [Lab 3](./lab3.md)