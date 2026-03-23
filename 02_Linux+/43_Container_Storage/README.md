# Linux+ Lab 43 – Container Storage (Docker Volumes)

---

## Objective

The purpose of this lab is to understand how Docker volumes provide persistent storage and how data can be shared between containers.

In this lab, I demonstrated:

- Creating Docker volumes
- Writing data inside a container
- Persisting data beyond container lifecycle
- Sharing data across multiple containers
- Cleaning up containers and volumes

This is a critical concept in DevOps, Cloud Engineering, and containerized application design.

---

## Environment

- Ubuntu Linux (VirtualBox VM)
- Docker Engine
- Bash Terminal
- Windows Host Machine
- GitHub Repository

---

## Commands Used

| Command | Description |
|--------|-------------|
| docker volume create my_volume | Creates a new Docker volume |
| docker volume ls | Lists all Docker volumes |
| docker volume inspect my_volume | Displays detailed information about the volume |
| docker run -it --name storage_test -v my_volume:/data ubuntu bash | Runs a container and mounts a volume |
| echo "text" > file | Writes text to a file |
| cat file | Displays file contents |
| docker rm container_name | Removes a container |
| docker ps -a | Lists all containers |
| docker volume rm my_volume | Removes a Docker volume |

---

## Command Breakdown (Important)

### docker run Command

```bash
docker run -it --name storage_test -v my_volume:/data ubuntu bash
```

| Part | Meaning |
|------|--------|
| docker run | Starts a new container |
| -it | Interactive terminal (keyboard + screen access) |
| --name storage_test | Assigns a custom name to the container |
| -v my_volume:/data | Mounts Docker volume to container directory |
| ubuntu | Image used to create container |
| bash | Opens bash shell inside container |

---

## Symbol Definitions

| Symbol | Meaning |
|--------|--------|
| - | Flag indicator (modifies command behavior) |
| -- | Long-form flag (more readable version of flags) |
| : | Maps volume to container path |
| > | Redirects output to a file (overwrites) |
| / | Root directory path indicator |
| "" | Wraps text string for commands |
| ~ | Home directory of current user |
| $ | Regular user prompt |
| # | Root user prompt |

---

## Screenshots

### 01. Enter Lab Directory
![01_enter_lab_directory.png](Screenshots/01_enter_lab_directory.png)

This screenshot shows the Linux terminal successfully navigating into the `43_Container_Storage` lab directory. This confirms the working directory was prepared correctly before beginning Docker storage operations.

### 02. List Docker Volumes
![02_list_docker_volumes.png](Screenshots/02_list_docker_volumes.png)

This screenshot shows the initial Docker volume list before any new storage resources were created. It establishes the baseline state of the environment.

### 03. Create Docker Volume
![03_create_docker_volume.png](Screenshots/03_create_docker_volume.png)

This screenshot shows the creation of the Docker volume `my_volume` and confirms it now appears in the Docker volume list. This demonstrates the successful creation of persistent storage.

### 04. Inspect Docker Volume
![04_inspect_docker_volume.png](Screenshots/04_inspect_docker_volume.png)

This screenshot shows detailed information about the Docker volume, including the driver and mountpoint on the host system. It confirms where Docker stores the volume data outside the container lifecycle.

### 05. Write Data to Volume
![05_write_data_to_volume.png](Screenshots/05_write_data_to_volume.png)

This screenshot shows data being written to `/data/testfile.txt` inside the container and then immediately read back. Because `/data` is backed by a Docker volume, this data is stored persistently.

### 06. Verify Volume Persistence
![06_verify_volume_persistence.png](Screenshots/06_verify_volume_persistence.png)

This screenshot confirms that the file still exists after the original container was removed and a new container mounted the same volume. This proves Docker volume persistence.

### 07. Remove Original Container
![07_remove_container.png](Screenshots/07_remove_container.png)

This screenshot shows the successful removal of the original container while preserving the Docker volume. It demonstrates that storage can survive container deletion.

### 08. Start New Container
![08_start_new_container.png](Screenshots/08_start_new_container.png)

This screenshot shows a new container being launched with the same Docker volume attached. This is a key step in validating storage reuse across container instances.

### 09. Verify Persisted Data in New Container
![09_verify_volume_persistence.png](Screenshots/09_verify_volume_persistence.png)

This screenshot confirms that the data stored in the volume remained available in the newly created container. This demonstrates storage independence from the original container lifecycle.

### 10. Container One Writes Shared Data
![10_container_one_write.png](Screenshots/10_container_one_write.png)

This screenshot shows `container_one` writing shared data into the mounted Docker volume. It demonstrates how one container can populate shared persistent storage.

### 11. Container Two Starts with Same Volume
![11_container_two_start.png](Screenshots/11_container_two_start.png)

This screenshot shows `container_two` starting with the same volume mounted at `/data`. This sets up the validation of shared storage across multiple containers.

### 12. Container Two Reads Shared Data
![12_container_two_read_shared_data.png](Screenshots/12_container_two_read_shared_data.png)

This screenshot confirms that `container_two` can read data originally written by `container_one`. This demonstrates shared, persistent storage across containers.

### 13. Cleanup Containers
![13_cleanup_containers.png](Screenshots/13_cleanup_containers.png)

This screenshot shows the removal of the temporary lab containers used during the storage test. This is good operational hygiene and helps keep the environment clean.

### 14. Verify Cleanup
![14_verify_cleanup.png](Screenshots/14_verify_cleanup.png)

This screenshot shows the result of `docker ps -a` after cleanup, confirming that the targeted lab containers were removed successfully.

### 15. Full Cleanup Complete
![15_full_cleanup_complete.png](Screenshots/15_full_cleanup_complete.png)

This screenshot verifies that no containers remain in the lab environment, confirming full cleanup of all containers involved in the exercise.

### 16. Volume Removed and Verified
![16_volume_removed_and_verified.png](Screenshots/16_volume_removed_and_verified.png)

This screenshot confirms that the Docker volume was successfully removed. The empty result from `docker volume ls` verifies that no volumes remain. Proper cleanup is important because Docker volumes persist independently of containers and can consume disk space if not removed.

---

## Key Concepts

- Docker volumes provide persistent storage
- Volumes exist independently of containers
- Multiple containers can share the same volume
- Data survives container deletion
- Cleanup is required to avoid storage issues

---

## Real-World Relevance

Docker volumes are widely used in:

- Databases (MySQL, PostgreSQL)
- Logging systems
- Microservices architecture
- Kubernetes persistent storage
- Cloud-native applications

---

## What I Learned

- How to create and manage Docker volumes
- How to persist data across containers
- How containers share data using volumes
- Importance of cleaning up containers and volumes
- Real-world container storage concepts used in DevOps and cloud environments

---
