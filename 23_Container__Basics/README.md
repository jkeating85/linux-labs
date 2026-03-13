# Linux Lab 23 — Container Basics with Docker

## Objective

The purpose of this lab was to learn the fundamentals of Docker containers in a Linux environment.  
Docker is a containerization platform used heavily in DevOps, cloud computing, and platform engineering.

In this lab Docker was tested by:

• Running a container from the **hello-world image**  
• Troubleshooting a Docker permission error  
• Running Docker with administrative privileges  
• Configuring Docker to run without sudo  
• Verifying containers using the Docker CLI

This demonstrates basic container management skills required in modern cloud and DevOps environments.

---

# Environment

| Component | Description |
|----------|-------------|
| Operating System | Ubuntu Linux |
| Virtualization | Oracle VirtualBox |
| Host System | Windows |
| Shell | Bash Terminal |
| Container Platform | Docker |
| Container Registry | Docker Hub |

---

# Commands Used

| Command | Description |
|-------|-------------|
| docker run hello-world | Attempts to run a test container |
| sudo docker run hello-world | Runs the container with administrator privileges |
| sudo usermod -aG docker $USER | Adds the current user to the docker group |
| newgrp docker | Applies new group permissions without logging out |
| docker ps -a | Displays all containers |

---

# Command Definitions

## docker

Docker is a containerization platform used to package applications and their dependencies into isolated environments called **containers**.

Containers allow software to run consistently across different systems.

Docker is widely used in:

• DevOps  
• cloud infrastructure  
• platform engineering  
• microservices architecture  
• Kubernetes environments

---

## docker run

The `docker run` command creates and starts a new container from a Docker image.

Example:

docker run hello-world

When this command runs Docker performs several steps:

1. Docker checks if the image exists locally.
2. If the image is missing Docker downloads it from Docker Hub.
3. Docker creates a container from the image.
4. The container runs its executable.
5. Output is displayed in the terminal.

---

## hello-world image

The **hello-world image** is a minimal container used to verify that Docker is installed and functioning correctly.

When the container runs it prints:

Hello from Docker!

This confirms that:

• Docker daemon is running  
• Docker can download images  
• Docker can create containers  
• Docker containers execute properly

---

## sudo

`sudo` allows a normal user to execute commands with **administrative privileges (root access)**.

Example:

sudo docker run hello-world

This was required because the user had not yet been added to the Docker group.

---

## usermod

`usermod` is a Linux command used to modify user accounts.

Example:

sudo usermod -aG docker $USER

This command adds the current user to the **docker group**.

---

# Explanation of Command Symbols

## -a

`-a` means **append**.

This ensures the user is added to a group **without removing existing group memberships**.

Without `-a`, the command would overwrite all groups assigned to the user.

---

## -G

`-G` specifies the **group list** that the user should belong to.

In this case the group being assigned is:

docker

---

## docker group

The **docker group** allows users to run Docker commands without needing to use `sudo`.

Adding a user to this group is the standard configuration on Linux systems.

---

## $USER

`$USER` is an **environment variable** representing the currently logged-in user.

Example:

sudo usermod -aG docker $USER

This automatically applies the command to the current user account.

---

## newgrp

`newgrp` refreshes group membership in the current terminal session.

Example:

newgrp docker

Without this command the user would normally need to **log out and log back in** for the new group permissions to apply.

---

## docker ps

`docker ps` lists **currently running containers**.

---

## docker ps -a

The `-a` flag means **all containers**.

Example:

docker ps -a

This command shows:

• running containers  
• stopped containers  
• container IDs  
• container images  
• container status

---

# Docker Container Lifecycle

When the command below is executed:

docker run hello-world

Docker performs the following process:

1. Docker client sends a request to the Docker daemon.
2. Docker daemon checks if the image exists locally.
3. If not found Docker pulls the image from Docker Hub.
4. Docker creates a container from the image.
5. The container runs the program contained in the image.
6. The container prints output to the terminal.
7. The container exits after completing execution.

---

# Screenshots

## Docker Permission Error

![Docker Permission Error](screenshots/05_docker_permission_denied.png)

This screenshot shows the permission error that occurs when a user attempts to run Docker without being part of the docker group.

---

## Docker Hello World Container

![Docker Hello World](screenshots/06_docker_hello_world_success.png)

This screenshot shows the successful execution of the hello-world container.

The message confirms that Docker is installed and functioning properly.

---

## Docker Container List

![Docker Container List](screenshots/07_docker_container_list.png)

This screenshot displays the container created during the lab using the command:

docker ps -a

---

# Key Concepts Learned

Through this lab the following concepts were practiced:

• Running containers with Docker  
• Pulling container images from Docker Hub  
• Troubleshooting Docker permission errors  
• Managing Linux user groups  
• Understanding Docker container lifecycle  
• Listing containers using the Docker CLI

---

# Real World Importance

Docker containers are foundational to modern infrastructure.

Container technologies are used in:

• Kubernetes orchestration  
• cloud infrastructure platforms  
• DevOps CI/CD pipelines  
• scalable microservice architectures

Understanding Docker container basics is a key skill for:

• DevOps engineers  
• cloud engineers  
• site reliability engineers  
• platform engineers

---

# Lab Conclusion

This lab demonstrated how to run Docker containers, troubleshoot Docker permission issues, and configure Docker for non-root users.

These tasks reflect common responsibilities in Linux administration and containerized environments.

---

# Next Lab

Linux Lab 24 — System Troubleshooting

Topics will include:

• service failures  
• system diagnostics  
• resource monitoring  
• log analysis