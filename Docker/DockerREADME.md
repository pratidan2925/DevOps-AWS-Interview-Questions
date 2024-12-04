#### What is Docker ?

Docker is an open-source platform that enables developers to automate the deployment, scaling, and management of applications in lightweight, portable containers. Docker containers package software and its dependencies in a standardized unit, ensuring that the application runs consistently across different environments, whether on a developer's laptop, on-premises servers, or in the cloud.

#### What is the use of Docker ?

Consistent Environment: Docker ensures that applications run the same in development, testing, and production environments by packaging the application and its dependencies in a container.
Isolation: Containers provide process and resource isolation, enabling multiple applications or services to run on the same host without interfering with each other.
Portability: Docker containers can run on any system that supports Docker, making it easy to move applications between environments or cloud providers.
Scalability: Docker facilitates the scaling of applications by allowing the creation of multiple container instances, which can be managed by orchestration tools like Kubernetes and Docker Swarm.
Efficiency: Containers are lightweight and use fewer resources compared to virtual machines because they share the host system's OS kernel.
Continuous Integration and Continuous Deployment (CI/CD): Docker integrates well with CI/CD pipelines, enabling automated testing, building, and deployment of applications.

#### **What is a Container?**

A container is a lightweight, standalone, and executable software package that includes everything needed to run a piece of software, including the code, runtime, system tools, libraries, and settings. Containers provide an isolated environment for running applications, ensuring that they run consistently regardless of the host environment.

#### **Explain the difference between COPY and ADD in a Dockerfile.**

Answer: Both COPY and ADD are used to copy files from the host to the Docker image, but ADD has additional functionalities. ADD can copy files from a URL and automatically extract tar archives, while COPY simply copies files and directories.


#### **What is different between p and P in docker**

-p(small) <host_port>:<container_port>: This flag is used to map a specific port on the host machine to a specific port on the Docker container. For example, -p 8080:80 maps port 8080 on the host to port 80 on the container. This is useful when you need to expose a particular port of your application to the outside world or other services.
-P(Capital): This flag is used to publish all exposed ports of the container to random ports on the host machine. Docker will automatically assign high-order, dynamically allocated ports (above 32767) to each exposed port within the container. For example, if a container has multiple exposed ports, using -P will map each of them to a unique, random port on the host.
-p(small): Maps a specific port of the host to a specific port of the container.
-P(Capital): Maps all exposed ports of the container to random ports on the host.

#### **Docker image vs docker stack**

Docker Image: An image is a read-only template with instructions for creating a Docker container. It contains the application code, libraries, dependencies, tools, and other files needed to run the application. Images are created from a Dockerfile and are the basis for creating containers.
Docker Stack: A stack is a collection of multiple services that make up an application. It is defined using a docker-compose.yml file, which describes how to deploy and interconnect various services (containers). Docker Stack allows you to deploy a multi-container application as a single unit using Docker Swarm or Kubernetes for orchestration.

#### **How to debug Docker**

Logs: Use docker logs <container_id> to retrieve the logs from a specific container. This helps in understanding what happened inside the container.
Exec into Container: Use docker exec -it <container_id> /bin/bash to get an interactive shell inside the running container. This is useful for manual inspection and troubleshooting.
Inspect: Use docker inspect <container_id> to get detailed information about the container’s configuration, state, and networking. This command provides JSON output with extensive details.
Check Docker Daemon Logs: Review Docker daemon logs using journalctl -u docker.service or sudo cat /var/log/docker.log (location may vary by system).
Network Troubleshooting: Use commands like docker network ls, docker network inspect, and docker network connect to diagnose and resolve network issues.

#### **You login in office .. and see that your docker container is not available what will you do**

Check Docker Service: Ensure Docker is running using systemctl status docker or service docker status.
List Containers: Use docker ps -a to list all containers, including stopped ones, to see if the container has stopped or failed.
Start/Restart Docker: If Docker service is not running, restart it using systemctl restart docker.
Container Logs: Check the logs of the container using docker logs <container_id> to understand why it stopped.
Inspect Container: Use docker inspect <container_id> to get detailed information and potential reasons for the issue.
Check System Resources: Ensure that there are enough system resources (CPU, memory, disk space) available for Docker.

