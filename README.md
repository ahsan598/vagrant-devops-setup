# 💻 Vagrant-Based DevOps Lab

<!-- Project Identity Badges -->
![type: infrastructure](https://img.shields.io/badge/type-devops--vm-orange?style=for-the-badge)
![scope: local lab](https://img.shields.io/badge/scope-local--lab-darkgreen?style=for-the-badge)
![tech: vagrant](https://img.shields.io/badge/tech-vagrant-steelblue?style=for-the-badge)


This repository provides a **modular collection of Vagrant environments** designed to spin up local virtual machines for DevOps tooling, automation workflows, and hands-on infrastructure practice.

Each setup is fully configurable — including VM resources, networking, and provisioning — making it ideal for learning, prototyping, or creating repeatable local labs.

Included environments:
-  A minimal, reusable Ubuntu base VM template
- CI/CD pipeline setup using Jenkins and agent VMs
- Multi-node Kubernetes cluster for orchestration practice
- Ansible-ready VM for configuration management testing

---

### ⚙️ Requirements

Install these tools before using the setup:

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Terminal or code editor (e.g., VS Code, Git Bash, native shell)


### 🔑 Features

- Single and multi-VM environments using `Vagrantfile`
- Customizable CPU, memory, IP, and ports
- Provisioning with Bash scripts
- Quick teardown and rebuild for iterative testing
- Ideal for local DevOps simulations and sandboxing


### 📁 Directory Overview

```sh
vagrant-vms/
├── base-vm/               # Minimal reusable Ubuntu VM
├── cicd-pipeline-setup/   # Jenkins + agents (can reuse base VM)
├── ansible-ready-vm/      # For testing Ansible locally
├── k8s-cluster/           # Multi-node Kubernetes playground
```


###  🚀 Usage (Basic Commands)

```sh
# Start all VMs in the current directory
vagrant up

# SSH into a specific VM
vagrant ssh <vm-name>

# Destroy VM(s)
vagrant destroy -f
```


### 💡 Use Cases

- Hands-on with Jenkins, Kubernetes, and Ansible
- Simulate CI/CD pipelines and infrastructure locally
- Practice infrastructure automation in a safe, offline setup


### 📌 Notes

- All configurations are local-only and offline-friendly
- Not intended for production use
- `Vagrantfile` reads settings from `config.yaml` dynamically
