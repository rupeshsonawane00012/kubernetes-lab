# 🚀 Kubernetes Beginner Lab

This project demonstrates basic Kubernetes concepts:

## 📌 Concepts Covered
- Pod
- Deployment
- Service (NodePort)
- Labels & Selectors
- Debugging

---

## ⚙️ Setup

```bash
kubectl apply -f namespace.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

🌐 Access

Get Node IP:

kubectl get nodes -o wide

Open:

http://<Node-IP>:30011