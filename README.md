# 💻 Vagrant-Based DevOps Lab

<!-- Project Identity Badges -->
![type: infrastructure](https://img.shields.io/badge/type-vagrant--vm-sunset-orange?style=for-the-badge&logo=vagrant)
![scope: local lab](https://img.shields.io/badge/scope-local--lab-turquoise?style=for-the-badge)
![tech: devops](https://img.shields.io/badge/tech-devops-crimson-red?style=for-the-badge)


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


### 📌 Key Points

- All configurations are local-only and offline-friendly
- Not intended for production use
- `Vagrantfile` reads settings from `config.yaml` dynamically


---


### 📦 Popular Vagrant Boxes (Base Images)

| Box Name                    | OS / Distro          | Package Manager | Default User | Notes                               |
| --------------------------- | -------------------- | --------------- | ------------ | ----------------------------------- |
| `ubuntu/jammy64`            | Ubuntu 22.04 LTS     | `apt`           | `vagrant`    | Most used LTS, stable for servers   |
| `ubuntu/noble64`            | Ubuntu 24.04 LTS     | `apt`           | `vagrant`    | Latest Ubuntu LTS (April 2024)      |
| `debian/bookworm64`         | Debian 12            | `apt`           | `vagrant`    | Stable, minimal base                |
| `rockylinux/9`              | Rocky Linux 9        | `dnf`           | `vagrant`    | RHEL-based, enterprise-grade        |
| `almalinux/9`               | AlmaLinux 9          | `dnf`           | `vagrant`    | RHEL alternative, great for Ansible |
| `generic/centos9s`          | CentOS Stream 9      | `dnf`           | `vagrant`    | Continuously updated, RHEL-ish      |
| `fedora/40-cloud-base`      | Fedora 40            | `dnf`           | `vagrant`    | Bleeding edge, good for testing     |
| `opensuse/Leap-15.5.x86_64` | openSUSE Leap 15.5   | `zypper`        | `vagrant`    | Good for SUSE environments          |
| `archlinux/archlinux`       | Arch Linux (rolling) | `pacman`        | `vagrant`    | Rolling release, power users        |
| `kali-linux/rolling`        | Kali Linux (2025)    | `apt`           | `vagrant`    | For security testing labs           |


### 🧾 Notes:

- You can search more at: [Vagrant Cloud](https://portal.cloud.hashicorp.com/vagrant/discover)
- Default provider is usually `virtualbox`, but many also support `libvirt` and `vmware_desktop`
- You can use `vagrant init <box-name>` and then `vagrant up` to try them out


---

✅ Top Picks (If You Just Want 2–3 for Learning):

| Purpose                  | Recommended Box                      |
| ------------------------ | ------------------------------------ |
| General purpose (DevOps) | `ubuntu/jammy64` or `ubuntu/noble64` |
| RHEL-based learning      | `rockylinux/9` or `almalinux/9`      |
| Lightweight + stable     | `debian/bookworm64`                  |
