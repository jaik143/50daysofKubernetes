# 🏗️ Day 5/50 - Kubernetes Architecture Overview

Welcome to Day 5 of my **#50DaysOfKubernetes** Challenge!  
Today, I dived into the internal components of the **Kubernetes architecture**, which powers modern cloud-native deployments.

---

## 📘 What I Learned

Kubernetes follows a **master-worker architecture**, where the control plane manages the cluster and nodes run the workloads.

---

## 🧠 Core Components of Kubernetes Architecture

### 🔹 Control Plane Components (Master Node)

| Component        | Description |
|------------------|-------------|
| `kube-apiserver` | Entry point for all Kubernetes commands (REST API) |
| `etcd`           | Key-value store for cluster state/configuration |
| `kube-scheduler` | Assigns pods to worker nodes |
| `kube-controller-manager` | Handles replication, node monitoring, etc. |
| `cloud-controller-manager` | Manages cloud-specific controller logic |

---

### 🔹 Node Components (Worker Nodes)

| Component      | Description |
|----------------|-------------|
| `kubelet`      | Communicates with control plane, ensures containers run as expected |
| `kube-proxy`   | Manages networking rules for pod communication |
| `Container Runtime` | E.g., Docker or containerd, runs the actual containers |

---

### 🔁 How It All Works (In Brief)

1. **User sends request** → `kubectl` → API Server
2. **API Server stores config/state** in `etcd`
3. **Scheduler decides** which node should run the pod
4. **kubelet on node** pulls image and starts container
5. **kube-proxy handles networking** for services/pods

---

## 🖼️ Kubernetes Architecture Diagram


![Kubernetes Architecture](https://kubernetes.io/images/docs/components-of-kubernetes.svg)

---

## 📝 Key Takeaways

- Kubernetes is modular and follows **control plane + worker nodes** pattern
- The **API server** is the central hub for all operations
- **etcd** is the single source of truth for cluster state
- Workers run the actual containers, managed by the control plane

---

---

📌 **Next up:** Day 6 – Pods Deep Dive 🚀  
Stay tuned!
