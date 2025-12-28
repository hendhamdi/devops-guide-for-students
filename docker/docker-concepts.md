# 🐳 Docker Fundamentals

Docker is a **platform that allows you to package applications into containers**.  
Containers are **lightweight, portable, and isolated** environments that run the same way everywhere.

---

## 🧩 Why Docker?

- Makes it easy to **run applications consistently** on any system
- Eliminates the "**it works on my machine**" problem
- Simplifies **deployment and scaling**
- Works well with **CI/CD pipelines** and DevOps practices

---

## 🔄 Key Concepts

### Container
- A **container** is a running instance of an image  
- It includes the **application and all its dependencies**  
- Isolated from other containers and the host system

### Image
- An **image** is a blueprint for a container  
- It defines what goes into the container (OS, libraries, app)  

### Dockerfile
- A **Dockerfile** is a text file with instructions to build an image  
- Example commands: `FROM`, `COPY`, `RUN`, `CMD`

### Volume
- Used to **persist data** outside of containers  
- Example: database files

### Network
- Containers can communicate via **Docker networks**  
- Ensures secure and isolated connections

---

## 🛠️ Typical Docker Workflow

1. **Write a Dockerfile** – define your application environment  
2. **Build an image** – `docker build -t myapp .`  
3. **Run a container** – `docker run -d -p 8080:80 myapp`  
4. **Check logs** – `docker logs <container_id>`  
5. **Stop/remove container** – `docker stop <container_id>` / `docker rm <container_id>`

---

## 🖼️ Docker Concept Diagram

![Docker Image vs Container](https://user-images.githubusercontent.com/54731898/136222615-1d1c44ff-a0fe-412c-89cb-79a5a552f233.PNG "Docker Image vs Container")

*Diagram showing the flow: Dockerfile → Image → Container*

> Source: GitHub User Images


---

## 🔁 Example Dockerfile

```dockerfile
# Use Node.js official image
FROM node:18

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy application code
COPY . .

# Expose port 3000
EXPOSE 3000

# Start the app
CMD ["node", "index.js"]
```
---

## 🔑 Docker Commands Cheat Sheet

```bash
docker build -t myapp .           # Build an image
docker images                     # List images
docker run -d -p 3000:3000 myapp  # Run container
docker ps                         # List running containers
docker stop <container_id>        # Stop container
docker rm <container_id>          # Remove container
docker rmi <image_id>             # Remove image
```

---

## 📌 Summary

Docker allows you to package and run applications in isolated containers
It makes development, testing, and deployment simpler, faster, and more consistent
It is a key tool in DevOps pipelines

➡️ Next step in learning:

`ci-cd/ci-cd-basics.md` → CI/CD concepts & pipelines

