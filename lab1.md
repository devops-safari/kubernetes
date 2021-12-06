# Lab1: Installing and running minikube

## Lab scenario

your team decided to use Kubernetes, and you were tasked to install minikube.

## Objectives

In this lab, you'll:

- Task 1: Downloading minikube
- Task 2: Running minikube

## Instructions

### Task 1: Downloading minikube

In your terminal, download minikube and install it

```sh
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

chmod +x minikube

sudo mkdir -p /usr/local/bin/

sudo install minikube /usr/local/bin/
```

### Task 2: Running minikube

In your terminal, start minikube

```sh
minikube start
```

---
Go to [Lab 2](./lab2.md)