#### **How to orchestrate DOCKER container**

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

#### **What is docker application**

A Docker application is a software application packaged in a Docker container. This container includes everything the application needs to run, such as the code, runtime, libraries, environment variables, and configuration files. Docker applications can be easily deployed, scaled, and managed across different environments, ensuring consistency and reliability
How to create docker image from docker container
Commit the Container: Use docker commit <container_id> <new_image_name> to create a new image from the changes made in a running container. This captures the current state of the container as a new image.
Tag and Push (Optional): Tag the new image and push it to a Docker registry if you want to share it.

#### **What is docker policy to start docker container automatically**

Docker provides restart policies to control whether your containers start automatically when they exit, or when Docker restarts. These policies can be set using the --restart flag:
no: Do not automatically restart the container (default).
on-failure: Restart the container only if it exits with a non-zero exit status. You can optionally specify the maximum number of restart attempts (e.g., on-failure:5).
always: Always restart the container regardless of the exit status.
unless-stopped: Always restart the container except when the container is manually stopped.
Example:
docker run --restart=always my_image
These policies help ensure that your containers remain running and are resilient to failures or system restarts.

#### **How to change Docker file access?**

Use the command chmod to modify file access:
Example: chmod 644 Dockerfile to set read and write permissions.

#### **What is the use of a multistage Dockerfile, and how to create it?**
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


#### **Apache service is running on Docker and showing errors, how to resolve that? What are common errors?**
Check Logs: Use docker logs <container_id> to inspect logs.
Common Errors:
"403 Forbidden": Check file permissions.
"404 Not Found": Verify the document root and file existence.
"502 Bad Gateway": Ensure the backend services are available.


#### **Difference between CMD and ENTRYPOINT**
CMD: Provides defaults for an executing container. It can be overridden by arguments passed during container run. Example: CMD ["echo", "Hello World"]
ENTRYPOINT: Sets a command that will always run and cannot be overridden. It ensures the container runs as intended. Example: ENTRYPOINT ["python", "app.py"]

#### What is Docker?
 Docker is a platform for developing, shipping, and running applications inside lightweight, portable containers.
 
#### What is a Docker Container? 
A Docker container is a lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, runtime, libraries, and settings.

#### What are Docker Images?
 Docker images are read-only templates used to create containers. They include the application code, libraries, and dependencies.
 
#### What is Docker Hub? 
Docker Hub is a cloud-based registry service for storing and sharing Docker images. It allows users to find, manage, and distribute container images.
#### Explain Docker Architecture?
 Docker architecture includes:
Docker Client: CLI that users interact with.
Docker Daemon: Runs on the host machine and manages Docker objects like images, containers, networks, and volumes.
Docker Registry: Stores Docker images.
Docker Objects: Images, containers, networks, and volumes.

#### What is a Dockerfile?
 A Dockerfile is a text file containing a set of instructions to build a Docker image. It specifies the base image, dependencies, configurations, and commands to run within the container.
Tell us something about Docker Compose.
 Docker Compose is a tool for defining and running multi-container Docker applications. It uses a YAML file to configure the application's services, networks, and volumes.

#### What is Docker Swarm?
 Docker Swarm is a native clustering and orchestration tool for Docker. It allows you to create and manage a cluster of Docker nodes as a single virtual system.

#### What is a Docker Namespace? 
Namespaces provide isolation for containers by ensuring that a container's processes, filesystems, user IDs, and network interfaces are separated from those of other containers and the host system.

#### What is the lifecycle of a Docker Container?
Create: Create a container from an image.
Start: Run the container.
Pause: Pause the container's processes.
Unpause: Resume the container's processes.
Stop: Stop the container.
Kill: Forcefully stop the container.
Remove: Delete the container.

#### What is Docker Machine?
 Docker Machine is a tool that simplifies the installation of Docker on virtual hosts and provisions Docker hosts on local and cloud infrastructure.

