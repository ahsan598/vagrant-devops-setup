# 🧱 Single VM Setup (Vagrant)

This setup provides a lightweight **Vagrant environment** to spin up a single virtual machine using **VirtualBox**. Ideal for DevOps testing, provisioning, and tool sandboxing.

---

### 🔧 Features

- Ubuntu 24.04 LTS (can be customized)
- SSH access
- Easily configurable resources (CPU, RAM, IP)
- Shared folder support

### ⚙️ Configuration

All VM settings are defined in `config.yaml`:
- CPU, memory
- Static IP
- Port forwarding
- Optional GUI mode

> You can easily modify `config.yaml` before running `vagrant up`.

### 💡 Notes
- Default box is Ubuntu 24.04 LTS (changeable in config)
- Use `chmod +x provision.sh` before running if needed
- Provisioning script is optional and can be skipped via config


---

### 📁 Quick Commands

- Run these commands from the folder containing the Vagrantfile to manage your VM.

| Command                      | Description                                   |
| ---------------------------- | --------------------------------------------- |
| `vagrant up`                 | Start your VM                                 |
| `vagrant ssh`                | Login into your VM                            |
| `vagrant halt`               | Stop your VM                                  |
| `vagrant destroy`            | Destroy your VM                               |
| `vagrant status`             | Show the current status of the VM             |
| `vagrant box list`           | List all locally installed Vagrant boxes      |

