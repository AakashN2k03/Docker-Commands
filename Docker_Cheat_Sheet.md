# 🐳 Docker Terminal Cheat Sheet

A beginner-friendly guide to the most common Docker commands you'll use daily.

---

## 1️⃣ Check Version

```bash
docker --version
docker version   # Detailed info (Client + Server)
```

---

## 2️⃣ Images

| Command               | Purpose                           |
| --------------------- | --------------------------------- |
| `docker pull <image>` | Download an image from Docker Hub |

| Eg:1.docker pull ngnix by default latest version
2.docker pull ngnix:1.25 (version)

| `docker images` | List images on your system |
| `docker rmi <image_id>` | Remove an image |

**Example:**

```bash
docker pull ubuntu
docker images
docker rmi ubuntu
```

---

## 3️⃣ Containers

| Command                       | Purpose                                |
| ----------------------------- | -------------------------------------- |
| `docker run <image>`          | Create & run a container               |
| `docker run -d <image>`       | Run container in background (detached) |
| `docker run -it <image> bash` | Run container with interactive shell   |
| `docker ps`                   | Show running containers                |
| `docker ps -a`                | Show all containers (stopped too)      |
| `docker stop <id>`            | Stop a container                       |
| `docker start <id>`           | Start a stopped container              |
| `docker restart <id>`         | Restart a container                    |
| `docker rm <id>`              | Remove a container                     |

**Example:**

```bash
docker run -d -p 8080:80 nginx
docker ps
docker stop abc123
docker rm abc123
```

---

## 4️⃣ Volumes

| Command                       | Purpose          |
| ----------------------------- | ---------------- |
| `docker volume ls`            | List all volumes |
| `docker volume create <name>` | Create a volume  |
| `docker volume rm <name>`     | Remove a volume  |

---

## 5️⃣ Build Images

| Command                          | Purpose                     |
| -------------------------------- | --------------------------- |
| `docker build -t name:tag .`     | Build image from Dockerfile |
| `docker tag <image_id> name:tag` | Add a new tag to image      |

**Example:**

```bash
docker build -t myapp:v1 .
```

---

## 6️⃣ Logs & Exec

| Command                     | Purpose                        |
| --------------------------- | ------------------------------ |
| `docker logs <id>`          | View container logs            |
| `docker exec -it <id> bash` | Access running container shell |

---

## 7️⃣ Clean Up

| Command                  | Purpose                                                      |
| ------------------------ | ------------------------------------------------------------ |
| `docker system prune`    | Remove stopped containers, unused networks & dangling images |
| `docker system prune -a` | Remove **all** unused images and containers                  |

---

💡 **Pro Tip:**  
Always run `docker ps` before stopping or removing containers to confirm their IDs.

---