## How to check for Docker Client and Docker Server version? 
Run the command docker version.

#### How do you get the number of containers running, paused, and stopped?
 Use the command docker ps -a -f "status=running" for running containers, docker ps -a -f "status=paused" for paused containers, and docker ps -a -f "status=exited" for stopped containers.

#### If you vaguely remember the command and you’d like to confirm it, how will you get help on that particular command?
 Use the command docker <command> --help.

#### How to login into the docker repository?
 Use the command docker login and provide your Docker Hub credentials.

#### How do you create a docker container from an image?
 Use the command docker run <image_name>.

#### Once you’ve worked with an image, how do you push it to docker hub? 
Tag the image with your repository name using docker tag <image_id> <repository_name> and then push it using docker push <repository_name>.

#### How to build a Dockerfile? 
Create a text file named Dockerfile with the necessary instructions and then build it using docker build -t <image_name> ..

#### Do you know why the docker system prune is used? What does it do? 
docker system prune is used to remove unused data (e.g., stopped containers, networks, dangling images). It helps free up disk space.

#### Will you lose your data when a docker container exists? 
Yes, unless the data is stored in a volume or bind mount, data in the container is lost when it is removed.

#### Where do you think Docker is being used?
Application development and deployment
Continuous Integration/Continuous Deployment (CI/CD)
Microservices architecture
Testing and development environments
Cloud-based applications

#### How is Docker different from other containerization methods? 
Docker offers a complete ecosystem with easy-to-use CLI tools, a centralized registry (Docker Hub), and wide community support, making it simpler to use compared to other containerization methods.

#### Can I use JSON instead of YAML for my compose file in Docker? 
No, Docker Compose uses YAML for defining services, networks, and volumes.
#### How have you used Docker in your previous position? 
(Provide a specific example from your experience, such as using Docker for CI/CD pipelines, microservices, etc.)

#### How far do Docker containers scale? Are there any requirements for the same? 
Docker containers can scale horizontally with orchestration tools like Docker Swarm or Kubernetes. Requirements include sufficient compute resources and proper configuration of the orchestration tool.

#### What platforms does docker run on?
Docker runs on Linux, Windows, and macOS.

#### Is there a way to identify the status of a Docker container? 
Use the command docker ps to see the status of running containers and docker inspect <container_id> for detailed status.

#### Can you remove a paused container from Docker?
 Yes, you can remove a paused container using the command docker rm -f <container_id>.

#### Suppose you have an application that has many dependent services. Will docker compose wait for the current container to be ready to move to the running of the next service?
 Yes, Docker Compose can be configured to wait for dependencies using the depends_on option and health checks.

#### How will you monitor Docker in production? 
Use monitoring tools like Prometheus, Grafana, or Docker's built-in stats command (docker stats).

#### Is it a good practice to run Docker compose in production?
 Generally, it's better to use orchestration tools like Kubernetes or Docker Swarm in production for better scalability and management.

#### What changes are expected in your docker compose file while moving it to production?
Define production-ready services and configurations
Use environment variables for sensitive data
Optimize resource allocations (e.g., CPU, memory limits)
Implement proper logging and monitoring configurations
Use external databases and services instead of local ones










#### What is the difference between virtualization and containerization?
Answer: Virtualization involves creating virtual machines (VMs) that emulate physical hardware, allowing multiple operating systems to run on a single physical machine. Each VM includes its own OS, which can lead to higher resource usage. Containerization, on the other hand, involves running multiple containers on a single OS kernel, sharing the same OS but isolated from each other. Containers are more lightweight and start faster compared to VMs.


#### How to do the port mapping to the container?
Answer: Port mapping is done using the -p or --publish flag when running a Docker container. The syntax is -p [host_port]:[container_port]. For example, docker run -p 8080:80 my-image maps port 80 inside the container to port 8080 on the host machine, allowing access to the container's service through the host's port.


