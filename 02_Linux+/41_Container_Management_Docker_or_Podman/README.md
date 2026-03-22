# Linux+ Lab 41 — Container Management (Docker)

---

## Objective

The purpose of this lab is to learn how to install, configure, and manage containers using Docker in a Linux environment.

In this lab, I performed:
- Docker installation and verification
- Running a container
- Managing containers and images
- Cleaning up resources

This lab demonstrates foundational containerization skills used in DevOps, Cloud Engineering, and Cybersecurity.

---

## Environment

- Ubuntu Linux (VirtualBox VM)
- Bash Terminal
- Windows Host Machine
- Docker (docker.io package)
- GitHub Lab Repository

---

## Commands Used

| Command | Description |
|--------|-------------|
| `sudo apt update` | Updates package lists from repositories |
| `sudo apt install docker.io -y` | Installs Docker without prompts |
| `docker --version` | Displays Docker version |
| `systemctl status docker` | Checks Docker service status |
| `sudo usermod -aG docker $USER` | Adds user to Docker group |
| `newgrp docker` | Applies new group permissions |
| `docker run hello-world` | Runs a test container |
| `docker ps -a` | Lists all containers |
| `docker images` | Lists Docker images |
| `docker rm <id>` | Removes a container |
| `docker rmi <image>` | Removes an image |

---

## Command Breakdown

### Example:
```bash
docker rm 5b63f3898784
```

| Part | Meaning |
|------|--------|
| `docker` | Container management tool |
| `rm` | Remove container |
| `5b63f3898784` | Container ID |

---

### Example:
```bash
sudo usermod -aG docker $USER
```

| Part | Meaning |
|------|--------|
| `sudo` | Run as root |
| `usermod` | Modify user account |
| `-aG` | Append to group |
| `docker` | Target group |
| `$USER` | Current user |

---

## Workflow / Steps

1. Created lab directory in Windows and Linux
2. Navigated to lab directory in Linux
3. Installed Docker using apt package manager
4. Verified Docker installation and service status
5. Configured Docker permissions for non-root usage
6. Ran first container using `hello-world`
7. Listed containers and images
8. Removed containers and images for cleanup

---

## Screenshots

---

### 01_directory_setup.png
Shows the Windows lab folder structure including the Screenshots folder and README.md file. This demonstrates proper lab organization and preparation for documentation.

---

### 02_navigate_to_lab_directory.png
Displays navigation to the Linux lab directory using `cd`, verification with `pwd`, and directory listing with `ls`. This confirms correct working directory.

---

### 03_create_lab_directory.png
Shows creation of the lab directory using `mkdir` and verification using `ls`. This confirms successful directory creation in Linux.

---

### 04_enter_lab_directory.png
Displays entering the lab directory and confirming the path with `pwd`. The empty `ls` output confirms a clean working directory.

---

### 05_install_docker.png
Shows updating package lists and installing Docker using `apt`. Output confirms Docker is installed and ready.

---

### 06_verify_docker_installation.png
Displays Docker version and service status. The "active (running)" status confirms Docker daemon is operational.

---

### 07_fix_docker_permissions.png
Shows adding the user to the Docker group and verifying Docker can run without sudo. This is critical for proper user-level container management.

---

### 08_run_first_container.png
Displays running the `hello-world` container. The output confirms Docker can pull images, create containers, and execute workloads.

---

### 09_list_containers_and_images.png
Shows listing all containers and images. Demonstrates visibility into container lifecycle and image management.

---

### 10_remove_container_and_image.png
Displays removal of containers and images. Confirms ability to clean up Docker resources, which is essential in production environments.

---

## Key Concepts

- Containerization
- Docker Engine
- Docker Images vs Containers
- Container Lifecycle Management
- Linux Package Management
- User and Group Permissions
- Systemd Service Management

---

## Real-World Relevance

Docker is widely used in:
- Cloud platforms (Azure, AWS, GCP)
- DevOps pipelines (CI/CD)
- Microservices architecture
- Application deployment
- Security isolation environments

Understanding Docker is essential for roles such as:
- Cloud Engineer
- DevOps Engineer
- Site Reliability Engineer (SRE)
- Cybersecurity Analyst

---

## What I Learned

- How to install and configure Docker in Linux
- How to run and verify containers
- The difference between images and containers
- How to manage container lifecycle (create, list, remove)
- How to configure permissions for Docker usage
- How containerization works in real-world environments