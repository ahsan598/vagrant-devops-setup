# 💻 Vagrant-Based DevOps Lab

<!-- Project Identity Badges -->
![type: infrastructure](https://img.shields.io/badge/type-devops--vm-steelblue?style=for-the-badge)
![scope: local lab](https://img.shields.io/badge/scope-local--lab-darkgreen?style=for-the-badge)
![tech: vagrant](https://img.shields.io/badge/tech-vagrant-orange?style=for-the-badge)


This repository provides a modular collection of Vagrant environments designed to spin up local virtual machines for DevOps tooling, automation workflows, and hands-on infrastructure practice.

Each setup is fully configurable — including VM resources, networking, and provisioning — making it ideal for learning, prototyping, or creating repeatable local labs.

Included environments:
-  A minimal, reusable Ubuntu base VM template
- CI/CD pipeline setup using Jenkins and agent VMs
- Multi-node Kubernetes cluster for orchestration practice
- Ansible-ready VM for configuration management testing

---

### 🧰 Requirements

Install the following tools before getting started:

- [Vagrant](https://www.vagrantup.com/downloads) – for VM provisioning
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) – as the VM provider
- Code Editor or Terminal – (e.g., VS Code, Git Bash, or a native Linux terminal)


### 🔧 Key Features

- Single and multi-VM setups via `Vagrantfile`
- Customizable CPU, Memory, IP, and Port forwarding
- Basic provisioning using Bash scripts
- Ideal for simulating local DevOps clusters
- Quick teardown and rebuilds


### 📂 Project Structure

```sh
vagrant-vms/
├── base-vm/                  # Single minimal reusable VM (Ubuntu)
├── cicd-pipeline-setup/      # Multi-VM: Jenkins + agents + (can reuse 1 VM for app/db tests)
├── ansible-ready-vm/         # Only if you're testing Ansible
├── k8s-cluster/              # Your orchestration playground
```


###  🚀 Quick Usage

```sh
# Start VM(s)
vagrant up

# SSH into a specific VM
vagrant ssh <vm-name>

# Tear down
vagrant destroy -f
```


### 💡 Use Cases

- Practice with tools like Jenkins, Ansible, etc.
- Simulate multi-node infra for CI/CD or Kubernetes
- Run experiments in an isolated local sandbox


### 📌 Notes

- All configurations are local-only and offline-friendly
- Not intended for production use
- `Vagrantfile` reads settings from `config.yaml` dynamically