#### How can you get shell access to a running container?
Answer: To get shell access to a running container, use the docker exec command. For example, docker exec -it <container_id> /bin/bash or docker exec -it <container_id> /bin/sh opens an interactive terminal session to the container, depending on the available shell in the container.


#### What is the difference between RUN and CMD in a Dockerfile?
Answer: RUN is used to execute commands during the image build process and create a new layer in the image. For example, RUN apt-get update installs packages while building the image. CMD specifies the default command to run when the container starts, but it can be overridden at runtime. For example, CMD ["nginx", "-g", "daemon off;"] starts Nginx by default when the container is launched.


#### What is a Dockerfile?
Answer: A Dockerfile is a text file containing a set of instructions for building a Docker image. It defines the base image, software packages, environment variables, commands to run, and other configurations required to create an image. The Dockerfile is used by Docker to automate the image creation process.


#### How did you create Docker Compose?
Answer: Docker Compose is used to define and run multi-container Docker applications. You create a docker-compose.yml file that specifies the services, networks, and volumes for your application. For example:
yaml
Copy code

```
version: '3'
services:
  web:
    image: nginx
    ports:
      - "8080:80"
  db:
    image: mysql
    environment:
      MYSQL_ROOT_PASSWORD: example

Run docker-compose up to start the services defined in the file.

```
#### What is the Docker namespace?
Answer: Docker namespaces provide isolation for resources between containers. For example, the net namespace isolates network interfaces, allowing containers to have their own network stack. Docker uses namespaces to ensure that containers do not interfere with each other and maintain separation between container environments.

#### What is the life cycle of a Docker container?
Answer: The lifecycle of a Docker container includes:
Create: The container is created from an image.
Start: The container is started and begins running its main process.
Run: The container executes its process and performs tasks.
Stop: The container’s main process is terminated, but the container still exists.
Remove: The container is deleted, freeing up resources. It can be removed with docker rm.


#### Why is the docker system prune used? What does it do?
Answer: docker system prune is used to clean up unused Docker objects, including stopped containers, unused networks, dangling images, and build cache. It helps reclaim disk space by removing resources that are no longer needed. Be cautious, as this command can delete data that you might need later.


#### What is the purpose of Docker Host?
Answer: The Docker Host is the machine (physical or virtual) where Docker is installed and running. It provides the environment for Docker containers to run, manage, and communicate. The Docker Host handles the execution of containers, networking, and storage. It can be a local development machine, a remote server, or a cloud instance.


#### Interviewer : You have noticed that the default Docker directory /var/lib/docker is getting full as you continue downloading images and generating logs. What Precautions you take to avoid this and tell me the steps to achieve ?

In, Our previous environment we made sure that our / space is not exceeding more that 50% and we used to store all docker Appdata in separate directory By creating an EBS volume and attaching it to instance. post that,
lsblk
fdisk disckname
lsblk
adding filesystem - mkfs.ext4 /dev/xvdf1

once done we create a directory called /dockerdata with "mkdir /dockerdata" and By adding an entry to /etc/fstab, EBS volume is mounted every time the system starts. Once all done we do the changes to the docker service directory file accordingly .

#### Interviewer :Okay, Imagine you are managing Docker images on your system. How would you list all the dangling images, and then how would you delete ?

docker images --filter=dangling=true This command shows the unwanted none files

docker images -q --filter=dangling=true This command will delete unwanted none files


#### 8. Can you write a simple Dockerfile?
```
FROM python:3.8-slim      # Use an official Python runtime as a parent image
WORKDIR /app              # Set the working directory in the container
COPY . /app   # Copy the current directory contents into the container at /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

#Make port 80 available to the world outside this container
EXPOSE 80
# Define environment variable
ENV NAME World

#Run app.py when the container launches
CMD ["python", "app.py"]

```
#### 20. What is the difference between CMD and ENTRYPOINT in Docker?
Answer:
CMD: Provides default arguments for the entrypoint. If an executable is not provided in the CMD instruction, the container will use the ENTRYPOINT executable. CMD can be overridden by passing arguments during docker run.
ENTRYPOINT: Defines the main command to run within the container. It is not overridden by arguments passed during docker run unless the --entrypoint flag is used. ENTRYPOINT is typically used to ensure that a particular command always runs.
Example:
 Dockerfile with CMD
