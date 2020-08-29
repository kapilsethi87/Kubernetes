# Kubernetes Dashboard

A Kubernetes dashboard is a web-based Kubernetes user interface which is used to deploy containerized applications to a Kubernetes cluster, troubleshoot the applications, and manage the cluster itself along with its attendant resources.

**Step - 1**

### For creating the dashboard first - bring this up before starting Nodes
```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml		//Create Dashboard
```

### To create a service account for your dashboard
```bash
kubectl create serviceaccount dashboard -n default
```

### This command will add the cluster binding rules to your dashboard account
```bash
kubectl create clusterrolebinding dashboard-admin -n default \
   --clusterrole=cluster-admin \
   --serviceaccount=default:dashboard
```

### To get the secret key to be pasted into the dashboard token pwd. Copy the outcoming secret key
```bash
kubectl describe secret <Mountable secrets)
		OR OR OR OR OR OR OR
kubectl get secret $(kubectl get serviceaccount dashboard -o jsonpath="{.secrets[0].name}") -o jsonpath="{.data.token}"
```

### List the current namespaces in a cluster using
```bash
kubectl get namespaces
```

### To enable proxy and continues with new terminal window
```bash
kubectl proxy
```

### Kubernetes Dashboard
```bash
http://<master-node-ip-address>:<exposed-port>
http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/.
```