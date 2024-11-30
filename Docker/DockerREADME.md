## **What is Docker ?**

Docker is an open-source platform that enables developers to automate the deployment, scaling, and management of applications in lightweight, portable containers. Docker containers package software and its dependencies in a standardized unit, ensuring that the application runs consistently across different environments, whether on a developer's laptop, on-premises servers, or in the cloud.

## **What is the use of Docker ?**

Consistent Environment: Docker ensures that applications run the same in development, testing, and production environments by packaging the application and its dependencies in a container.
Isolation: Containers provide process and resource isolation, enabling multiple applications or services to run on the same host without interfering with each other.
Portability: Docker containers can run on any system that supports Docker, making it easy to move applications between environments or cloud providers.
Scalability: Docker facilitates the scaling of applications by allowing the creation of multiple container instances, which can be managed by orchestration tools like Kubernetes and Docker Swarm.
Efficiency: Containers are lightweight and use fewer resources compared to virtual machines because they share the host system's OS kernel.
Continuous Integration and Continuous Deployment (CI/CD): Docker integrates well with CI/CD pipelines, enabling automated testing, building, and deployment of applications.

## **What is a Container?**

A container is a lightweight, standalone, and executable software package that includes everything needed to run a piece of software, including the code, runtime, system tools, libraries, and settings. Containers provide an isolated environment for running applications, ensuring that they run consistently regardless of the host environment.

## **Explain the difference between COPY and ADD in a Dockerfile.**

Answer: Both COPY and ADD are used to copy files from the host to the Docker image, but ADD has additional functionalities. ADD can copy files from a URL and automatically extract tar archives, while COPY simply copies files and directories.


## **What is different between p and P in docker**

-p(small) <host_port>:<container_port>: This flag is used to map a specific port on the host machine to a specific port on the Docker container. For example, -p 8080:80 maps port 8080 on the host to port 80 on the container. This is useful when you need to expose a particular port of your application to the outside world or other services.
-P(Capital): This flag is used to publish all exposed ports of the container to random ports on the host machine. Docker will automatically assign high-order, dynamically allocated ports (above 32767) to each exposed port within the container. For example, if a container has multiple exposed ports, using -P will map each of them to a unique, random port on the host.
-p(small): Maps a specific port of the host to a specific port of the container.
-P(Capital): Maps all exposed ports of the container to random ports on the host.

## **Docker image vs docker stack**

Docker Image: An image is a read-only template with instructions for creating a Docker container. It contains the application code, libraries, dependencies, tools, and other files needed to run the application. Images are created from a Dockerfile and are the basis for creating containers.
Docker Stack: A stack is a collection of multiple services that make up an application. It is defined using a docker-compose.yml file, which describes how to deploy and interconnect various services (containers). Docker Stack allows you to deploy a multi-container application as a single unit using Docker Swarm or Kubernetes for orchestration.

## **How to debug Docker**

Logs: Use docker logs <container_id> to retrieve the logs from a specific container. This helps in understanding what happened inside the container.
Exec into Container: Use docker exec -it <container_id> /bin/bash to get an interactive shell inside the running container. This is useful for manual inspection and troubleshooting.
Inspect: Use docker inspect <container_id> to get detailed information about the container’s configuration, state, and networking. This command provides JSON output with extensive details.
Check Docker Daemon Logs: Review Docker daemon logs using journalctl -u docker.service or sudo cat /var/log/docker.log (location may vary by system).
Network Troubleshooting: Use commands like docker network ls, docker network inspect, and docker network connect to diagnose and resolve network issues.

## **You login in office .. and see that your docker container is not available what will you do**

Check Docker Service: Ensure Docker is running using systemctl status docker or service docker status.
List Containers: Use docker ps -a to list all containers, including stopped ones, to see if the container has stopped or failed.
Start/Restart Docker: If Docker service is not running, restart it using systemctl restart docker.
Container Logs: Check the logs of the container using docker logs <container_id> to understand why it stopped.
Inspect Container: Use docker inspect <container_id> to get detailed information and potential reasons for the issue.
Check System Resources: Ensure that there are enough system resources (CPU, memory, disk space) available for Docker.

