# 🚗 sidecar-pattern-demo
A pod declaration containing two containers: a busybox container that sends messages to stderr and a sidecar container that logs them.

### 🚀 Running the demo
1. Create the pod:
```bash
kubectl apply -f pod-declaration.yml
```

2. See the logs:
```bash
kubectl logs pod/sidecar-pattern-pod -c sidecar-container
```

---

### ⚙️  You can also go into the container and see their shared directory:

1. Exec into the pod:
```bash
kubectl exec -it pod/sidecar-pattern-pod --container sidecar-container
```

2. Go into var direcory:
```bash
cd var
```

3. Go into the emptyDir volume Kubernetes created:
```bash
cd my-volume-directory
```

4. See the file we are working in:
```bash
cat my-volume-file.txt
```
