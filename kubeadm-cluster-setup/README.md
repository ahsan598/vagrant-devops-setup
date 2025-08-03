# ⚙️ Kubernetes Cluster Setup using Kubeadm (Vagrant-based)

This project provides a simple and reproducible way to set up a **multi-node Kubernetes cluster** using **kubeadm** and **Vagrant** virtual machines.

It’s ideal for learning and practicing **Kubernetes the hard way**—hands-on and close to production-like setup without cloud dependencies.

---

### 🧰 Requirements

- [Vagrant](https://developer.hashicorp.com/vagrant/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Basic understanding of Linux & Kubernetes


### 🖥️ Cluster Topology

- `master`: control-plane node  
- `worker1`, `worker2`: worker nodes  
- Ubuntu base boxes with custom CPU/RAM/IP


### 📚 Follow manual setup instructions here:

- [Kubernetes the Hard Way (by Kelsey Hightower)](https://github.com/kelseyhightower/kubernetes-the-hard-way)
- [KodeKloud Kubeadm Clusters Repo](https://github.com/kodekloudhub/certified-kubernetes-administrator-course/tree/master/kubeadm-clusters)
- [Kubeadm Official Docs](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/)



💡 **Tip:** Use the included [setup-kubeadm.md](setup-kubeadm.md) guide to manually configure the cluster if needed.
