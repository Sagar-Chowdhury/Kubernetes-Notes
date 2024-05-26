![image](https://github.com/Sagar-Chowdhury/Kubernetes-Notes/assets/76145064/ed2a56e0-050a-4e28-8ef4-8b902c143f27)

### What can Kubernetes do for you?

With modern web services, users expect applications to be available 24/7, and developers expect to deploy new versions of those applications several times a day. Containerization helps package software to serve these goals, enabling applications to be released and updated without downtime. Kubernetes helps you make sure those containerized applications run where and when you want, and helps them find the resources and tools they need to work. Kubernetes is a production-ready, open source platform designed with Google's accumulated experience in container orchestration, combined with best-of-breed ideas from the community.


![image](https://github.com/Sagar-Chowdhury/Kubernetes-Notes/assets/76145064/9b23a493-43da-40d3-818a-362b2639d4dd)

## Kubernetes Clusters
Kubernetes coordinates a highly available cluster of computers that are connected to work as a single unit.

![module_01_cluster](https://github.com/Sagar-Chowdhury/Kubernetes-Notes/assets/76145064/36413442-5996-44e3-9600-9fe9ce008c03)

Kubernetes is a production-grade, open-source platform designed to orchestrate the placement (scheduling) and execution of application containers within and across computer clusters. It automates the distribution and scheduling of application containers, allowing for more efficient and flexible deployment models compared to traditional methods where applications were installed directly onto specific machines.

#### Key Components of a Kubernetes Cluster

1. **Control Plane**
    - **Role**: Manages the entire cluster.
    - **Functions**: 
        - Scheduling applications
        - Maintaining the desired state of applications
        - Scaling applications
        - Rolling out updates
    - **Components**:
        - API Server: Exposes the Kubernetes API.
        - etcd: A consistent and highly available key-value store used as Kubernetes' backing store for all cluster data.
        - Controller Manager: Runs controller processes.
        - Scheduler: Assigns workloads to specific nodes.

2. **Nodes**
    - **Role**: Worker machines that run applications.
    - **Types**: Can be either Virtual Machines (VMs) or physical computers.
    - **Components**:
        - Kubelet: An agent that manages the node and communicates with the control plane.
        - Container Runtime: Tools like containerd or CRI-O that handle container operations.
    - **Recommendations**: For production, a minimum of three nodes is recommended to ensure redundancy and availability. This setup prevents the loss of an etcd member and a control plane instance if one node goes down.


#### Minikube

- **Purpose**: A lightweight Kubernetes implementation for local development.
- **Functionality**: 
    - Creates a VM on your local machine.
    - Deploys a simple cluster with only one node.
- **Availability**: 
    - Compatible with Linux, macOS, and Windows systems.
- **CLI Operations**: 
    - Includes commands for starting, stopping, checking the status, and deleting the cluster.

