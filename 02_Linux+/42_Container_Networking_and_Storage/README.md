# Linux+ Lab 42: Container Networking and Storage

---

## Objective

The purpose of this lab is to understand Docker container networking, inspect container configurations, and verify connectivity and services running inside containers.

In this lab, I:

* Created a custom Docker network
* Deployed a container on that network
* Verified container networking and IP addressing
* Tested a running NGINX web server
* Inspected container and network configurations
* Managed container lifecycle

---

## Environment

* Ubuntu Linux (VirtualBox VM)
* Docker Engine
* Bash Terminal
* Windows Host Machine
* GitHub Repository (IT_Labs)

---

## Commands Used (with Definitions)

| Command                  | Description                     |
| ------------------------ | ------------------------------- |
| `docker network create`  | Creates a custom Docker network |
| `docker network ls`      | Lists Docker networks           |
| `docker run`             | Runs a container                |
| `docker ps`              | Shows running containers        |
| `docker ps -a`           | Shows all containers            |
| `docker network inspect` | Shows network configuration     |
| `docker inspect`         | Shows container configuration   |
| `docker exec -it`        | Access container shell          |
| `ip a`                   | Shows IP addresses              |
| `curl localhost`         | Tests web server                |
| `docker stop`            | Stops container                 |

---

## Command Breakdown (Flags Explained)

### docker exec -it container1 bash

* `-i` → Interactive input
* `-t` → Terminal session
* `bash` → Opens shell

---

### docker inspect container1 | grep IPAddress

* `inspect` → Full container details
* `|` → Pipe output
* `grep` → Filter output
* `IPAddress` → Extract IP

---

### docker ps -a

* `-a` → Show all containers

---

## Workflow / Steps Performed

1. Navigated to lab directory
2. Listed Docker networks
3. Created custom network
4. Verified network creation
5. Ran container on custom network
6. Verified running container
7. Inspected network
8. Entered container shell
9. Installed networking tools
10. Checked container IP
11. Inspected container configuration
12. Tested NGINX service
13. Verified container from host
14. Listed networks again
15. Inspected network details
16. Retrieved container IP
17. Stopped container
18. Verified container stopped

---

## Screenshots (with Explanations)

---

### 01_enter_lab_directory.png

![01](./screenshots/01_enter_lab_directory.png)

This shows navigation into the lab directory, confirming the correct working environment before executing Docker commands.

---

### 02_list_docker_networks.png

![02](./screenshots/02_list_docker_networks.png)

This displays all existing Docker networks including default bridge, host, and none networks.

---

### 03_create_custom_network.png

![03](./screenshots/03_create_custom_network.png)

This shows the creation of a custom Docker bridge network used for container isolation.

---

### 04_verify_custom_network.png

![04](./screenshots/04_verify_custom_network.png)

This confirms the custom network exists after creation.

---

### 05_run_container_on_network.png

![05](./screenshots/05_run_container_on_network.png)

This shows the container being launched on the custom network.

---

### 06_verify_running_container.png

![06](./screenshots/06_verify_running_container.png)

This confirms the container is actively running using `docker ps`.

---

### 07_inspect_network.png

![07](./screenshots/07_inspect_network.png)

This shows detailed JSON output of the Docker network including subnet and gateway configuration.

---

### 08_enter_container_shell.png

![08](./screenshots/08_enter_container_shell.png)

This demonstrates entering the container interactively using `docker exec`.

---

### 09_install_iproute2.png

![09](./screenshots/09_install_iproute2.png)

This shows installation of networking tools inside the container.

---

### 10_container_ip_address.png

![10](./screenshots/10_container_ip_address.png)

This confirms the container’s internal IP using `ip a`.

---

### 11_container_inspect_summary.png

![11](./screenshots/11_container_inspect_summary.png)

This shows container configuration details including status and runtime settings.

---

### 12_nginx_localhost_test.png

![12](./screenshots/12_nginx_localhost_test.png)

This confirms NGINX is running by displaying HTML output from `curl localhost`.

---

### 13_verify_container_running.png

![13](./screenshots/13_verify_container_running.png)

This verifies the container is still running from the host system.

---

### 14_list_docker_networks.png

![14](./screenshots/14_list_docker_networks.png)

This reconfirms available Docker networks including the custom network.

---

### 15_inspect_custom_network.png

![15](./screenshots/15_inspect_custom_network.png)

This shows detailed configuration of the custom network including IP range.

---

### 16_verify_container_ip.png

![16](./screenshots/16_verify_container_ip.png)

This confirms the container IP address from the host using `docker inspect`.

---

### 17_stop_container.png

![17](./screenshots/17_stop_container.png)

This shows the container being stopped using `docker stop`.

---

### 18_verify_container_stopped.png

![18](./screenshots/18_verify_container_stopped.png)

This confirms the container status is **Exited**, verifying proper shutdown.

---

## Key Concepts

* Docker bridge networking
* Container IP allocation
* Network isolation
* Container inspection
* Service verification

---

## Real-World Relevance

This lab reflects real-world usage in:

* Cloud platforms (Azure, AWS)
* Kubernetes networking
* Microservices environments
* DevOps pipelines

---

## What I Learned

* How Docker networking works
* How to inspect containers and networks
* How to verify services inside containers
* How to troubleshoot container connectivity
* How to manage container lifecycle

---
