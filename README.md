# Kubernetes 
## What is Kubernetes?
Kubernetes is an open-source container orchestration platform for automating the deployment, scaling, and management of containerized applications. It was originally developed by Google and is now maintained by the Cloud Native Computing Foundation (CNCF).
Containers are lightweight, portable, and consistent environments that package an application and its dependencies. Kubernetes helps manage and coordinate the deployment and operation of these containers at scale. It provides features such as automated load balancing, rolling updates, self-healing, and efficient scaling of applications.
## Why we use Kubernetes ?
Organizations use Kubernetes for several reasons, as it offers a range of benefits that address challenges in deploying, managing, and scaling containerized applications. Here are some key reasons why Kubernetes is widely adopted:

**1)Container Orchestration:**
Kubernetes automates the deployment, scaling, and management of containerized applications, allowing for efficient container orchestration.

**2)Automatic Load Balancing:**
Kubernetes can automatically distribute network traffic across multiple containers to ensure optimal load balancing and performance

**3)Self-Healing:**
If a container or node fails, Kubernetes can automatically detect the failure and take corrective actions, such as restarting containers on healthy nodes, to maintain application availability.

**4)Automatic Scaling:**
Kubernetes can automatically scale the number of container instances (pods) based on demand. This ensures that applications have the resources they need during periods of increased workload.

**5)Service Discovery:**
Kubernetes provides built-in service discovery mechanisms, allowing containers to find and communicate with each other without hardcoding IP addresses or ports.

**6)Rolling Updates and Rollbacks:**
Kubernetes supports rolling updates, enabling applications to be updated without downtime by gradually replacing old instances with new ones. In case of issues, rollbacks can be performed seamlessly.

**7)Declarative Configuration:**
Configuration in Kubernetes is done declaratively using YAML files, where users specify the desired state of the system. Kubernetes then works to ensure that the actual state matches the declared state.

**8)Secrets and Configuration Management:**
Kubernetes allows secure storage and management of sensitive information such as API keys, passwords, and other secrets. It also facilitates the management of configuration data.

**9)Persistent Storage:**
Kubernetes provides support for persistent storage, allowing applications to store and retrieve data persistently. This is essential for stateful applications that require long-term storage.

**10)Multi-Environment Portability:**
Kubernetes is designed to be cloud-agnostic, allowing users to deploy and manage applications consistently across various infrastructure providers, whether on-premises or in the cloud.

**11)Resource Quotas and Limits:**
Kubernetes allows users to set resource quotas and limits for individual containers, ensuring fair resource allocation and preventing resource contention.

**12)Pods and Multi-Container Applications:**
Kubernetes uses the concept of pods, which can host one or more containers that share the same network namespace. This enables the deployment of multi-container applications that need to work together.

**13)Security Policies:**
Kubernetes provides mechanisms for defining and enforcing security policies, helping organizations ensure the security of their containerized applications.

**14)Horizontal Pod Autoscaling:**
Kubernetes can automatically adjust the number of running pod instances based on CPU or memory utilization, providing efficient horizontal autoscaling.

## Architecture of Kubernetes ?
The architecture of Kubernetes is designed to provide a scalable and extensible platform for automating the deployment, scaling, and management of containerized applications. Here are the key components and concepts in the architecture of Kubernetes:

**1)	Master Node:**

The master node is responsible for managing the Kubernetes cluster. It includes several components:

**•	API Server:** The central component that exposes the Kubernetes API and serves as the primary management point for the entire cluster.

**•	Controller Manager:** Ensures that the desired state of the cluster matches the actual state by controlling various controllers.

**•	Scheduler:** Assigns work (containers) to worker nodes based on resource availability and constraints.

**2)	Worker Node (Minion or Node):**

Each worker node in the cluster is responsible for running containers and includes the following components:

**•	Kubelet:** An agent that communicates with the master node and manages containers on the node.

**•	Container Runtime:** The software responsible for running containers, such as Docker or containerd.

**•	Kube Proxy:** Maintains network rules on the host and enables communication between containers across the cluster.

**3)	etcd:**

•	A distributed key-value store that stores the configuration data of the cluster, including details about the nodes, configurations, and the state of the cluster. etcd is a crucial component for maintaining the cluster's desired state.

**4)	Kubernetes API:**

•	The Kubernetes API serves as the entry point for interacting with the cluster. Users, applications, and other components communicate with the cluster through the API, which is handled by the API server on the master node.

**5)	Controller:**

•	Controllers are responsible for monitoring the state of the cluster through the API server and making changes to the cluster to ensure that the current state matches the desired state. Examples include the Replication Controller, Deployment Controller, and StatefulSet Controller.

**6)	Kubelet:**

•	The Kubelet runs on each worker node and is responsible for ensuring that containers are running in a Pod. It communicates with the master node's API server to receive instructions and report the status of containers on the node.

**7)	Pod:**

•	A Pod is the smallest deployable unit in Kubernetes and represents a group of one or more containers that share the same network namespace and storage. Containers within a Pod can communicate with each other using localhost, making them suitable for tightly coupled applications. 

## Lifecycle of kubernetes
