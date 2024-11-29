# Kubernetes
---
#### Difference between Docker and Kubernetes
- Docker is a container platform while Kubernetes is a container orchestration platform.
- Kubernetes offers features like auto healing, auto scaling, cluster management, and enterprise capabilities.
---
#### Cloud Control Manager in Kubernetes
- Cloud Control Manager is responsible for managing default controllers in Kubernetes.
- Cloud Control Manager helps in implementing Kubernetes on cloud providers, allowing them to contribute to the logic for specific services like load balancers.
---
#### QProxy updates IP tables to route requests from a node Port service to Pods
- Container runtime is required for containers to run
- Kubernetes supports multiple container runtimes, including Docker shim
---
#### Difference between Docker container and Kubernetes pod
- A pod is a runtime specification in Kubernetes written in YAML files
- A pod can have one or multiple containers that can communicate using the same network and share resources
---
#### Namespace provides logical isolation of resources in a Kubernetes cluster.
- Namespace allows multiple projects and teams to work within the same Kubernetes cluster.
- Developers within a namespace have logical separation and can work on their respective projects.
---
#### Q proxy is responsible for routing requests to pods using IP tables.
- Q proxy updates the IP tables on every Linux machine.
- By default, IP tables are used for routing in Kubernetes.
---
#### Three different types of services in Kubernetes: cluster IP mode, node Port mode, and load balancer mode.
- Cluster IP mode allows access to the service only within the Kubernetes cluster.
- Node Port mode enables access to the service using the Node IP and port number defined in the service.yaml file.
---
#### Pod lifecycle and management in Kubernetes
- The cubelet continuously monitors the status of pods and sends notifications to the API server when a pod goes down.
- The API server informs the replica set controller to scale up the pod count if necessary.
---
#### Day-to-day activities on Kubernetes
- We manage Kubernetes clusters and ensure application deployment with monitoring.
- We troubleshoot issues related to pods, services, and routing traffic. We also perform maintenance activities for worker nodes.
---
