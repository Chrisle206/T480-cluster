# T480-cluster

**Thinkpad T480 cluster for my Kubernetes Homelab practice**  

## 🧩 What is this

T480-cluster is a home-lab project that turns a cluster of Lenovo Thinkpad T480 laptops into a Kubernetes (or similar) cluster environment — useful for learning, experimentation, and small-scale workloads. It serves as a sandbox for deploying, managing, and observing containerized applications, clusters, and services in a fully controlled environment.

## 📂 Repository Structure
/
├── apps/ # Example apps or workloads to deploy on the cluster
├── clusters/ # Cluster definitions and configuration (e.g. staging, production-like setups)
│ └── staging/ # Example staging cluster configuration
├── monitoring/ # Monitoring and controllers definitions / manifests
│ └── controllers/ # Custom controllers / monitoring tooling
└── README.md # This file


## 🚀 Why it exists / Use Cases

- Learning Kubernetes — deploy real clusters on physical machines rather than cloud VMs  
- Testing microservices or distributed workloads in a contained environment  
- Exploring cluster management, monitoring, and coordination without relying on external cloud infrastructure  
- Quickly spin up and tear down environments for development, experimentation, or CI-like workflows  

## 🛠️ Getting Started

### Prerequisites

- Lenovo Thinkpad T480 laptop (or similar machine)
- A modern OS compatible with container runtime + Kubernetes (Linux preferred)  
- Basic knowledge of Kubernetes (or willingness to learn)  
- Network setup allowing cluster communication between nodes  

### Quick Setup (example flow)

1. Prepare each node — install Linux, Docker or container runtime, `kubeadm` (or your preferred distribution tool).  
2. From a designated “master / control-plane” node: initialize the cluster (e.g. `kubeadm init`, or use a distro like `k3s`/`k3d`, etc.).  
3. Join worker nodes.  
4. Deploy example workloads from `apps/`.  
5. (Optional) Set up monitoring or controllers defined under `monitoring/`.  

> **Note**: Exact commands depend on your chosen Kubernetes flavor / container runtime / OS. This repo doesn’t prescribe a rigid setup — it’s meant for experimentation.  

## ✅ What’s Included / What’s Working

- Cluster configurations under `clusters/` (e.g. staging)  
- Example apps/workloads under `apps/`  
- Monitoring / controllers setup under `monitoring/`  
- Modular layout that allows adding more clusters, workloads or tooling as needed  

## ⚠️ What’s *Not* Included (or Known Limitations)

- No guarantee of production-grade stability or reliability — intended for homelab / learning use only.  
- No automated installer or “one-click” setup (you must manually provision OS + cluster).  
- Hardware-specific (designed for Thinkpad T480) — other hardware may behave differently.  
- No guarantees about network, security, or backup — treat this as a playground, not production.  

## 🎯 Intended Audience

- Developers learning Kubernetes, containers, distributed systems  
- Tech hobbyists experimenting with clustering, homelab setups  
- Anyone wanting a small-scale environment for testing containerized workloads  


Happy clustering! 🖥️🖥️🖥️  