## **How to orchestrate DOCKER container**

Docker Swarm: A native clustering and orchestration tool for Docker. It allows you to create a swarm of Docker nodes and manage them as a single cluster, distributing containers across the nodes, scaling services, and managing the lifecycle of containers.
Commands:
docker swarm init: Initialize a new swarm.
docker service create: Deploy a new service in the swarm.
docker service scale: Scale services up or down.
Kubernetes: An open-source platform for automating deployment, scaling, and operations of application containers across clusters of hosts. It provides advanced orchestration capabilities, including self-healing, scaling, and load balancing.
Components:
Pods: The smallest deployable units that can contain one or more containers.
Services: A way to expose an application running on a set of pods as a network service.
Deployments: Manage the deployment and scaling of a set of pods.

## **What is docker application**

A Docker application is a software application packaged in a Docker container. This container includes everything the application needs to run, such as the code, runtime, libraries, environment variables, and configuration files. Docker applications can be easily deployed, scaled, and managed across different environments, ensuring consistency and reliability
How to create docker image from docker container
Commit the Container: Use docker commit <container_id> <new_image_name> to create a new image from the changes made in a running container. This captures the current state of the container as a new image.
Tag and Push (Optional): Tag the new image and push it to a Docker registry if you want to share it.

## **What is docker policy to start docker container automatically**

Docker provides restart policies to control whether your containers start automatically when they exit, or when Docker restarts. These policies can be set using the --restart flag:
no: Do not automatically restart the container (default).
on-failure: Restart the container only if it exits with a non-zero exit status. You can optionally specify the maximum number of restart attempts (e.g., on-failure:5).
always: Always restart the container regardless of the exit status.
unless-stopped: Always restart the container except when the container is manually stopped.
Example:
docker run --restart=always my_image
These policies help ensure that your containers remain running and are resilient to failures or system restarts.

## **How to change Docker file access?**

Use the command chmod to modify file access:
Example: chmod 644 Dockerfile to set read and write permissions.

## **What is the use of a multistage Dockerfile, and how to create it?**
Multistage Dockerfile helps in optimizing image size by using multiple stages to build an image. The final image contains only necessary binaries.
Dockerfile
Copy code
FROM golang:alpine AS builder
WORKDIR /app
COPY . .
RUN go build -o app


FROM alpine
WORKDIR /app
COPY --from=builder /app/app .
CMD ["./app"]


### **Apache service is running on Docker and showing errors, how to resolve that? What are common errors?**
Check Logs: Use docker logs <container_id> to inspect logs.
Common Errors:
"403 Forbidden": Check file permissions.
"404 Not Found": Verify the document root and file existence.
"502 Bad Gateway": Ensure the backend services are available.


## **Difference between CMD and ENTRYPOINT**
CMD: Provides defaults for an executing container. It can be overridden by arguments passed during container run. Example: CMD ["echo", "Hello World"]
ENTRYPOINT: Sets a command that will always run and cannot be overridden. It ensures the container runs as intended. Example: ENTRYPOINT ["python", "app.py"]

## What is Docker?
 Docker is a platform for developing, shipping, and running applications inside lightweight, portable containers.
 
## What is a Docker Container? 
A Docker container is a lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, runtime, libraries, and settings.

## What are Docker Images?
 Docker images are read-only templates used to create containers. They include the application code, libraries, and dependencies.
 
## What is Docker Hub? 
Docker Hub is a cloud-based registry service for storing and sharing Docker images. It allows users to find, manage, and distribute container images.
## Explain Docker Architecture?
 Docker architecture includes:
Docker Client: CLI that users interact with.
Docker Daemon: Runs on the host machine and manages Docker objects like images, containers, networks, and volumes.
Docker Registry: Stores Docker images.
Docker Objects: Images, containers, networks, and volumes.

## What is a Dockerfile?
 A Dockerfile is a text file containing a set of instructions to build a Docker image. It specifies the base image, dependencies, configurations, and commands to run within the container.
