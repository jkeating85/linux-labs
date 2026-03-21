# Linux+ Lab 40 — Ansible Basics

---

## 🧪 Objective

The purpose of this lab is to introduce configuration management using Ansible. In this lab, I installed Ansible, created an inventory file, wrote a playbook, and executed automation tasks to create and modify a file on the system. This demonstrates foundational DevOps and automation skills used in cloud, infrastructure, and system administration environments.

---

## 🖥️ Environment

* Ubuntu Linux (VirtualBox VM)
* Bash Terminal
* Windows Host Machine
* GitHub Lab Repository

---

## ⚙️ Commands Used (With Definitions)

### 📁 Directory Setup

```bash
mkdir -p ~/IT_Labs/02_Linux+/40_Ansible_Basics/Screenshots
```

Creates the full directory structure, including parent folders if they do not exist.

```bash
cd ~/IT_Labs/02_Linux+/40_Ansible_Basics
```

Changes into the lab directory.

```bash
pwd
```

Displays the current working directory to confirm correct location.

---

### 🧰 Ansible Installation

```bash
ansible --version
```

Checks if Ansible is installed. If not installed, an error will appear.

```bash
sudo apt update
```

Updates package lists from repositories to ensure the latest versions are available.

```bash
sudo apt install ansible -y
```

Installs Ansible and required dependencies automatically.

```bash
ansible --version
```

Verifies that Ansible is successfully installed.

---

### 📄 Inventory & Testing

```bash
nano inventory.ini
```

Creates and edits the Ansible inventory file.

```bash
ansible -i inventory.ini local -m ping
```

Tests connectivity using Ansible’s built-in ping module.

* `-i` → Specifies inventory file
* `-m` → Specifies module
* `ping` → Tests connectivity (returns "pong" if successful)

---

### 📜 Playbook Creation & Execution

```bash
nano first_playbook.yml
```

Creates and edits the Ansible playbook.

```bash
ansible-playbook -i inventory.ini first_playbook.yml
```

Executes the playbook.

* `ansible-playbook` → Runs automation tasks
* `-i` → Specifies inventory file

---

### 🔍 Verification

```bash
cat /tmp/ansible_test.txt
```

Displays the contents of the file created by Ansible to confirm successful execution.

```bash
echo "" >> /tmp/ansible_test.txt
```

Adds a newline for cleaner output formatting.

---

## 🧠 Command Breakdown Example

```bash
ansible-playbook -i inventory.ini first_playbook.yml
```

| Part               | Meaning                                   |
| ------------------ | ----------------------------------------- |
| ansible-playbook   | Runs an Ansible automation playbook       |
| -i inventory.ini   | Specifies which inventory file to use     |
| first_playbook.yml | The YAML file containing automation tasks |

---

## 🖼️ Screenshots (With Explanations)

### Screenshot 1 — Directory Setup

Shows creation of lab directory and navigation into the correct path.

### Screenshot 2 — Ansible Not Installed

Shows system response indicating Ansible is not installed.

### Screenshot 3 — Package Update

Shows system updating package lists from repositories.

### Screenshot 4 — Installing Ansible

Shows installation of Ansible and dependencies.

### Screenshot 5 — Version Verification

Confirms Ansible installation and displays version information.

### Screenshot 6 — Inventory Test (Ping)

Shows successful Ansible communication with localhost (`pong` response).

### Screenshot 7 — Playbook Creation

Displays YAML playbook defining automation tasks.

### Screenshot 8 — Playbook Execution

Shows Ansible running tasks including file creation and modification.

### Screenshot 9 — Play Recap

Displays summary of tasks executed successfully.

### Screenshot 10 — File Verification

Shows the contents of the file created and modified by Ansible.

---

## 🧠 Key Concepts

* Ansible is an agentless automation tool used for configuration management
* Uses YAML playbooks to define automation tasks
* Uses inventory files to define managed systems
* Tasks are executed in a repeatable and consistent way
* Enables infrastructure as code (IaC) practices

---

## 🌍 Real-World Relevance

This lab demonstrates how system administrators and DevOps engineers automate configuration tasks, manage systems at scale, ensure consistency across environments, and reduce manual errors in deployments. Ansible is widely used in cloud environments (Azure, AWS), DevOps pipelines, infrastructure automation, and security compliance.

---

## 🧠 What I Learned

* How to install and configure Ansible
* How to create and use an inventory file
* How to write a basic Ansible playbook
* How to execute automation tasks
* How to verify system changes after automation

---

## 🎯 Professional Insight

This lab demonstrates the transition from manual system administration to automated infrastructure management. By using Ansible playbooks, I can define system states declaratively and ensure consistent results across environments. Verification using `cat` confirms that automation tasks were applied successfully, which is critical in production systems to validate changes and maintain reliability.

---
