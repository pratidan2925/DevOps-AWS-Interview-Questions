#### Can you explain the projects you have worked on?
I have worked on projects involving:
CI/CD Pipelines: Implemented and optimized pipelines using Jenkins and GitLab CI for automated builds and deployments.
Kubernetes: Deployed and managed containerized applications, set up Helm charts for application deployment, and monitored clusters with Prometheus and Grafana.
Infrastructure Automation: Used Terraform to provision and manage cloud infrastructure on AWS, including EC2 instances, RDS, and VPCs.
Monitoring and Logging: Implemented monitoring solutions using Grafana and Prometheus, and centralized logging with ELK Stack or CloudWatch.
#### What challenges did you face during this project?
Some challenges included:
Networking Configuration: Ensuring proper networking setup and security group rules for inter-service communication.
Scaling: Configuring auto-scaling policies to handle varying loads.
Monitoring and Debugging: Implementing effective monitoring and troubleshooting for Kubernetes clusters.

 Which technologies you used in your last project and explain the flow of project
In my last project, I used Jenkins for CI/CD, Terraform for infrastructure as code, Ansible for configuration management, Docker for containerization, and Kubernetes for orchestration. The project involved setting up a continuous integration and continuous deployment pipeline where code changes were automatically tested, built, and deployed to a Kubernetes cluster. Monitoring was handled using Prometheus and Grafana, while logs were managed with ELK stack.
3. Which challenges you faced in the last project and how you tackle those challenges
One major challenge was ensuring seamless deployment without downtime. We tackled this by implementing blue-green deployment strategies using Kubernetes, where traffic was gradually shifted from the old version to the new version, allowing us to monitor the new release and roll back if necessary. Another challenge was managing infrastructure changes safely, which we addressed by implementing a strict code review process and using Terraform's plan and apply steps to preview changes before applying them.



