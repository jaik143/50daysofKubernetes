# 🌟 Day 2 - Dockerizing a Full-Stack Application 🐳

Welcome to **Day 2** of my **#50DaysOfKubernetes** challenge!  
Today, I focused on **Dockerizing a full-stack TODO application** — an essential step before deploying it to Kubernetes.

---

## 🔧 What I Accomplished

✅ Created a **custom Docker image** for my TODO app  
✅ Tagged and **pushed the image to Docker Hub**  
✅ **Ran the app container** using Docker  
✅ Accessed the live app on `localhost:3000` using port mapping  

---

## 💡 Key Takeaways

- Dockerizing applications makes them portable and production-ready.
- Tagging and pushing to Docker Hub is crucial for CI/CD and Kubernetes deployment.
- Port mapping allows access to services inside containers via local ports.
- Reinforced understanding of the **Docker CLI** and **container lifecycle**.

---

## 🧪 Practiced Commands

```bash
docker build -t jaik143/todo-app:latest .
docker images
docker login
docker tag todo-app jaik143/todo-app:latest
docker push jaik143/todo-app:latest
docker run -d -p 3000:3000 jaik143/todo-app:latest
```

## 🔗 LinkedIn Post

📣 [LinkedIn Post – Day 2](https://www.linkedin.com/posts/jayanth-kadali-419798182_50daysofkubernetes-docker-containerization-activity-7345468180468797440-tfPG)
