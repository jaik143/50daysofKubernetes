# 📦 Day 3/40 - Multi-Stage Docker Build

Welcome to **Day 3** of my **50 Days Kubernetes Challenge**!

---

## 🧠 What I Learned

Today I learned how to use **Multi-Stage Docker Builds** to create lightweight, production-ready Docker images.  
This involves:

- Building a React application using Node.js in the **first stage**.
- Serving the final build using **NGINX** in the **second stage**.
- Reducing image size and separating build-time dependencies from the final image.

---

## 📂 Project Used

Cloned from:  
🔗 (https://github.com/piyushsachdeva/todoapp-docker)

---

## 📜 Dockerfile

```dockerfile
# Stage 1: Build the app
FROM node:18-alpine AS installer
WORKDIR /app
COPY package*.json ./
RUN npm install 
COPY . .
RUN npm run build

# Stage 2: Serve with NGINX
FROM nginx:latest AS deployer
COPY --from=installer /app/build /usr/share/nginx/html