FROM ubuntu
CMD ["echo", "Hello, World!"]

 Dockerfile with ENTRYPOINT
FROM ubuntu
ENTRYPOINT ["echo"]
CMD ["Hello, World!"]

Running docker run <image> Hi would result in:
With CMD: Hi
With ENTRYPOINT: echo Hi



#### 1. How do you handle credentials for a PHP application accessing MySQL or any other secrets in Docker?
Answer: To handle credentials securely for a PHP application accessing MySQL in Docker, I typically use Docker secrets or environment variables in conjunction with a secret management tool like AWS Secrets Manager or HashiCorp Vault. For example, if I use Docker secrets, I would store the MySQL credentials in a secret and then inject them into the container at runtime. This prevents hardcoding sensitive information in the image or source code.
Scenario: In a project, I set up a Dockerized PHP application that needed to connect to a MySQL database. I stored the MySQL credentials in AWS Secrets Manager and used a custom entrypoint script to fetch these credentials at container startup. This approach ensured that the secrets were never exposed in the source code or Docker image.

#### 2. What is the command for running container logs?
Answer: The command to view logs for a running container is:
docker logs <container_id_or_name>

To follow the logs in real-time (like tail -f), you can use the -f option:
docker logs -f <container_id_or_name>

Scenario: I often use this command while debugging applications running inside containers, particularly to monitor real-time log outputs during deployment processes or to troubleshoot issues.

#### 3. How do you ensure data persistence with Docker volumes?
Answer: Docker volumes are used to persist data generated by and used by Docker containers. A volume can be mounted to a container, allowing data to persist even if the container is stopped or removed.
Scenario: In one project, I used Docker volumes to store database data for a MySQL container. The volume was mounted to the container's /var/lib/mysql directory, ensuring that the data remained intact even when the container was updated or recreated.

#### 4. What are the key differences between Docker and Kubernetes?
Answer: Docker is a platform for developing, shipping, and running applications in containers. Kubernetes, on the other hand, is an orchestration platform that manages containerized applications across multiple hosts, providing features like load balancing, scaling, and automated rollouts.
Scenario: In my work, I use Docker for containerizing applications, while Kubernetes manages these containers at scale across a cluster of nodes. Docker handles individual containers, while Kubernetes orchestrates them for high availability and scalability.

#### **What is Docker, and how does it facilitate containerization?**
   - Answer: Docker is a platform that enables developers to package applications and their dependencies into lightweight containers. Containers are isolated environments that ensure consistency across different computing environments, from development to production.

#### 8. **How do you create Docker images, and what are best practices for Dockerfile creation?**
   - Answer: I create Docker images by writing Dockerfiles, which are text documents that specify the steps needed to assemble a Docker image. Best practices include using minimal base images, leveraging layers for caching, minimizing the number of layers, and securing the images by scanning for vulnerabilities.




#### 19. How do you handle credentials for a PHP application accessing MySQL or any other secrets in Docker?
Answer: For securely managing credentials in Docker:
Environment Variables: Store secrets as environment variables and pass them securely to the container.
Secrets Management: Use Docker secrets (with Docker Swarm) or AWS Secrets Manager to manage sensitive data.
Encrypted Files: Use encrypted configuration files or external secret management tools.
Scenario: I used AWS Secrets Manager to store and retrieve database credentials for a PHP application running in Docker, ensuring that sensitive information was not exposed in the Docker image or environment.

#### 20. What is the command for running container logs?
Answer: The command to view logs from a running Docker container is:
```
docker logs <container_id_or_name>
```
Scenario: I frequently use docker logs my_container to troubleshoot issues by checking the application logs in the container.


