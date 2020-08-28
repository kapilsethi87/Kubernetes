# Minikube
<img src="/minikube/img/minikube_logo_name.jpg" width="400px"/> 

---

Minikube is a tool that makes it easy to run Kubernetes locally. Minikube runs a single-node Kubernetes cluster inside a Virtual Machine (VM) on your laptop for users looking to try out Kubernetes or develop with it day-to-day

## Setup VMWare for Minikube

#### If you are running VMWare Workstation 15 and want to run minikube, just follow these easy instructions.

Add VMware path to your Windows PATH variable.
C:\Program Files (x86)\VMware\VMware Workstation

[Install Docker machine driver](https://github.com/machine-drivers/docker-machine-driver-vmware/releases/download/v0.1.0/docker-machine-driver-vmware_windows_amd64.exe)

Rename docker-machine-driver-vmware_windows_amd64.exe to docker-machine-driver-vmware.exe.

Add this folder to your Windows PATH variable as above.

[Install VIX (Vmware Run)](https://my.vmware.com/web/vmware/details/vix_api_162/cHBiaGhlYmR3)

[VMware on the Command-line](https://docs.vmware.com/en/VMware-Fusion/10.0/com.vmware.fusion.using.doc/GUID-24F54E24-EFB0-4E94-8A07-2AD791F0E497.html)

---

# Install kubectl on Windows

**Step 1:**
Download the latest release v1.18.0 from
```bash
https://storage.googleapis.com/kubernetes-release/release/v1.18.0/bin/windows/amd64/kubectl.exe
```

**Step 2:**
Create a folder at C:\Kubenetes.
Add the kubectl.exe to this folder.
Add this folder to your Windows PATH variable.

**Step 3:**
Test to ensure the version of kubectl
```bash
kubectl version --client
```

---

# Install Minikube

To install Minikube manually on Windows, download "minikube-windows-amd64", rename it to minikube.exe, and add it to your path.
```bash
https://github.com/kubernetes/minikube/releases/download/v1.12.3/minikube-windows-amd64.exe
```

----

# Start the Minikube

#### Use vmware as the hypervisor driver
```bash
minikube start --driver=vmware
```

#### Minikube Default Credentials
```bash
username: docker
password: tcuser
```