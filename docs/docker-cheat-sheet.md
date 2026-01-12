# 🐳 Docker Cheat Sheet

A quick reference guide for working with Docker — covering essential commands for building, managing containers, networking, and more.

---

## 🛠️ Build Commands

| Command | Description |
|--------|-------------|
| `docker build .` | Builds an image from a Dockerfile in the current directory |
| `docker build https://github.com/docker/rootfs.git#container:docker` | Builds an image from a remote Git repository |
| `docker build -t imagename:tag .` | Builds and tags an image for easier tracking |
| `docker build https://yourserver/file.tar.gz` | Builds an image from a remote tar archive |
| `docker build -t image:1.0 -<<EOF ... EOF` | Builds an image from a Dockerfile via STDIN |

---

## 🧹 Clean-Up Commands

| Command | Description |
|--------|-------------|
| `docker image prune` | Removes unused images |
| `docker image prune -a` | Removes all images not used by any containers |
| `docker system prune` | Removes stopped containers, unused networks, dangling images, and build cache |
| `docker image rm <image>` | Removes an image |
| `docker rm <container>` | Removes a container |
| `docker kill $(docker ps -q)` | Stops all running containers |
| `docker rm $(docker ps -a -q)` | Removes all stopped containers |
| `docker volume rm $(docker volume ls -f dangling=true -q)` | Removes all dangling volumes |

---

## 🧩 Container Interaction

| Command | Description |
|--------|-------------|
| `docker start <container>` | Starts a container |
| `docker stop <container>` | Stops a container |
| `docker pause <container>` | Pauses a container |
| `docker unpause <container>` | Unpauses a container |
| `docker restart <container>` | Restarts a container |
| `docker wait <container>` | Waits for a container to stop and prints its exit code |
| `docker export <container>` | Exports container contents to a tar archive |
| `docker attach <container>` | Attaches to a running container |
| `docker logs -ft <container>` | Follows logs from a container |
| `docker exec -ti <container> script.sh` | Runs a command/script inside a container |
| `docker create <image>` | Creates a new container from an image |
| `docker commit -m "msg" -a "author" <container> username/image:tag` | Saves a running container as an image |
| `docker commit <container> <image>` | Creates a new image from a container |
| `docker stack rm <stackname>` | Removes a Docker Swarm stack |

---

## 🔍 Container Inspection

| Command | Description |
|--------|-------------|
| `docker ps` | Lists all running containers |
| `docker ps -a` | Lists all containers (including stopped) |
| `docker diff <container>` | Inspects file system changes in a container |
| `docker top <container>` | Shows processes in a container |
| `docker inspect <container>` | Displays detailed container info |
| `docker logs <container>` | Fetches logs from a container |
| `docker stats <container>` | Shows live resource usage stats |

---

## 📦 Manage Images

| Command | Description |
|--------|-------------|
| `docker image ls` | Lists all Docker images |
| `docker image rm <image>` | Removes an image |
| `docker tag <image> <tag>` | Tags an image |
| `docker history <image>` | Shows image history |
| `docker inspect <image>` | Inspects image metadata |

--- 

## ⚙️ Common Run Flags

| Flag | Description |
|------|-------------|
| `--detach`, `-d` | Runs container in the background |
| `--env`, `-e` | Sets environment variables |
| `--hostname`, `-h` | Sets container hostname |
| `--label`, `-l` | Adds metadata label |
| `--name` | Assigns a container name |
| `--network` | Connects container to a network |
| `--rm` | Automatically removes container on exit |
| `--read-only` | Mounts container filesystem as read-only |
| `--workdir`, `-w` | Sets working directory |

---

## 📡 Registry Commands

| Command | Description |
|--------|-------------|
| `docker login` | Authenticates to a Docker registry |
| `docker logout` | Logs out from a registry |
| `docker pull <image>` | Pulls an image from a registry |
| `docker push <repo>/<image>:tag` | Pushes an image to a registry |
| `docker search <term>` | Searches Docker Hub for images |

---

## 🚀 Run Command Syntax

```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]