#### 25. Do you only update Docker images in Kubernetes, or do you also update replicas, storage levels, and CPU allocation?
Answer: In Kubernetes, I update not only Docker images but also replicas, storage, and CPU/memory allocation as needed. This is typically done by updating the Deployment or StatefulSet manifests.
Scenario: I scaled up a deployment by increasing the number of replicas and adjusted the resource requests and limits for CPU and memory to meet the increased load requirements.



#### What are the two layers in Docker?
Docker Engine: The runtime environment that runs and manages Docker containers. It includes the Docker Daemon and the Docker CLI.
Docker Images: Read-only templates used to create containers. They contain the application and its dependencies.
#### 7. Why Docker Swarm?
Answer: Docker Swarm is a native clustering and orchestration tool for Docker containers. It is used because:
Simplicity: Swarm is easy to set up and integrates seamlessly with existing Docker environments.
Native Docker Integration: It uses the same Docker CLI and API, making it familiar to Docker users.
Scalability: Swarm allows scaling applications up or down by simply adjusting the number of replicas.
High Availability: Swarm provides built-in support for high availability and load balancing.
#### Difference between Docker and container.
Docker: A platform for developing, shipping, and running applications using container technology. It includes tools and services for creating and managing containers.
Container: A lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, runtime, system tools, and libraries.
#### Have you written a Dockerfile from scratch? Tell me some commands and explain.
Example Dockerfile:
```
# Use an official base image
FROM ubuntu:20.04

# Install dependencies
RUN apt-get update && apt-get install -y \
    curl \
    git \
    vim

# Set environment variables
ENV APP_HOME /app

# Create and set working directory
WORKDIR $APP_HOME

# Copy application files
COPY . $APP_HOME

# Expose application port
EXPOSE 8080

# Define entry point
CMD ["bash"]

```
Commands Explained:
FROM: Specifies the base image.
RUN: Executes commands during the image build process.
ENV: Sets environment variables.
WORKDIR: Sets the working directory inside the container.
COPY: Copies files from the host to the container.
EXPOSE: Exposes a port for communication.
CMD: Specifies the default command to run when the container starts.
#### What is the difference between CMD and ENTRYPOINT in Docker?
CMD: Provides default arguments for the container’s entry point. It can be overridden by providing arguments when running the container. Example: CMD ["nginx", "-g", "daemon off;"].
ENTRYPOINT: Sets the default executable to be run when the container starts. It is not overridden by arguments provided at runtime. Example: ENTRYPOINT ["nginx"].
#### Can you describe your project focused on reducing Docker image sizes?
In a recent project, I optimized Docker images by:
Using Multi-Stage Builds: Split the build process into multiple stages to minimize the final image size.
Minimizing Layers: Combined commands in the Dockerfile to reduce the number of layers.
Selecting Smaller Base Images: Used lightweight base images like alpine instead of ubuntu.
Removing Unnecessary Files: Ensured that build artifacts and caches were removed in the final image.
#### What is the difference between CMD and ENTRYPOINT in a Dockerfile?
CMD: Provides default arguments for the ENTRYPOINT command or specifies the default command to run when the container starts. It can be overridden by providing arguments during container run.
ENTRYPOINT: Configures the main command that will be executed when the container starts. It defines the container’s behavior and is not easily overridden.
#### Have you used Docker Compose? How would you ensure multiple containers start in a specific sequence?
Yes, I have used Docker Compose. To ensure containers start in a specific sequence, you can use the depends_on option in the docker-compose.yml file. This defines dependencies between services and ensures that they start in the required order.
#### What is the purpose of the RUN instruction in a Dockerfile?
The RUN instruction in a Dockerfile is used to execute commands during the image build process. It allows you to install packages, configure the environment, and set up the image with the necessary tools and dependencies.
#### Can you explain Docker networking?
Docker networking allows containers to communicate with each other and with the outside world. Docker provides different network modes:
Bridge Network: Default network mode for containers, allowing communication between containers on the same host.
Host Network: Containers share the host’s network stack, bypassing network isolation.
Overlay Network: Enables communication between containers across different hosts, often used with Docker Swarm or Kubernetes.
Macvlan Network: Assigns a unique MAC address to a container, making it appear as a separate physical device on the network.

