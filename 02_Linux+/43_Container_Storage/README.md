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

## Screenshots & Explanations

---

### Screenshot 01 – Create Docker Volume

**Filename:**  
01_create_volume.png  

**Explanation:**  
This screenshot shows the creation of a Docker volume named `my_volume`. Docker volumes are used to store persistent data outside of containers.

---

### Screenshot 02 – List Volumes

**Filename:**  
02_list_volumes.png  

**Explanation:**  
This output confirms that the Docker volume was successfully created and is available for use.

---

### Screenshot 03 – Inspect Volume

**Filename:**  
03_inspect_volume.png  

**Explanation:**  
This output shows detailed information about the volume, including its mount location on the host system.

---

### Screenshot 04 – Run Container with Volume

**Filename:**  
04_run_container_with_volume.png  

**Explanation:**  
This command runs a container and attaches the volume to `/data`, allowing persistent storage inside the container.

---

### Screenshot 05 – Write Data to Volume

**Filename:**  
05_write_data_to_volume.png  

**Explanation:**  
This step writes data into a file located in the mounted volume directory.

---

### Screenshot 06 – Verify Written Data

**Filename:**  
06_verify_data_written.png  

**Explanation:**  
This confirms that the data was successfully written inside the container and stored in the volume.

---

### Screenshot 07 – Exit Container

**Filename:**  
07_exit_container.png  

**Explanation:**  
This step exits the container, simulating container shutdown while preserving data in the volume.

---

### Screenshot 08 – Remove Container

**Filename:**  
08_remove_container.png  

**Explanation:**  
This removes the container while keeping the Docker volume intact.

---

### Screenshot 09 – Recreate Container with Same Volume

**Filename:**  
09_recreate_container.png  

**Explanation:**  
This creates a new container and reattaches the same volume, demonstrating persistence.

---

### Screenshot 10 – Read Persisted Data

**Filename:**  
10_read_persisted_data.png  

**Explanation:**  
This confirms that data still exists after container removal, proving volume persistence.

---

### Screenshot 11 – Write Shared Data (Container One)

**Filename:**  
11_write_shared_data.png  

**Explanation:**  
This step writes data in one container to the shared volume.

---

### Screenshot 12 – Read Shared Data (Container Two)

**Filename:**  
12_container_two_read_shared_data.png  

**Explanation:**  
This output demonstrates that data written in one container persists within the Docker volume and can be accessed by another container. This confirms that Docker volumes provide shared, persistent storage independent of container lifecycle, which is critical for real-world applications such as databases, logging systems, and microservices architectures.

---

### Screenshot 13 – Remove Containers

**Filename:**  
13_cleanup_containers.png  

**Explanation:**  
This step removes all containers used in the lab to maintain a clean working environment.

---

### Screenshot 14 – Verify No Containers Remain

**Filename:**  
14_verify_cleanup.png  

**Explanation:**  
This output confirms that all containers were successfully removed from the system. The empty result from `docker ps -a` indicates a clean environment.

---

### Screenshot 15 – Full Cleanup Complete

**Filename:**  
15_full_cleanup_complete.png  

**Explanation:**  
This verifies that no containers remain in the system, confirming proper cleanup.

---

### Screenshot 16 – Remove Volume

**Filename:**  
16_volume_removed_and_verified.png  

**Explanation:**  
This output confirms that the Docker volume was successfully removed. The empty result from `docker volume ls` verifies that no volumes remain. Proper cleanup of volumes is important because Docker volumes persist independently of containers and can consume disk space if not removed.

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