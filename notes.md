

#🚀 Kubernetes Basic Commands (kubectl)
📊 1. Cluster & Nodes Commands
✅ Check cluster info
kubectl cluster-info

👉 Shows cluster details

👉 Marathi:

Kubernetes cluster चालू आहे का ते कळतं

✅ Check nodes (machines)
kubectl get nodes

👉 Output = EC2 / servers

👉 Marathi:

कोणत्या machines वर app चालतो ते दिसतं

📦 2. Pods Commands
✅ Create Pod
kubectl run nginx-pod --image=nginx

👉 Pod = app running container

✅ List Pods
kubectl get pods

👉 Marathi:

सगळे running pods दिसतात

✅ Detailed info
kubectl describe pod nginx-pod

👉 Shows events, errors, IP

✅ Check logs
kubectl logs nginx-pod

👉 Marathi:

app मध्ये काय चालू आहे ते logs मध्ये दिसतं

✅ Delete Pod
kubectl delete pod nginx-pod
🌐 3. Services Commands
✅ Create Service (Expose Pod)
kubectl expose pod nginx-pod --type=NodePort --port=80

👉 Makes app accessible

✅ List Services
kubectl get svc
✅ Describe Service
kubectl describe svc nginx-pod

👉 Shows NodePort, IP

📁 4. YAML File Commands (VERY IMPORTANT 🔥)
✅ Create from YAML
kubectl apply -f deployment.yaml

👉 Marathi:

YAML file वापरून resources तयार करतो

✅ Delete from YAML
kubectl delete -f deployment.yaml
✅ See YAML of running object
kubectl get pod nginx-pod -o yaml

👉 Super useful for learning 🔥

🔁 5. Deployment Commands
✅ Create deployment
kubectl create deployment nginx-deploy --image=nginx
✅ Check deployments
kubectl get deployments
✅ Scale app
kubectl scale deployment nginx-deploy --replicas=3

👉 Marathi:

एक app → 3 copies (auto scaling)

🔍 6. Debugging Commands (VERY IMPORTANT)
✅ Check everything
kubectl get all
✅ Watch live changes
kubectl get pods -w
✅ Execute inside container
kubectl exec -it nginx-pod -- /bin/bash

👉 Marathi:

container आत जाऊन check करू शकतो

📌 7. Namespaces Commands
✅ List namespaces
kubectl get ns
✅ Use namespace
kubectl get pods -n kube-system

👉 Marathi:

वेगवेगळे environments manage करायला

🎯 Most Important Commands (Interview + Real Use)

👉 Learn these FIRST:

kubectl get pods
kubectl get svc
kubectl get nodes
kubectl describe pod <name>
kubectl logs <name>
kubectl apply -f file.yaml
kubectl delete pod <name>
kubectl exec -it <pod> -- /bin/bash
🧠 Simple Summary (Super Important 🔥)

👉 Flow:

Create → Check → Debug → Expose → Scale

👉 Marathi:

तयार करा → पाहा → problem fix करा → बाहेर expose करा → scale करा

⚡ Pro Tip (Game Changer)

Use shortcut:

kubectl get pods = kubectl get po
kubectl get services = kubectl get svc
kubectl get deployments = kubectl get deploy
