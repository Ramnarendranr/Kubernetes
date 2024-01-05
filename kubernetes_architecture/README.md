# Kubernetes architecture
my notes on kubernetes


There are totally **8 components** in kubernetes architecture and that's why kubernetes architecture is also called as k8s architecture.

Architecture is divided into **control plane and data place.**

control place is also called as **master nod**e and data plane is also known as **worker node**.

the main components in worker node are:
  1. **kube-proxy**: responsible for networking, generating ip address ,load balancing, uses ip tables
  2. **kubelet**: creation of pods and ensures pods are always in running state.
  3. **Container runtime**: running your container.

Components in master node are:
  1. **API server**: exposes the Kubernetes/heart of Kubernetes
  2. **Scheduler**: scheduling pods or resources in Kubernetes, scheduling is done by API server (serve on which slave/worker node)
  3. **etcd**: key value store (backup) , stored as objects or key value pairs
  4. **controller manager**: to control the automated process such as autoscaling/autohealing
  5. **cloud controller manager**: manages the cloud platform that’s linked to/with Kubernetes.

