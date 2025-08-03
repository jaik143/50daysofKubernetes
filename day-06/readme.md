# ☸️ Day 6/50 – Multi-Node Cluster, Multi-Container Pods & Context Switching

Welcome to Day 6 of my **#50DaysOfKubernetes** Challenge!  
Today was all about **setting up a multi-node cluster**, creating **multi-container pods**, and learning how to switch between **Kubernetes contexts** efficiently.

---

## 🧠 What I Learned

### 🔹 1. Multi-Node Kubernetes Cluster

A **multi-node cluster** consists of:
- **1 Master Node** (Control Plane)
- **1 or more Worker Nodes**

💡 Multi-node clusters are ideal for real-world workloads and simulate how Kubernetes behaves in production.




### 🔹 3. Kubernetes Context Switching

When managing **multiple clusters**, we use **contexts** to switch between them using the `~/.kube/config` file.

---

## ⚙️ Setup: Multi-Node Cluster

If using Minikube or KIND:

```bash
# KIND example:
kind create cluster --name my-cluster --config=multi-node.yaml


!(images/day-005.png)