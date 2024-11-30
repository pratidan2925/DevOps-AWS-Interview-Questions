# Kubernetes

#### 1. Difference between Docker and Kubernetes
- Docker is a container platform while Kubernetes is a container orchestration platform.
- Kubernetes offers features like auto healing, auto scaling, cluster management, and enterprise capabilities.
  
---
#### 2.Cloud Control Manager in Kubernetes
- On a broad level, you can divide the kubernetes components in two parts

1. Control Plane (API SERVER, SCHEDULER, Controller Manager, C-CM, ETCD)

2. Data Plane (Kubelet, Kube-proxy, Container Runtime)
---
#### 3. What are the main differences between the Docker Swarm and Kubernetes?

- Kubernetes is better suited for large organisations as it offers more scalability, networking capabilities like policies and huge third party ecosystem 
---
#### 4.Difference between Docker container and Kubernetes pod
- A pod is a runtime specification in Kubernetes written in YAML files
- A pod can have one or multiple containers that can communicate using the same network and share resources
---
#### 5.What is a namespace in Kubernetes ?

- In Kubernetes namespace is a logical isolation of resources, network policies, rbac and everything. For example, there are two projects using same k8s cluster. One project can use ns1 and other project can use ns2 without any overlap and authentication problems.

---
#### 6.Three different types of services in Kubernetes: cluster IP mode, node Port mode, and load balancer mode.
- Cluster IP mode allows access to the service only within the Kubernetes cluster.
- Node Port mode enables access to the service using the Node IP and port number defined in the service.yaml file.
- When a service is created a NodePort type, The kube-proxy updates the IPTables with Node IP address and port that is chosen in the service configuration to access the pods.
- Where as if you create a Service as type Load Balancer, the cloud control manager creates a external load balancer IP using the underlying cloud provider logic in the C-CM.

- Users can access services using the external IP

####  7.What is the role of kube proxy?

- Kube-proxy works by maintaining a set of network rules on each node in the cluster, which are updated dynamically as services are added or removed. When a client sends a request to a service, the request is intercepted by kube-proxy on the node where it was received. Kube-proxy then looks up the destination endpoint for the service and routes the request accordingly.

- Kube-proxy is an essential component of a Kubernetes cluster, as it ensures that services can communicate with each other.
---
#### 8. What is the role of Kubelet?
- Kubelet manages the containers that are scheduled to run on that node. It ensures that the containers are running and healthy, and that the resources they need are available.

- Kubelet communicates with the Kubernetes API server to get information about the containers that should be running on the node, and then starts and stops the containers as needed to maintain the desired state. It also monitors the containers to ensure that they are running correctly, and restarts them if necessary..
---
#### 9.Day-to-day activities on Kubernetes
- We manage Kubernetes clusters and ensure application deployment with monitoring.
- We troubleshoot issues related to pods, services, and routing traffic. We also perform maintenance activities for worker nodes.
---