Tell us something about Docker Compose.
 Docker Compose is a tool for defining and running multi-container Docker applications. It uses a YAML file to configure the application's services, networks, and volumes.

## What is Docker Swarm?
 Docker Swarm is a native clustering and orchestration tool for Docker. It allows you to create and manage a cluster of Docker nodes as a single virtual system.

## What is a Docker Namespace? 
Namespaces provide isolation for containers by ensuring that a container's processes, filesystems, user IDs, and network interfaces are separated from those of other containers and the host system.

## What is the lifecycle of a Docker Container?
Create: Create a container from an image.
Start: Run the container.
Pause: Pause the container's processes.
Unpause: Resume the container's processes.
Stop: Stop the container.
Kill: Forcefully stop the container.
Remove: Delete the container.

## What is Docker Machine?
 Docker Machine is a tool that simplifies the installation of Docker on virtual hosts and provisions Docker hosts on local and cloud infrastructure.

## How to check for Docker Client and Docker Server version? 
Run the command docker version.

## How do you get the number of containers running, paused, and stopped?
 Use the command docker ps -a -f "status=running" for running containers, docker ps -a -f "status=paused" for paused containers, and docker ps -a -f "status=exited" for stopped containers.

## If you vaguely remember the command and you’d like to confirm it, how will you get help on that particular command?
 Use the command docker <command> --help.

## How to login into the docker repository?
 Use the command docker login and provide your Docker Hub credentials.

## How do you create a docker container from an image?
 Use the command docker run <image_name>.

## Once you’ve worked with an image, how do you push it to docker hub? 
Tag the image with your repository name using docker tag <image_id> <repository_name> and then push it using docker push <repository_name>.

## How to build a Dockerfile? 
Create a text file named Dockerfile with the necessary instructions and then build it using docker build -t <image_name> ..

## Do you know why the docker system prune is used? What does it do? 
docker system prune is used to remove unused data (e.g., stopped containers, networks, dangling images). It helps free up disk space.

## Will you lose your data when a docker container exists? 
Yes, unless the data is stored in a volume or bind mount, data in the container is lost when it is removed.

## Where do you think Docker is being used?
Application development and deployment
Continuous Integration/Continuous Deployment (CI/CD)
Microservices architecture
Testing and development environments
Cloud-based applications

## How is Docker different from other containerization methods? 
Docker offers a complete ecosystem with easy-to-use CLI tools, a centralized registry (Docker Hub), and wide community support, making it simpler to use compared to other containerization methods.

## Can I use JSON instead of YAML for my compose file in Docker? 
No, Docker Compose uses YAML for defining services, networks, and volumes.
## How have you used Docker in your previous position? 
(Provide a specific example from your experience, such as using Docker for CI/CD pipelines, microservices, etc.)

## How far do Docker containers scale? Are there any requirements for the same? 
Docker containers can scale horizontally with orchestration tools like Docker Swarm or Kubernetes. Requirements include sufficient compute resources and proper configuration of the orchestration tool.

## What platforms does docker run on?
Docker runs on Linux, Windows, and macOS.

## Is there a way to identify the status of a Docker container? 
Use the command docker ps to see the status of running containers and docker inspect <container_id> for detailed status.

## Can you remove a paused container from Docker?
 Yes, you can remove a paused container using the command docker rm -f <container_id>.

## Suppose you have an application that has many dependent services. Will docker compose wait for the current container to be ready to move to the running of the next service?
 Yes, Docker Compose can be configured to wait for dependencies using the depends_on option and health checks.

## How will you monitor Docker in production? 
Use monitoring tools like Prometheus, Grafana, or Docker's built-in stats command (docker stats).

## Is it a good practice to run Docker compose in production?
 Generally, it's better to use orchestration tools like Kubernetes or Docker Swarm in production for better scalability and management.

## What changes are expected in your docker compose file while moving it to production?
Define production-ready services and configurations
Use environment variables for sensitive data
Optimize resource allocations (e.g., CPU, memory limits)
Implement proper logging and monitoring configurations
Use external databases and services instead of local ones
