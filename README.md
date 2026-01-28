# ☸️ Kubernetes

My sandbox for mastering Kubernetes

## Basic Commands

```bash
kubectl get nodes
```

```bash
kubectl get services
```

```bash
kubectl get pods
```

## 🔹 Main kubectl Commands

### 📝CRUD Commands

**Create deployment**

```bash
kubectl create deployment nginx-depl --image=nginx
```

```bash
kubectl create deployment mongodb-deployment --image=mongo
```

**Edit deployment**

```bash
kubectl edit deployment nginx-depl
```

**Delete deployment**

```bash
kubectl delete deployment mongodb-deployment
```
```bash
kubectl delete -f [name].yaml
```

### 📊 Status of Different K8s Components

```bash
kubectl get nodes|pod|services|replicaset|deployment
```

```bash
kubectl get pod -o wide
```

### 🐛 Debugging Tools

**Logs**

```bash
kubectl logs nginx-depl-5fcbf6fffd-w6r6n
```

**Get interactive terminal**

```bash
kubectl exec -it mongodb-deployment-7f79558879-slcch -- bash
```

**Get info about pod**

```bash
kubectl describe pod mongodb-deployment-7f79558879-slcch
```

### ⚙️ Use Configuration File for CRUD

**Apply configuration**

```bash
kubectl apply -f nginx-deployment.yaml
```

**Delete using configuration**

```bash
kubectl delete -f nginx-deployment.yaml
```