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


#### Explain the Cluster architecture




# Common pod issues in Kubernetes and their resolutions

#### 1. Kubernetes is unable to pull the container image:-
Check image name: Ensure the image name and tag are correct.
Check image registry: Ensure the image is available in the specified container registry.
Credentials: If the image is in a private registry, make sure the proper image pull secret is configured and associated with the pod.
Command: Use kubectl describe pod <pod-name> to see the exact error message related to image pulling.

#### 2. Pods keep crashing and restarting:-
Check logs: Use kubectl logs <pod-name> to check the application logs for errors.
Describe the pod: Use kubectl describe pod <pod-name> to get more detailed information about the pod's state and recent events.
Resource limits: Ensure the pod has enough CPU and memory. Adjust resources.requests and resources.limits in the pod spec if necessary.
Health checks: Ensure your readiness and liveness probes are correctly configured to reflect the application's state.

#### 3. Pods are being killed due to running out of memory:-
Resource limits: Set appropriate resources.requests and resources.limits for memory in the pod spec.
Memory leaks: Check your application for memory leaks or inefficiencies.
Monitoring: Use tools like Prometheus and Grafana to monitor memory usage and adjust the resources accordingly.

#### 4. Pods remain in the "Pending" state and are not scheduled:-
Resource availability: Ensure there are enough resources (CPU, memory) available in the cluster to schedule the pod. Check with kubectl describe nodes.
Node selectors and affinities: Verify that any node selectors, affinities, or taints and tolerations are correctly configured and match available nodes.
Cluster capacity: If the cluster is running out of resources, consider scaling up the cluster by adding more nodes.

#### 5. Pods are not scheduled because nodes are in the "NotReady" state:-
Node status: Check the status of nodes with kubectl get nodes.
Kubelet status: Ensure the kubelet service is running on the node.
Network issues: Check for network connectivity issues between the node and the control plane.
Node health: Investigate node-specific issues such as disk pressure, memory pressure, or PID pressure.



# Kubernetes common errors:

#### 1. CrashLoopBackOff:
- Description: A pod repeatedly crashes and restarts.
- Troubleshooting:
- Check pod logs: `kubectl logs <pod-name>`.
- Describe the pod for more details: `kubectl describe pod <pod-name>`.
- Investigate the application's start-up and initialization code.

#### 2. ImagePullBackOff:
- Description: Kubernetes cannot pull the container image from the registry.
- Troubleshooting:
- Verify the image name and tag.
- Check the image registry credentials.
- Ensure the image exists in the specified registry.

#### 3. Pending Pods:
- Description: Pods remain in the "Pending" state and are not scheduled.
- Troubleshooting:
- Check node resources (CPU, memory) to ensure there is enough capacity.
- Ensure the nodes are labeled correctly if using node selectors or affinities.
- Verify there are no taints on nodes that would prevent scheduling.
#### 4. Node Not Ready:
- Description: One or more nodes are in a "NotReady" state.
- Troubleshooting:
- Check node status: `kubectl describe node <node-name>`.
- Review kubelet logs on the affected node.
- Ensure the node has network connectivity.

#### 5. Service Not Working
- Description: Services are not accessible or routing traffic correctly.
- Troubleshooting:
- Check the service and endpoints: `kubectl get svc` and `kubectl get endpoints`.
- Verify network policies and firewall rules.
- Ensure the pods backing the service are healthy and running.

#### 6. Insufficient Resources:
- Description: Pods cannot be scheduled due to insufficient resources.
- Troubleshooting:
- Review resource requests and limits in pod specifications.
- Scale the cluster by adding more nodes.

#### 8. PersistentVolume Claims Pending:
- **Description**: PVCs remain in a "Pending" state.
- **Troubleshooting**:
- Check if there are available PVs that match the PVC specifications.
- Ensure the storage class exists and is configured correctly.
- Verify that the underlying storage backend is healthy.

#### 9. **Pod Stuck Terminating**:
- **Description**: Pods get stuck in a "Terminating" state.
- **Troubleshooting**:
- Check for finalizers that might be preventing pod deletion.
- Review the logs for shutdown hooks or long-running processes.
- Force delete the pod if necessary: `kubectl delete pod <pod-name> --force --grace-period=0`.

#### 10. **DNS Resolution Issues**:
- **Description**: DNS lookups within the cluster fail.
- **Troubleshooting**:
- Check the DNS pod logs (e.g., CoreDNS): `kubectl logs <coredns-pod>`.
- Ensure the DNS service is running: `kubectl get svc -n kube-system`.
- Verify network policies and firewall rules do not block DNS traffic.



#### HELM
Helm is a powerful package manager for Kubernetes that helps you manage Kubernetes applications. Helm uses a packaging format called charts, which are collections of files that describe a related set of Kubernetes resources.


