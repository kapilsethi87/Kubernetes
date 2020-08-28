# Kubernetes
<img src="img/K8_logo.png" width="100px"/> 

---

Kubernetes is an open source platform for managing containerized applications across multiple hosts. It provides basic mechanisms for deployment, maintenance, and scaling of applications.

Kubernetes builds upon a decade and a half of experience at Google running production workloads at scale using a system called Borg, combined with best-of-breed ideas and practices from the community.

# Kubernetes Components
## Master Node Components
1) Kube API-server
2) etcd 					//etcd is the cluster brain, 
3) Kube-scheduler
4) Kube Controller Manager
  

* **Node Manager** - It manages the nodes. it createsnew nodes if any node unavailable or destroyed.
* **Replication Controller** - It manages if the desired number of containers is running in the replication group.
* **Endpoints controller** - 	 It populates the endpoints object that is, joins Services & Pods.

## Worker Node Components
1) The kubelet
2) Kube-proxy
3) Kubernetes pod
4) Container Runtime

[Kubectl Short Commands](https://kubernetes.io/docs/reference/kubectl/overview/#resource-types)

[Kubernetes Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

[Kubernetes Documentation](https://kubernetes.io/docs/home/)

### Kubectl Command Explain
```sh
kubectl explain pods
kubectl explain pods --recursive
```

### There are two types of Pods
 
* **Single container pod** - They can be simply created with the kubctl run command, where you have a defined image on the Docker registry which we will pull while creating a pod. 
* **Multi container pod** - Multi container pods are created using yaml mail with the definition of the containers.


[LinuxDevOps.in](http://linuxdevops.in)
