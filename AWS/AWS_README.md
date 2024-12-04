# AWS

## What is AWS ?

 AWS (Amazon Web Services) is a leading cloud platform offering scalable computing, storage, and various IT services on demand, including web hosting, data storage, databases, and machine learning, known for its reliability, security, and global reach.
 Core Services:
 
 Compute: EC2 (virtual servers), Lambda (serverless computing)
 
 Storage: S3 (object storage), EBS (block storage)
 
 Databases: RDS (relational), DynamoDB (NoSQL)
 
 Networking: VPC (virtual private cloud), Route 53 (DNS service)
     
**Key Features:**

Scalability: Automatically scales resources based on demand.

Flexibility: Supports a wide range of operating systems, databases, and programming languages.

Security: Provides robust security features, including encryption, access management, and compliance certifications.

Global Reach: Operates data centers worldwide, enabling low-latency access.

 
## what is key pair

A key pair, consisting of a public key and a private key, is a set of security credentials that you use to prove your identity when connecting to an Amazon EC2 instance. 

For Linux instances, the private key allows you to securely SSH into your instance.

For Windows instances, the private key is required to decrypt the administrator password, which you then use to connect to your instance.


## what is region and Availability zone
In AWS, a region is a geographical area where AWS data centers are located. Each region consists of multiple isolated locations called Availability Zones (AZs). Availability Zones are distinct data centers within a region that are engineered to be isolated from failures in other AZs, while still being interconnected through low-latency links.
**1.       Region:**

A geographic area where AWS infrastructure is physically located.

Example: US East (N. Virginia), EU (Ireland), Asia Pacific (Tokyo).

Each region operates independently and is isolated from other regions.

**2.       Availability Zone (AZ):**

Isolated locations within a region, typically separate data centers.

Designed to be fault-tolerant, meaning failures in one AZ should not affect others.

Allows customers to run applications in multiple AZs for high availability and fault tolerance.


 
## Cli commands

aws s3 ls: Lists S3 buckets.

aws s3 cp: Copies files to/from S3

aws s3 mv: Moves files within S3.

aws s3 rm: Deletes files from S3.

aws s3 sync: Syncs local and S3 directories.

aws s3api put-bucket-acl: Sets bucket ACL permissions.

aws s3api put-bucket-versioning: Manages bucket versioning.

aws s3api list-object-versions: Lists object versions.

aws s3api create-bucket: Creates a new S3 bucket.

aws s3api delete-bucket: Deletes an S3 bucket.

aws s3api put-object: Uploads objects to S3.

aws s3api delete-object: Deletes objects from S3.
 
## 5. What is AMI

An AMI (Amazon Machine Image) is a template used to create virtual servers in Amazon Web Services (AWS). It includes the operating system, application server, and applications needed to launch an instance. AMIs can be customized and shared, making them convenient for quickly deploying pre-configured environments in the cloud.

## 6.  What is Snapshot?

A snapshot is a point-in-time copy of data in AWS services like EBS volumes or RDS databases. It's used for backups, disaster recovery, and creating new resources based on existing data.

## 7.  How to create snapshots .

To create a snapshot in AWS:

Go to the EC2 dashboard.

Select the volume you want to snapshot.

Choose "Create Snapshot."

Provide a name and description for the snapshot.

Click "Create Snapshot" to initiate the process.

Monitor the snapshot's progress in the dashboard.

Once completed, the snapshot is available for use as a backup.


## 8. Disaster Recovery (DR) in AWS:

Disaster Recovery in AWS involves strategies and tools to ensure business continuity by quickly restoring services and data in the event of a disruption. Key components include:

Backup and Restore: Regular backups using Amazon S3 and AWS Backup.

Data Replication: Use S3 Cross-Region Replication and DynamoDB Global Tables.

Automated Failover: Utilize Route 53 for DNS failover and Amazon Aurora for automatic database failover.

High Availability: Deploy resources across multiple Availability Zones (AZs) and use Auto Scaling.

Monitoring: Leverage Amazon CloudWatch for resource monitoring and AWS CloudTrail for activity tracking.

Security: Implement IAM for access control and AWS Shield/WAF for protection against attacks.

By implementing these components, AWS enables rapid recovery and minimal downtime during disasters.

## 9. RTO (Recovery Time Objective) and RPO (Recovery Point Objective):

**RTO**

Definition: The maximum time allowed to restore services after a disruption.

Purpose: Measures how quickly systems must be recovered.

Example: If RTO is 4 hours, systems must be back up within 4 hours of a failure.

**RPO**

Definition: The maximum acceptable data loss measured in time.

Purpose: Measures the amount of data that can be lost.

Example: If RPO is 1 hour, backups must ensure no more than 1 hour of data is lost.

Key Points

RTO: Focuses on recovery time.

RPO: Focuses on data loss.

Importance: Together, they guide disaster recovery planning to meet business continuity needs.


## 10. What is Disaster Management and What steps are followed to management disaster 

Disaster management in the IT sector involves planning, preparing, responding, and recovering from any incidents that can disrupt IT services and operations.
These incidents can range from natural disasters, cyber-attacks, hardware failures, to human errors. Effective disaster management ensures business continuity, minimizes downtime, and reduces data loss.

**Here are the steps typically followed in disaster management in the IT sector:**

**1. Risk Assessment and Business Impact Analysis**

Identify Risks: Identify potential threats and vulnerabilities that could impact IT infrastructure.

Assess Impact: Determine the potential impact of each risk on business operations, including financial losses, reputational damage, and operational downtime.

Prioritize Risks: Rank risks based on their likelihood and potential impact to prioritize mitigation efforts.

**2. Disaster Recovery Planning (DRP)**

Develop DRP: Create a comprehensive disaster recovery plan outlining procedures for responding to various disaster scenarios.

Define RTO and RPO: Establish Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO) to determine acceptable downtime and data loss.

Identify Critical Systems: Identify and prioritize critical systems, applications, and data that need to be recovered first.

**3. Implementation of Preventative Measures**

Backup Solutions: Implement regular data backup solutions, ensuring backups are stored offsite or in the cloud.

Redundancy: Use redundant hardware, networks, and power supplies to minimize single points of failure.

Security Measures: Enhance security measures, including firewalls, antivirus software, and intrusion detection systems, to protect against cyber threats.

**4. Disaster Response**

Activate DRP: In the event of a disaster, activate the disaster recovery plan.

Communication Plan: Ensure clear communication with stakeholders, including employees, customers, and partners, about the disaster and recovery efforts.

Incident Management: Coordinate incident response efforts, including damage assessment, resource allocation, and initial recovery steps.

**5. Disaster Recovery**

Restore Systems: Restore IT systems and data from backups or redundant systems as per the DRP.

Validate Recovery: Test restored systems and data to ensure they are fully functional and up-to-date.

Monitor Progress: Continuously monitor the recovery process to identify and address any issues.

**6. Post-Disaster Review**

Evaluate Response: Conduct a thorough review of the disaster response and recovery efforts to identify strengths and areas for improvement.

Update DRP: Update the disaster recovery plan based on lessons learned and new potential threats.

Training and Drills: Conduct regular training and disaster recovery drills to ensure readiness for future incidents.

**7. Continuous Improvement**

Regular Audits: Perform regular audits of disaster recovery processes and infrastructure to ensure compliance and readiness.

Stay Informed: Keep abreast of new technologies, threats, and best practices in disaster management to continually improve the plan.

Stakeholder Engagement: Maintain ongoing communication and collaboration with stakeholders to ensure their needs and expectations are met.

Implementing these steps helps organizations in the IT sector to be resilient in the face of disasters, ensuring minimal disruption to their operations and services.


## 11.  AWS resources and their limits.
**Compute**

EC2 Instances: 20 On-Demand instances.

EC2 Spot Instances: 20 running instances.

Elastic IP Addresses: 5 per region.

EC2 Key Pairs: 5000 key pairs per region.

**Networking**

VPCs: 5 per region.

Internet Gateways: 5 per region.

VPC Elastic Network Interfaces: 350 per region.

Route Tables: 200 per VPC.

Security Groups: 2500 per VPC.

Security Group Rules: 60 inbound and 60 outbound rules per security group.

**Storage**

S3 Buckets: 100 per account.

EBS Volumes: 5,000 per region.

EFS File Systems: 10 per account.

**Databases**

RDS Instances: 40 per region.

RDS DB Snapshots: 100 per region.

DynamoDB Tables: 256 tables per region.

**Load Balancing**

Elastic Load Balancers (Classic and ALB): 50 per region.

Application Load Balancers: 50 per region.

Network Load Balancers: 50 per region.

**Containers**

ECS Clusters: 2,000 per region.

ECS Services: 1,000 per cluster.

EKS Clusters: 100 per region.

**Serverless**

Lambda Functions: No limit on number of functions; limits on invocation and execution.

Lambda Concurrent Executions: 1,000 per region.

API Gateway APIs: 600 regional APIs per region.

**Monitoring**

CloudWatch Alarms: 5000 per region.

CloudWatch Log Groups: No limit.

CloudWatch Metrics: 10000 per region.

**Management and Governance**

CloudFormation Stacks: 200 per region.

IAM Roles: 1,000 per account.

IAM Users: 5,000 per account.

IAM Groups: 300 per account.

#  EC2

## what is EC2

Amazon EC2 (Elastic Compute Cloud) is a service provided by AWS that lets you rent virtual servers (instances) to run your applications in the cloud. 
It offers flexibility, scalability, and pay-as-you-go pricing, making it easy to launch, manage, and scale your compute capacity as needed.

## Which troubleshoot area you perform while creating EC2 instance
When creating an EC2 instance on AWS, key troubleshooting areas include:
Configuration: Ensure correct instance type, AMI, and network settings.
Networking: Verify internet access, subnet, and security group configurations.
IAM Role: Confirm proper permissions for accessing AWS services.
SSH Access: Check key pair selection and security group rules for SSH.
Instance Status: Monitor instance status and review system logs for errors.
Resource Utilization: Monitor CPU, memory, and disk usage for any anomalies.
Service Limits: Ensure you're not exceeding AWS service limits.
Region and AZ: Verify capacity and check for service disruptions or maintenance.

## 3.   How to create EC2 instance on Aws console
1. Sign in to AWS Management Console.
2. Navigate to the EC2 Dashboard.
3. Click "Launch Instance."
4. Choose an Amazon Machine Image (AMI).
5. Select an Instance Type.
6. Configure Instance Details (e.g., network settings, IAM role).
7. Add Storage (configure root volume).
8. Add Tags (optional).
9. Configure Security Group (control inbound/outbound traffic).
10. Review Instance Launch.
11. Select Key Pair (create or choose existing).
12. Launch Instance.
13. Access your instance using SSH or Remote Desktop.
Follow these steps, and you'll have an EC2 instance up and running in no time!

## 4. How to check EC2 logs
For Linux Instances:
Use SSH to connect to the instance.
Navigate to /var/log for system logs.
Use commands like cat, less, or tail to view log files.
For Windows Instances:
Use Remote Desktop to connect.
Access Event Viewer for system logs.
Check application-specific log directories for application logs.
Ensure permissions and refer to application documentation for specific log locations.


##  5.  How can you add more security to EC2 instance
To add more security to an EC2 instance:
Use Security Groups: Configure inbound and outbound traffic rules.
Enable Network ACLs: Control traffic at the subnet level.
Utilize IAM Roles: Manage access to AWS services.
Implement Encryption: Encrypt data at rest and in transit.
Regularly Update and Patch: Keep software up to date.
Use Bastion Hosts: Restrict direct access to instances.
Enable Multi-Factor Authentication: Add an extra layer of security.
Enable CloudWatch Logs: Monitor and manage instance logs centrally.
Implement Least Privilege: Restrict user permissions to necessary actions.
Regular Security Audits: Review configurations and conduct audits periodically.
These measures enhance the security of EC2 instances, protecting them from various threats.


##  6. If you have windows EC2 machine which storage you use for booting
For booting a Windows EC2 instance on AWS, you typically use Amazon Elastic Block Store (Amazon EBS) volumes as the storage for the boot volume. During the instance launch process, you specify an Amazon EBS volume as the root volume, which contains the operating system and boot files necessary for the instance to start up.


##  7. How to attach s3 to EC2 windows
To interact with Amazon S3 from an EC2 instance using the AWS CLI:
Install AWS CLI and configure credentials.
Use CLI commands like aws s3 ls to list buckets or aws s3 cp to copy files.
Ensure appropriate permissions for S3 access.
Be aware of data transfer costs and implement security best practices.
By following these steps, you can easily manage S3 resources from your EC2 instance using the AWS CLI.


## 8.  how to take backup of EC-2
To take a backup of an EC2 instance, you have a few options depending on your requirements:
Manual Snapshot:
Create a manual snapshot of the EBS volume attached to your EC2 instance using the AWS Management Console or AWS CLI.
This captures a point-in-time copy of the volume, allowing you to restore it later if needed.
Automated Snapshots:
Enable automated snapshots for the EBS volumes attached to your EC2 instance.
Set up a backup policy to automatically create snapshots on a schedule (e.g., daily, weekly).
AMI (Amazon Machine Image):
Create an AMI of your EC2 instance, which includes the root volume and any attached volumes.
This allows you to launch new instances based on the AMI, effectively creating a backup of the entire instance configuration.
Third-party Backup Solutions:
Use third-party backup solutions available in the AWS Marketplace or from other vendors.
These solutions offer additional features such as incremental backups, cross-region replication, and centralized management.
 
## 9.  What are EC2 pricing options ?
Amazon EC2 offers various pricing options:
On-Demand Instances: Pay-as-you-go with no commitments.
Reserved Instances (RI): Reserved capacity for a fixed term with significant discounts.
Spot Instances: Bid for unused capacity at discounted prices.
Dedicated Hosts: Physical servers dedicated to your use.
Savings Plans: Flexible pricing with significant discounts for consistent usage commitments.
Choose the option that best fits your workload and budget requirements.
 
## 10. Explain EC2 folder
/etc: Contains system configuration files.
/var: Holds variable data files, such as logs and temporary files.
/home: Home directories for users.
/usr: User-related programs and utilities.
/opt: Optional software packages.
/tmp: Temporary files that are cleared on reboot.
/root: Home directory for the root user.
These directories contain various files and data relevant to the operation of the EC2 instance and any applications running on it. Depending on your application and setup, you may create additional directories as needed.
 
## 11. How to resize your EC2 instance  ? / How to increase EC2 volume ?
 Resizing an EC2 instance involves changing its instance type to one with different compute, memory, or storage capacity. Here's how you can resize your EC2 instance:
Stop the Instance: Before resizing, stop your EC2 instance. You can do this through the AWS Management Console, CLI, or SDK.
Note Instance Details: Make note of important details such as the instance ID, security groups, and any attached EBS volumes.
Change Instance Type: In the AWS Management Console, navigate to the EC2 dashboard and select your instance. Click on "Actions" > "Instance Settings" > "Change Instance Type". Choose the new instance type that meets your requirements and click "Apply".
Start the Instance: Once the instance type is changed, start the EC2 instance again.
Verify Configuration: After the instance is running, ensure that all configurations and settings, such as security groups and attached volumes, are as expected.
Test and Monitor: Test the resized instance to ensure that it is functioning correctly. Monitor its performance to ensure that it meets your requirements.
Adjustments: Depending on the new instance type, you may need to make adjustments to configurations, such as adjusting auto-scaling groups or load balancers.
 
Or
"To resize an EC2 instance, you would follow these steps( for interview)
Stop the EC2 instance using the AWS Management Console or CLI.
Navigate to the EC2 dashboard and select the instance.
Click on 'Actions', then 'Instance Settings', and choose 'Change Instance Type'.
Select the new instance type that meets your requirements and click 'Apply'.
Start the instance again.
Verify the configuration and performance to ensure it meets your needs."
 
## 12. Tell me about EC2 family / EC2 Types.
The EC2 family refers to the grouping of different types of Amazon EC2 instances based on their specific characteristics and intended use cases. Each family represents a set of instance types optimized for particular computing requirements, such as
General Purpose: Balanced compute, memory, and networking.
Compute Optimized: High-performance processors for compute-heavy tasks.
Memory Optimized: High memory-to-CPU ratio for memory-intensive workloads.
Storage Optimized: High disk I/O performance for storage-heavy applications.
Accelerated Computing: GPU or FPGA instances for specialized tasks.
Instance Families: Specialized instances tailored for specific use cases, like local storage or high-frequency trading.
 

 
# IAM
 
## What is IAM?
IAM (Identity and Access Management) is a service in AWS that allows you to control access to AWS services and resources. It enables you to create and manage users, groups, and roles, define fine-grained access policies, set up multi-factor authentication (MFA), and monitor user activity.

## Difference between Authentication and Authorization
Authentication:
Authentication is the process of verifying the identity of a user or entity.
In AWS, authentication involves proving the identity of users or services attempting to access AWS resources.
This is typically done through credentials such as usernames, passwords, access keys, or temporary security tokens.
Common authentication mechanisms in AWS includAWS Identity and Access Management (IAM), AWS Single Sign-On (SSO), and Multi-Factor Authentication (MFA).
Authorization:
Authorization is the process of determining what actions a user or entity is allowed to perform after they have been authenticated.
In AWS, authorization involves granting permissions to users or services based on their identity and the policies associated with their credentials.
This is done through IAM policies, which define the permissions that users or entities have to AWS resources.
IAM policies specify what actions are allowed or denied on which AWS resources, based on various conditions such as user identity, resource attributes, and requested actions.
 
## Inline policy
An inline policy in AWS IAM is a policy directly attached to a specific IAM user, group, or role, providing granular control over permissions. It's managed within the configuration of the IAM entity to which it's attached.

## IM Manager
Identity Management (IM) Manager: This might refer to a system or software used for managing user identities, access controls, and permissions within an organization's IT infrastructure. Examples include Microsoft Active Directory, LDAP directories, or cloud-based identity management platforms.
 
# AWS Storage

## What is S3
Amazon S3 is a cloud storage service from AWS. It stores data in "buckets," with high durability and availability. Key features include:
Scalability: Handles large-scale data storage.
Security: Provides encryption and access controls.
Lifecycle Management: Automates data transition and deletion.
Storage Classes: Offers various cost-optimized storage options.
Integration: Works with other AWS services.
 
## 2.  What is Infrastructure storage
Infrastructure storage refers to the physical or virtual storage resources used to store and manage data within an IT infrastructure. It encompasses various types of storage technologies, including hard disk drives (HDDs), solid-state drives (SSDs), network-attached storage (NAS), storage area networks (SANs), and cloud storage services.

## 3.  What is snowball
 An AWS Snowball is a physical device provided by Amazon Web Services (AWS) for transferring large amounts of data to and from the AWS cloud. It's designed to help customers securely transfer terabytes or even petabytes of data in and out of AWS when traditional methods such as network transfer are not feasible due to limited bandwidth, long transfer times, or security concerns.

## 4. S3 Bucket Versioning
S3 bucket versioning is a feature in Amazon S3 that allows you to keep multiple versions of an object in a bucket. It helps protect against accidental deletion or overwrites by retaining previous versions of objects, enabling recovery, compliance, and audit trails. Each new version of an object uploaded to the bucket receives a unique version ID.

## 5. Types of S3 buckets
Amazon S3 buckets primarily come in two types
Standard S3 Bucket:
High durability and availability.
Suitable for frequently accessed data.
S3 Intelligent-Tiering Bucket:
Automatically moves data between access tiers to optimize costs.
Suitable for data with unpredictable access patterns.
Additionally, there are specialized storage classes:
S3 Standard-IA (Infrequent Access): For data accessed less often but needs quick retrieval.
S3 One Zone-IA: Lower-cost option for infrequently accessed data without multi-AZ redundancy.
S3 Glacier: Long-term archival with retrieval in minutes to hours.
S3 Glacier Deep Archive: Lowest-cost archival with retrieval in hours to days.
 

## 7.  what is data encryption in S3
Data encryption in Amazon S3 is the process of converting your data into a secure format that cannot be easily read by unauthorized users. This ensures that your data is protected both when it is stored in the cloud and when it is transmitted over the network.

## 8. Elastic block storage
Elastic Block Storage (EBS) is a block-level storage service provided by Amazon Web Services (AWS) for use with Amazon Elastic Compute Cloud (EC2) instances. It allows you to create and attach block storage volumes to EC2 instances, providing persistent storage that persists independently from the life of the instance.



## 9. EBS and EFS difference
Amazon EBS (Elastic Block Store)
Type: Block storage.
Use Case: Single EC2 instance attachment, suitable for databases and applications requiring high-performance block storage.
Performance: Various options (General Purpose SSD, Provisioned IOPS SSD, Throughput Optimized HDD, Cold HDD).
Durability: Replicated within the same Availability Zone (AZ).
Scalability: Can resize volumes; must be attached to an EC2 instance.
Amazon EFS (Elastic File System)
Type: File storage.
Use Case: Multiple EC2 instances, suitable for shared file storage, web serving, and content management.
Performance: Scales automatically with stored data, offers performance modes (General Purpose, Max I/O).
Durability: Data is stored across multiple Availability Zones.
Scalability: Automatically scales to petabytes without needing to provision capacity.
Summary:
EBS is block storage for single-instance high-performance needs.
EFS is file storage for multi-instance shared access and automatic scaling.
 
## 10. What is instance Storage
Instance Storage, also known as ephemeral storage or instance store, is a type of temporary block-level storage provided directly by the host machine on which an Amazon EC2 instance runs.

## 11. Cheapest storage
Amazon S3 Glacier
 
# IT ENVIRONMENT and GENERAL QUE

Suppose I want to  buy hardware. Which should we buy ?
Dedicated hardware.

## How does migration works in company
Software migration for upgrading or updating involves several critical steps to ensure a smooth transition while minimizing downtime and maintaining data integrity. Here's a short overview of the typical process:

 1. Planning:
    - Assessment: Evaluate the current system, software dependencies, and requirements for the upgrade.
    - Compatibility Check: Ensure the new version is compatible with existing hardware, software, and processes.
    - Backup: Perform a full backup of the current system to prevent data loss in case of issues during the upgrade.

 2. Preparation:
    - Test Environment: Set up a staging or test environment to simulate the upgrade process and identify potential issues.
    - Training: Train IT staff and end-users on new features and changes in the upgraded software.
    - Documentation: Prepare detailed documentation and a rollback plan in case the upgrade fails.

 3. Implementation:
    - Schedule Downtime: Plan for a maintenance window during off-peak hours to minimize the impact on users.
    - Install Update:Apply the upgrade or update following the software vendor’s instructions.
    - Migration Tools:Use migration tools or scripts, if necessary, to transfer data and configurations.

 4. Testing:
    - Validation: Verify that the upgrade was successful and that all critical functionalities are working as expected.
    - Performance Testing: Check system performance to ensure it meets the required standards.
    - Bug Fixes: Identify and address any issues that arose during the migration.

 5.Deployment:
    - Go Live: Once testing is successful, deploy the upgraded software to the production environment.
    - Monitoring: Closely monitor the system for any unexpected behavior or performance issues.

 6. Post-Migration:
    - User Support: Provide support to users during the transition period.
    - Review:Conduct a post-migration review to document lessons learned and improve future migration processes.

 By following these steps, IT teams can ensure a controlled and efficient software upgrade or update process, minimizing disruptions and maintaining system stability.
 
##  Role of product owner and scrum master
The Product Owner represents the customer's interests, prioritizes the backlog, communicates vision, makes feature decisions, and engages stakeholders. The Scrum Master facilitates Scrum, coaches the team, removes obstacles, leads ceremonies, protects from distractions, and promotes improvement.
The Product Owner focuses on "what" the team builds (backlog and priorities), while the Scrum Master focuses on "how" the team works (process and facilitation).
 
# ROUTE 53

## What is Route 53
Amazon Route 53 is a scalable and highly available Domain Name System (DNS) web service provided by AWS. It effectively translates domain names (like example.com) into the numerical IP addresses needed for computers to communicate with each other. Here are some key features of Route 53:
DNS Routing: Maps human-readable domain names to IP addresses.
Health Checks and Monitoring: Automatically reroutes traffic if a resource is unhealthy.
Traffic Flow: Provides advanced traffic management capabilities, such as weighted, latency-based, geolocation, and failover routing.
Domain Registration: Allows users to register domain names directly.


## Explain policies of Route 53

Simple Routing: Directs traffic to a single resource.
Weighted Routing: Distributes traffic based on set weights.
Latency-based Routing: Routes traffic to the resource with the lowest latency.
Failover Routing: Redirects traffic to a standby resource if the primary is unavailable.
Geo location Routing: Routes traffic based on user location.
Geo Proximity Routing: Directs traffic based on the geographic location of resources and users.
Multi-Value Answer Routing: Provides multiple IP addresses for redundancy.

## How domain name is resolved to IP address by Route 53

User enters a domain name in the browser.
Query goes to a recursive DNS resolver.
Resolver contacts the root name server for the TLD (e.g., .com).
TLD name server provides the authoritative name server.
Resolver queries the authoritative name server (Route 53).
Route 53 returns the IP address.
User's device connects to the IP address.



## Jump Server
  A Jump Server (Jump Box or Bastion Host) is a secure server used to access other servers in a protected network. It enhances security by serving as an intermediary, controlling and logging access to internal systems. Administrators connect to the Jump Server to manage other resources securely.
 
 
 
#### 1. Tell me about your professional experience and day-to-day activities.
Answer: I have been working as a DevOps Engineer for the past few years, focusing on automation, infrastructure management, and continuous integration/continuous deployment (CI/CD) pipelines. My day-to-day activities include:
Monitoring: Using tools like Prometheus and Grafana to monitor system performance and identify issues.
Automation: Writing Ansible playbooks and using Terraform for infrastructure as code to automate the provisioning and management of resources.
CI/CD: Managing Jenkins pipelines to ensure smooth build, test, and deployment processes.
Collaboration: Working closely with development and operations teams to resolve issues and improve processes.
Scripting: Writing Python and Shell scripts to automate repetitive tasks.
Incident Management: Responding to incidents and performing root cause analysis to prevent recurrence.

#### 2. What is the difference between IAM users and roles?
Answer:
IAM Users: These are AWS identities associated with a person or service. Users have permanent long-term credentials and specific permissions assigned directly to them.
IAM Roles: These are identities that can be assumed by users, applications, or services. Roles have temporary security credentials and are used to delegate permissions without sharing long-term credentials. Roles can be assumed by entities within or across AWS accounts.

#### 3. What is the main difference between root users and IAM users?
Answer:
Root User: The root user has full administrative access to the AWS account. This user is created when the account is first set up and has unrestricted access to all resources and services.
IAM Users: IAM users are created by the root user or other administrators and have specific permissions assigned to them. They do not have full administrative access unless explicitly granted.

#### 4. Do you know what EC2 is? Explain why EC2 is used.
Answer: Amazon Elastic Compute Cloud (EC2) is a web service that provides resizable compute capacity in the cloud. It is used for:
Scalability: Easily scale up or down based on demand.
Flexibility: Choose from a variety of instance types, storage options, and networking configurations.
Cost-Effectiveness: Pay only for the compute capacity you use.
Reliability: Benefit from Amazon's proven infrastructure with high availability and fault tolerance.


#### 5. What is the difference between on-demand instances and spot instances?
Answer:
On-Demand Instances: You pay for compute capacity by the hour or second with no long-term commitments. Ideal for unpredictable workloads or applications that cannot be interrupted.
Spot Instances: You bid for unused EC2 capacity, which can be significantly cheaper than on-demand instances. However, AWS can terminate spot instances when it needs the capacity back, making them suitable for fault-tolerant and flexible applications.


#### 6. Why do we use Auto Scaling in AWS? What are the types of auto-scaling groups? Explain them.
Answer: Auto Scaling ensures that you have the right number of EC2 instances available to handle the load for your application. It improves availability and reduces costs by scaling resources based on demand.
Types of Auto Scaling Groups:
Dynamic Scaling: Adjusts the number of instances based on demand patterns using policies.
Scheduled Scaling: Adds or removes instances at specific times based on a schedule.
Predictive Scaling: Uses machine learning to predict future traffic and adjusts the number of instances accordingly.


#### 7. Imagine you have an EC2 instance with auto-scaling enabled, set to scale out whenever the instance reaches peak load. However, you notice that auto-scaling is not functioning as expected. What could be the potential reasons for this issue, and how would you troubleshoot it?
Answer: Potential reasons and troubleshooting steps include:
Incorrect Scaling Policies: Verify that the scaling policies are correctly defined and triggered based on the correct metrics.
Instance Limits: Check if the account has reached its instance limits.
Health Checks: Ensure health checks are configured correctly, and instances are passing them.
CloudWatch Alarms: Verify that CloudWatch alarms are set up correctly to trigger scaling actions.
Auto Scaling Group Configuration: Review the configuration of the Auto Scaling group to ensure it matches the desired setup.


#### 8. Suppose you are using an EC2 instance that frequently shuts down unexpectedly. How would you automate the process so that the EC2 instance automatically restarts whenever it shuts down?
Answer: To automate the restart of an EC2 instance:
CloudWatch Alarm: Create a CloudWatch alarm that triggers whenever the instance status changes to stopped.
SNS Topic: Configure the CloudWatch alarm to send a notification to an SNS topic.
Lambda Function: Create a Lambda function that subscribes to the SNS topic and runs a script to start the instance.
IAM Role: Ensure the Lambda function has an IAM role with permissions to start EC2 instances.


#### 9. What is Amazon S3, and what are its primary use cases?
Answer: Amazon S3 (Simple Storage Service) is an object storage service that provides scalable, durable, and secure storage for any amount of data. Primary use cases include:
Backup and Restore: Store backup copies of data.
Archive: Archive infrequently accessed data.
Big Data Analytics: Store and analyze large datasets.
Content Distribution: Distribute static content such as images, videos, and software.
Data Lake: Centralize data storage for various analytics and machine learning applications.


#### 10. Can you explain the different types of storage classes available in Amazon S3? How to secure the object in S3 bucket?
Answer:
Storage Classes:
Standard: High durability and availability for frequently accessed data.
Intelligent-Tiering: Automatically moves data between access tiers based on changing access patterns.
Standard-IA (Infrequent Access): Lower cost for data accessed less frequently.
One Zone-IA: Lower cost than Standard-IA but stores data in a single availability zone.
Glacier: Low-cost storage for long-term archival with retrieval times in minutes to hours.
Glacier Deep Archive: Lowest-cost storage for long-term archival with retrieval times in hours.
Securing Objects:
Bucket Policies: Define who can access the bucket and its objects.
IAM Policies: Restrict access to specific users or roles.
Encryption: Enable server-side encryption for objects at rest.
Access Control Lists (ACLs): Control access to individual objects.
Bucket Versioning: Maintain multiple versions of objects for data protection.

 
 
####  4. What is VPC? Components of VPC
A Virtual Private Cloud (VPC) is a virtual network dedicated to your AWS account. Components of a VPC include subnets, route tables, internet gateways, NAT gateways, security groups, and network ACLs (NACLs).

#### 5. Types of subnet in VPC
There are two types of subnets in a VPC: public subnets and private subnets.

#### 6. Explain how to identify which is private and which is public subnet
A public subnet is one that has a route to an internet gateway, allowing instances within it to communicate directly with the internet. A private subnet lacks a direct route to the internet gateway, making its instances isolated from direct internet access.

#### 7. What is NACL? Why did you use NACL? Difference between NACL and security group
A Network Access Control List (NACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. NACLs are used to provide an additional layer of security and are stateless, meaning they do not track the state of connections. Security groups, on the other hand, are stateful and are applied at the instance level.

#### 8. What is KMS in AWS
AWS Key Management Service (KMS) is a managed service that enables you to create and control the encryption keys used to encrypt your data.

#### 9. Tell me 5 options or ways to secure AWS services or applications
Use IAM roles and policies to enforce the principle of least privilege.
Enable multi-factor authentication (MFA) for all users.
Encrypt data at rest and in transit using services like AWS KMS and SSL/TLS.
Regularly audit and rotate access keys and passwords.
Implement VPC security measures such as security groups and NACLs.

#### 10. What is VPC peering
VPC peering allows you to connect two VPCs privately using AWS's network, enabling instances in either VPC to communicate with each other as if they are within the same network.

#### 11. What is main requirement you must meet in order to create VPC peering
The main requirement is that the VPCs must not have overlapping CIDR blocks.

#### 12. Can we connect VPCs from different regions if yes how
Yes, you can connect VPCs from different regions using inter-region VPC peering.

#### 13. Is it necessary to create or declare VPC while creating RDS instance
Yes, you need to specify a VPC when creating an RDS instance, and the RDS instance will be launched within that VPC.

#### 14. What is RDS and what is the most important use case of RDS
Amazon Relational Database Service (RDS) is a managed service that makes it easy to set up, operate, and scale a relational database in the cloud. The most important use case is to provide a scalable, highly available, and cost-effective database solution without the need for managing the underlying infrastructure.

#### 15. Can you increase the capacity of an existing RDS if yes tell me the steps
Yes, you can increase the capacity of an existing RDS instance by modifying the instance size through the AWS Management Console or using the AWS CLI. Steps include:
Select the RDS instance.
Choose "Modify."
Select a new instance type or storage allocation.
Apply the changes.

#### 16. What is EC2? Types of EC2?
Amazon Elastic Compute Cloud (EC2) provides scalable computing capacity in the AWS cloud. Types of EC2 instances include:
General Purpose (e.g., t3, m5)
Compute Optimized (e.g., c5)
Memory Optimized (e.g., r5)
Storage Optimized (e.g., i3)
GPU Instances (e.g., p3)
High Memory Instances

#### 17. Suppose you create an EC2 without a key pair, can you access that EC2 instance?
Without a key pair, you cannot use SSH to access the EC2 instance. You would need to use a different authentication method, such as a systems manager or user data to configure an access method.

#### 21. How to run a script which you need to install while creating EC2
You can use the EC2 user data feature to run a script at the launch of the instance. The script is provided in the user data field during the EC2 instance configuration.

#### 22. Types of load balancer
Application Load Balancer (ALB)
Network Load Balancer (NLB)
Classic Load Balancer (CLB)

#### 23. Explain in details in which condition which load balancer is best suitable
ALB: Best for HTTP/HTTPS traffic, providing advanced routing, SSL termination, and user authentication.
NLB: Best for TCP/UDP traffic, providing high performance and low latency.
CLB: Best for simple load balancing of HTTP/HTTPS and TCP traffic.

#### 24. What is Lambda?
AWS Lambda is a serverless compute service that runs your code in response to events and automatically manages the underlying compute resources.

#### 25. What do you mean by trigger and event?
A trigger is a service or resource that invokes your Lambda function, while an event is the data passed to the function when it's triggered.

#### 26. Which language you used in Lambda
I've used Python for writing AWS Lambda functions.

#### 27. Explain where and why you used Lambda
I used Lambda for automating tasks such as processing S3 bucket events, responding to DynamoDB changes, and running scheduled tasks without managing servers.

#### 28. What is CloudWatch
Amazon CloudWatch is a monitoring and management service that provides data and actionable insights for AWS, hybrid, and on-premises applications and infrastructure resources.

#### 29. EKS and its configuration
Amazon Elastic Kubernetes Service (EKS) is a managed service that makes it easy to run Kubernetes on AWS. Configuration involves setting up an EKS cluster, creating worker nodes, and configuring kubectl to manage the cluster.


#### 15. In VPC, How to Identify Which Subnet is Private and Which Subnet is Public?
Answer:
Public Subnet: A public subnet is associated with a route table that has a route to an internet gateway, allowing resources within the subnet to access the internet.
Private Subnet: A private subnet is associated with a route table that does not have a route to an internet gateway, restricting direct access to the internet. Typically, traffic from private subnets can access the internet via a NAT gateway or NAT instance.

#### How do you execute jobs in AWS?
AWS provides various services to execute jobs, such as AWS Lambda for serverless execution, AWS Batch for batch processing jobs, AWS Step Functions for orchestrating workflows, and AWS ECS/EKS for containerized jobs. You can use the AWS Management Console, CLI, SDKs, or Infrastructure as Code tools like Terraform to configure and trigger these jobs.

#### What is VPC?
A Virtual Private Cloud (VPC) is a logically isolated section of the AWS cloud where you can launch AWS resources in a virtual network that you define. You have full control over your virtual networking environment, including selecting your own IP address range, creating subnets, and configuring route tables and network gateways.

#### How can you define a public and private subnet in VPC?
A public subnet is one that has a route to an Internet Gateway, allowing instances within the subnet to communicate directly with the internet. A private subnet does not have a route to an Internet Gateway but can connect to the internet via a NAT Gateway or NAT instance in a public subnet.

#### How an EC2 instance can fetch something from the internet?
An EC2 instance can fetch something from the internet if it is in a public subnet with an associated Elastic IP or public IP address and a route to an Internet Gateway. If in a private subnet, it can access the internet using a NAT Gateway or NAT instance in a public subnet.
#### How does a request from the app go to the internet?
For a request from an app on an EC2 instance to reach the internet, the instance must have a route to an Internet Gateway (for public subnets) or through a NAT Gateway/NAT instance (for private subnets). Additionally, security groups and NACLs must allow outbound traffic to the desired internet destinations.


#### If you restrict the security group, NACL, and the NAT Gateways, then how can you connect and fetch something from S3?
You can use VPC endpoints for S3, which allow instances in a VPC to securely access S3 without traversing the internet. You must configure the endpoint in your VPC and update route tables and security groups to allow traffic to the endpoint.

#### What is the difference between NACL and Security groups?
Security Groups are stateful and operate at the instance level, automatically allowing return traffic. NACLs (Network ACLs) are stateless and operate at the subnet level, requiring explicit rules for both inbound and outbound traffic. Security Groups are generally easier to manage for instance-level security, while NACLs offer an additional layer of control at the subnet level.

#### AMI and snapshot difference?
An AMI (Amazon Machine Image) is a template for creating an EC2 instance and includes an operating system, application server, and applications. A snapshot is a point-in-time backup of an EBS (Elastic Block Store) volume, which can be used to create new volumes or restore data to an existing volume.


#### What will you do to make your application more secure?
To make an application more secure, you can implement several measures:
Use IAM roles and policies to enforce the principle of least privilege.
Enable encryption for data at rest and in transit.
Implement multi-factor authentication (MFA).
Regularly update and patch your systems and software.
Monitor and audit access and activity using services like AWS CloudTrail and AWS Config.
Use security groups and NACLs to control traffic to and from your instances.
Implement secure coding practices and conduct regular security reviews and testing.


#### What is the difference between ALB and NLB?
ALB (Application Load Balancer) operates at the application layer (Layer 7) and supports advanced routing features, such as host-based and path-based routing, and provides SSL termination. NLB (Network Load Balancer) operates at the transport layer (Layer 4) and is designed for high performance, low latency, and handling millions of requests per second. NLB can also handle TCP and UDP traffic, while ALB is focused on HTTP/HTTPS traffic.
How to give bucket access to one user without console access?
You can give bucket access to a user by creating an IAM policy that grants the necessary permissions (e.g., s3
, s3
) and attaching it to the IAM user. This allows the user to interact with the S3 bucket programmatically via the AWS CLI, SDKs, or API without needing console access.

#### Is there any possible way to recover the object after deleted?
If S3 versioning is enabled on the bucket, you can recover a deleted object by retrieving a previous version of the object. If versioning is not enabled, the object cannot be recovered after deletion.

#### How to restrict or give permission to a specific object?
To restrict or give permission to a specific object, you can use bucket policies, IAM policies, or object ACLs (Access Control Lists). These policies can specify actions (e.g., s3
) and conditions to allow or deny access to specific objects.


#### What are inline-based policies?
Inline policies are policies that are directly attached to a single IAM user, group, or role. They are useful for specific permissions that are not intended to be reused. Unlike managed policies, inline policies are not shared and are directly associated with the entity to which they are attached.

#### How to access the S3 bucket privately?
To access an S3 bucket privately, you can:
Use VPC endpoints to route traffic to S3 without using the public internet.
Configure bucket policies and IAM policies to restrict access to specific VPCs or IP ranges.
Use S3 access points to create specific access policies.


#### What is the difference between a NAT instance and a NAT Gateway?
NAT Instance:
An EC2 instance configured to act as a NAT.
Requires manual management (scaling, high availability, updates).
Limited to instance types and sizes.
NAT Gateway:
Managed service provided by AWS.
Automatically scales and is highly available within an Availability Zone.
Easier to set up and maintain.

#### How can you restrict particular IPs accessing EC2 instances?
You can restrict IPs accessing EC2 instances by configuring security group rules and network ACLs to allow or deny traffic from specific IP addresses or ranges.


#### What is called VPC peering?
VPC peering is a networking connection between two VPCs that allows them to route traffic to each other privately. VPCs can be in the same or different AWS accounts and regions.

#### What is called Transit Gateway?
AWS Transit Gateway is a service that connects VPCs and on-premises networks through a central hub. It simplifies network management by allowing you to route traffic between multiple VPCs and VPN connections using a single gateway.


#### What are the types of autoscaling?
Types of autoscaling in AWS include:
Dynamic Scaling: Adjusts capacity based on demand using predefined policies.
Scheduled Scaling: Adjusts capacity based on a schedule.
Predictive Scaling: Uses machine learning to predict future traffic and adjust capacity accordingly.


#### To prevent DDOS attacks, which load balancer is used?
To help prevent DDoS attacks, AWS recommends using the AWS Shield service in conjunction with Elastic Load Balancing (ELB), including both Application Load Balancer (ALB) and Network Load Balancer (NLB).


#### What is called a sticky session?
A sticky session (session affinity) is a feature that binds a user's session to a specific instance in a load-balanced environment, ensuring that all requests from the user are directed to the same instance.


#### What is called Lambda?
AWS Lambda is a serverless compute service that lets you run code in response to events without provisioning or managing servers. It automatically scales and charges only for the compute time consumed.

#### What is called a Trust relationship in AWS?
A trust relationship in AWS is a policy that grants permission to one AWS account to access resources in another AWS account. It is commonly used in IAM roles to allow cross-account access.


#### What is called Public Subnet and Private Subnet?
A public subnet has a route to an Internet Gateway, allowing instances to communicate directly with the internet. A private subnet does not have a route to an Internet Gateway and is typically used for instances that should not be directly accessible from the internet.


#### How do you establish a connection between EC2 instance to another EC2 instance?
To establish a connection between EC2 instances:
Ensure both instances are in the same VPC or have VPC peering.
Configure security groups to allow inbound traffic on the necessary ports (e.g., SSH, HTTP).
Use the private IP address of the target instance to connect.


#### 4. What are the types of storage accounts in AWS S3?
Answer: AWS S3 offers several storage classes:
Standard: High durability and availability for frequently accessed data.
Intelligent-Tiering: Automatically moves data between two access tiers when access patterns change.
Standard-IA (Infrequent Access): Lower cost for data that is accessed less frequently but requires rapid access when needed.
One Zone-IA: Lower cost than Standard-IA but stores data in a single AZ.
Glacier: Low-cost storage for long-term archival with retrieval times in minutes to hours.
Glacier Deep Archive: Lowest-cost storage for long-term archival with retrieval times in hours.


#### 5. Are you familiar with lifecycle management in S3 buckets? How do you set up lifecycle policies?
Answer: Yes, I am familiar with lifecycle management in S3 buckets. Lifecycle policies help manage object storage by automatically transitioning objects to different storage classes or expiring them after a specified period. To set up lifecycle policies:
Go to the S3 bucket in the AWS Management Console.
Select the "Management" tab and then "Lifecycle".
Create a new lifecycle rule, specify the prefix or tags to identify the objects, and define the actions (transition or expiration).
Save the rule.

#### 6. What are the differences between load balancers, and why do we need them?
Answer: Load balancers distribute incoming traffic across multiple servers to ensure high availability and reliability. In AWS, the main types of load balancers are:
Application Load Balancer (ALB): Operates at the application layer (Layer 7), ideal for HTTP/HTTPS traffic, supports advanced routing features.
Network Load Balancer (NLB): Operates at the transport layer (Layer 4), handles high traffic with low latency, suitable for TCP/UDP traffic.
Classic Load Balancer (CLB): Operates at both the application and network layers but is legacy and less feature-rich compared to ALB and NLB.


#### 7. Have you worked with Auto Scaling Groups (ASG)?
Answer: Yes, I have worked with Auto Scaling Groups (ASG). ASGs automatically adjust the number of EC2 instances based on demand to maintain performance and optimize costs. They ensure the right number of instances are running to handle the load, and they can automatically scale in or out based on defined policies.


#### 11. Which AWS services do you consider when setting up a CI/CD pipeline for a microservices application?
Answer: When setting up a CI/CD pipeline for a microservices application, consider the following AWS services:
AWS CodeCommit: Source code repository.
AWS CodeBuild: Build service for compiling code and running tests.
AWS CodeDeploy: Deployment service to automate application deployments.
AWS CodePipeline: Orchestration service to define the CI/CD workflow.
Amazon ECR: Docker container registry to store and manage Docker images.
Amazon ECS or EKS: Container orchestration services to run and manage microservices.


#### 12. On a day with unusually high traffic for an e-commerce application, how would you, as a cloud engineer, manage the current setup to handle the load smoothly?
Answer: To manage high traffic:
Auto Scaling: Ensure Auto Scaling Groups are configured to automatically scale instances based on demand.
Load Balancers: Verify that load balancers are correctly distributing traffic and can handle increased load.
Caching: Use caching mechanisms like Amazon CloudFront or ElastiCache to reduce the load on the backend.
Database Scaling: Scale the database vertically or horizontally, and use read replicas to offload read traffic.
Monitoring: Continuously monitor the system with CloudWatch to identify and address bottlenecks.


#### 13. If traffic is currently handled on a single instance, how would you upgrade for high availability in AWS?
Answer: To upgrade for high availability:
Load Balancer: Add an Application Load Balancer (ALB) to distribute traffic across multiple instances.
Auto Scaling: Configure an Auto Scaling Group (ASG) to automatically adjust the number of instances based on demand.
Multiple Availability Zones: Deploy instances across multiple Availability Zones to ensure redundancy and fault tolerance.
RDS Multi-AZ: Use Amazon RDS Multi-AZ deployment for database high availability and failover support.


#### 14. When auto-scaling instances, how do you manage the backend RDS database?
Answer: To manage the backend RDS database during auto-scaling:
Read Replicas: Use RDS read replicas to offload read traffic from the primary database.
Scaling: Monitor database performance and scale up the RDS instance or adjust instance classes as needed.
Connection Management: Implement connection pooling to efficiently manage database connections from scaled instances.
Multi-AZ Deployment: Ensure the RDS database is configured for Multi-AZ deployment to enhance availability and failover capabilities.


#### 15. Have you ever set up cross-account access for S3? For example, if the QA team needs access to the production database.
Answer: Yes, I have set up cross-account access for S3. This involves:
IAM Roles: Create an IAM role in the target account with the necessary permissions.
Trust Relationship: Update the trust relationship in the role to allow the source account to assume the role.
Bucket Policy: Update the S3 bucket policy to grant access to the IAM role from the source account.


#### 16. How can an S3 account in Account A access an S3 account in Account B?
Answer: To allow an S3 account in Account A to access an S3 bucket in Account B:
Create IAM Role: Create an IAM role in Account B with permissions to access the S3 bucket.
Set Trust Relationship: Configure the trust relationship to allow IAM users or roles from Account A to assume the role.
Bucket Policy: Update the S3 bucket policy in Account B to grant access to the IAM role.


#### 17. Can you differentiate between IAM policies and IAM roles?
Answer:
IAM Policies: Documents that define permissions and can be attached to users, groups, or roles. They specify what actions are allowed or denied on which resources.
IAM Roles: Identities that can be assumed by trusted entities (users, applications, services) to gain temporary access to AWS resources. Roles have associated policies that define their permissions.


#### 18. Can you explain the STS assumption role policy?
Answer: The STS (Security Token Service) AssumeRole API allows an entity to assume a role and obtain temporary security credentials. This is commonly used to grant cross-account access. The entity must be granted permission to assume the role through the role's trust policy, which specifies which entities are allowed to assume the role.


#### 19. Have you experienced any challenging issues or incidents in your project? How did you and your team identify and resolve them?
Answer: Yes, one challenging issue was a significant performance degradation in a production environment. We identified the problem through:
Monitoring Tools: Using CloudWatch and Prometheus to detect abnormal metrics and logs.
Root Cause Analysis: Conducting a thorough investigation to isolate the issue, which was related to database connection limits.
Resolution: Implementing connection pooling and increasing database instance size to handle the load.
Post-Incident Review: Conducted a post-incident review to document the incident and improve processes to prevent future occurrences.


#### 6. VPC and What Is the Main Function of VPC
Answer: A Virtual Private Cloud (VPC) is a logically isolated section of the AWS cloud where you can launch AWS resources in a virtual network that you define. The main function of a VPC is to provide network security, segmentation, and isolation within the AWS cloud.

#### 7. How to Connect RDS with EC2 Instance: Give Specific Steps
Answer:
Ensure RDS is in the Same VPC: Make sure your RDS instance is in the same VPC as your EC2 instance.
Security Group Configuration: Modify the security group associated with the RDS instance to allow inbound traffic from the EC2 instance’s IP address or security group.
Connect Using Client: Use a database client like MySQL Workbench or connect directly from the EC2 instance using a command like mysql -h <RDS-endpoint> -u <username> -p.

#### 8. My S3 Bucket is Private and There Are Multiple Files in That Bucket. Now I Want to Make a Specific File Public. How Can I Do That?
Answer:
Navigate to the S3 console and open the bucket.
Find the specific file you want to make public.
Select the file, click on the "Permissions" tab, and then "Edit" under "Public access."
Check the box for "Grant public read access to this object(s)" and save the changes.

#### 18. What is the use case of AWS Config service?
Answer: AWS Config is used for:
Configuration Tracking: Monitoring and recording configuration changes of AWS resources.
Compliance Auditing: Assessing and auditing the compliance of resources with configuration policies.
Change Management: Reviewing historical changes and relationships between resources.
Governance: Ensuring that resources adhere to organizational policies and regulations.


#### 19. How to track AWS cloud service changes?
Answer: To track AWS cloud service changes, use:
AWS CloudTrail: Provides a log of API calls and changes to AWS services.
AWS Config: Monitors and records configuration changes and compliance.
AWS CloudWatch: Tracks metrics and logs related to service performance and changes.


#### 20. What is the use of DynamoDB?
Answer: Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. It is used for:
High-Performance Applications: Supporting applications that require low-latency data access.
Flexible Schema: Handling dynamic and unstructured data.
Scalable Workloads: Managing workloads with high read and write throughput.


#### 21. If you want to give someone temporary access for like 1 hour, how to do it, and how to configure that?
Answer: To provide temporary access in AWS:
Use AWS IAM Roles: Create a role with the required permissions and configure it with a trust relationship.
Configure Session Duration: Set a temporary security token for the role with a specific session duration (e.g., 1 hour) using AWS Security Token Service (STS).
Provide Access: Share the temporary credentials with the user.


#### How do you differentiate within an AWS account dev env, test env, and prod env?

Differentiate environments within an AWS account by using:
Separate VPCs for each environment.
Tagging resources with environment-specific tags.
Using different IAM roles and policies for each environment.
Employing naming conventions to distinguish resources.


#### Types of EC2 instances?
EC2 instance types are categorized based on use cases:
General Purpose (e.g., t3, m5)
Compute Optimized (e.g., c5)
Memory Optimized (e.g., r5, x1e)
Storage Optimized (e.g., i3, d2)
Accelerated Computing (e.g., p3, g4)


#### How can you encrypt the already created unencrypted EBS without creating a fresh EC2 instance?
To encrypt an already created unencrypted EBS volume:
Create a snapshot of the unencrypted volume.
Copy the snapshot and enable encryption during the copy process.
Create a new encrypted volume from the encrypted snapshot.
Detach the old volume and attach the new encrypted volume to the instance.

#### How can you deploy two websites on an EC2 instance?
To deploy two websites on an EC2 instance:
Use Different Ports: Configure each website to run on different ports and set up appropriate security group rules.
Use Virtual Hosts: If using a web server like Apache or Nginx, configure virtual hosts to serve different websites based on domain names or paths.
Example with Nginx: Configure Nginx with multiple server blocks to handle requests for each domain or path.


#### 10. What is the best way to design a 3-tier architecture, which services are included, and how to select services to design it?
Answer: A 3-tier architecture typically includes:
Presentation Layer: The user interface layer, which can be implemented using web servers or application frameworks.
Application Layer: The business logic layer, often built using application servers or microservices.
Data Layer: The database layer, using relational or NoSQL databases.
When selecting services:
Consider Scalability: Choose services that can scale based on application needs.
Ensure Security: Implement security features such as encryption and access controls.
Optimize Performance: Use services that provide high performance and low latency.
Evaluate Cost: Select services that fit within budget constraints.


#### 11. What are the strategies for infrastructure optimization, and what actions will you take to reduce infrastructure costs?
Answer: Strategies for infrastructure optimization include:
Right-Sizing: Adjust resource sizes to match actual usage.
Auto-Scaling: Use auto-scaling to handle varying workloads efficiently.
Cost Monitoring: Regularly review and analyze infrastructure costs.
Reserved Instances: Purchase reserved instances for predictable workloads to reduce costs.
Serverless: Use serverless architectures for infrequent or variable workloads.


#### 12. How does auto-scaling work? Does it involve changing the AMI in the auto-scaling group?
Answer: Auto-scaling automatically adjusts the number of instances based on predefined conditions such as CPU usage or traffic volume. It does not directly involve changing the AMI (Amazon Machine Image) in the auto-scaling group; however, you can update the launch configuration or launch template with a new AMI to deploy new instances with updated configurations.


#### 13. If someone created or deleted resources in AWS, how can you find out which user did what action? Which AWS service can help to find out these details?
Answer: AWS CloudTrail is the service that helps track user actions and changes in AWS. It records API calls made by or on behalf of your AWS account, including who made the call and what actions were taken. You can review CloudTrail logs to identify the user and actions associated with resource changes.


#### 14. What is the difference between Latency-Based Routing and Geo DNS?
Answer:
Latency-Based Routing: Directs user requests to the AWS region that provides the lowest latency for the end-user based on real-time network performance.
Geo DNS: Routes user requests based on geographic location, directing them to the nearest region or data center according to predefined geographic rules.


#### 15. What is the difference between a Domain and a Hosted Zone?
Answer:
Domain: A domain is a human-readable address that identifies a specific location on the internet (e.g., example.com).
Hosted Zone: A hosted zone is a container in Route 53 that holds information about how you want to route traffic for a domain (e.g., DNS records for example.com).


#### 16. When we create a VPC, what components will be created by default?
Answer: When creating a VPC, the following components are created by default:
Main Route Table: The default route table associated with the VPC.
Default Security Group: A default security group for the VPC.
Default Network ACL: A default network access control list (ACL) for the VPC.
Internet Gateway: (If explicitly attached) A gateway for internet access.
DHCP Options Set: A default DHCP options set with DNS settings.


#### 17. How to recover a CloudFormation stack if it's stuck in "CREATE_IN_PROGRESS" or "FAILED" status?
Answer: To recover a CloudFormation stack:
Check Events: Review the stack events to identify the cause of the failure.
Fix Issues: Address any issues with the stack resources or template.
Retry: If the stack is in "CREATE_IN_PROGRESS," you may need to wait or manually cancel and retry the stack creation.
Delete and Recreate: If the stack is in a failed state and cannot recover, consider deleting the stack and recreating it.




#### 11. How would you access data in an S3 bucket from Account A when your application is running on an EC2 instance in Account B?
Answer: To access an S3 bucket in Account A from an EC2 instance in Account B, I would set up a cross-account IAM role. Account B's EC2 instance would assume the role, which has the necessary permissions to access the S3 bucket in Account A.
Scenario: In one case, I created an IAM role in Account A with S3 bucket access and allowed Account B's EC2 instance to assume this role using AWS STS (Security Token Service). This setup provided secure access to the S3 bucket without sharing credentials.

#### 12. How do you provide access to an S3 bucket, and what permissions need to be set on the bucket side?
Answer: To provide access to an S3 bucket, you can configure an IAM policy or bucket policy. The necessary permissions typically include s3:GetObject, s3:PutObject, and s3:ListBucket.
Scenario: In a recent project, I set up an IAM policy that granted specific EC2 instances read and write access to an S3 bucket. Additionally, I implemented a bucket policy that restricted access to only those IAM roles and users who required it.

#### 13. How can Instance 2, with a static IP, communicate with Instance 1, which is in a private subnet and mapped to a multi-AZ load balancer?
Answer: Instance 2 can communicate with Instance 1 via the load balancer's DNS name or static IP if the load balancer is internet-facing. If the load balancer is internal, ensure Instance 2 is in the same VPC or connected via VPC peering.
Scenario: In a project, I configured an internal ALB in a multi-AZ setup, which routed traffic between instances in private subnets. Instance 2, residing in the same VPC, used the ALB's DNS name to communicate with Instance 1.

#### 14. How do you pass arguments to a VPC while using the terraform import command?
Answer: When using terraform import to import an existing VPC, you typically pass the VPC ID as an argument. For example:
bash
Copy code
terraform import aws_vpc.example_vpc vpc-12345678

Scenario: I once imported a manually created VPC into Terraform for management by passing the VPC ID. This allowed me to manage the VPC and its resources using Terraform going forward.



#### 17. For an EC2 instance in a private subnet, how can it verify and download required packages from the internet without using a NAT gateway or bastion host? Are there any other AWS services that can facilitate this?
Answer: An EC2 instance in a private subnet can use AWS PrivateLink to connect to AWS services or an S3 VPC endpoint for accessing S3. These services allow secure, private connections to AWS resources without requiring a NAT gateway.
Scenario: In one project, I used an S3 VPC endpoint to allow EC2 instances in private subnets to download software packages stored in S3, avoiding the need for a NAT gateway.

#### 18. What is the typical latency for a load balancer, and if you encounter high latency, what monitoring steps would you take?
Answer: The typical latency for a load balancer can vary but usually ranges from milliseconds to a few hundred milliseconds depending on the load. If I encounter high latency, I would use CloudWatch metrics to monitor the load balancer's performance, checking for metrics like TargetResponseTime, HealthyHostCount, and UnHealthyHostCount.
Scenario: In a previous role, I noticed an increase in latency and used CloudWatch to identify that one of the backend instances was underperforming. I mitigated the issue by replacing the instance and rebalancing the load.

#### 19. If your application is hosted in S3 and users are in different geographic locations, how can you reduce latency?
Answer: To reduce latency, I would use Amazon CloudFront, a Content Delivery Network (CDN), to cache the content at edge locations closer to the users. This reduces the latency by serving content from the nearest location.
Scenario: In a global project, I used CloudFront to distribute static content hosted in an S3 bucket, significantly reducing latency for users across different geographic regions.

#### 20. Which services can be integrated with a CDN (Content Delivery Network)?
Answer: Services that can be integrated with a CDN include:
Web applications hosted on EC2 or S3
API Gateway
Media files stored in S3
Streaming services
WebSocket services
Scenario: I integrated CloudFront with an S3 bucket hosting static assets for a web application. This integration improved the delivery speed and reduced latency for end-users globally.



7. How would you access data in an S3 bucket from Account A when your application is running on an EC2 instance in Account B?
Answer: To access an S3 bucket in Account A from an EC2 instance in Account B, you can use cross-account IAM roles. The steps include:
Create a Role in Account A: Create an IAM role in Account A with permissions to access the S3 bucket.
Allow Account B to Assume the Role: In the trust relationship of the role, specify Account B as a trusted entity.
Assume the Role in Account B: Use the AWS STS assume-role command in Account B to assume the role from Account A and obtain temporary credentials.
Access the S3 Bucket: Use the temporary credentials to access the S3 bucket.
Scenario: I have set up cross-account access in a project where multiple AWS accounts were used for different environments. By assuming roles across accounts, we securely accessed resources like S3 buckets without exposing sensitive credentials.


1. How do you execute jobs in AWS?
Answer: Jobs in AWS can be executed using various services depending on the nature of the job. For example, AWS Lambda can be used for serverless execution of functions, AWS Batch for batch processing jobs, and Amazon ECS or EKS for containerized workloads.
Scenario: In a recent project, I used AWS Lambda to execute periodic data processing tasks triggered by CloudWatch Events. For more complex, containerized workflows, I used Amazon ECS with Fargate to run jobs without managing the underlying infrastructure.


8. How do you provide access to an S3 bucket, and what permissions need to be set on the bucket side?
Answer: To provide access to an S3 bucket, you can use IAM policies or bucket policies. The steps are:
IAM Policy: Attach an IAM policy to a user, group, or role that grants the necessary permissions (e.g., s3:GetObject, s3:PutObject).
Bucket Policy: Set a bucket policy that grants access to specific IAM users, roles, or AWS accounts. The policy should define who can access the bucket and what actions they can perform.
Scenario: In a project, I provided read-only access to an S3 bucket by attaching an IAM policy to a role used by EC2 instances, ensuring that only authorized instances could access the bucket.

9. How can Instance 2, with a static IP, communicate with Instance 1, which is in a private subnet and mapped to a multi-AZ load balancer?
Answer: Instance 2 can communicate with Instance 1 through the load balancer. The static IP of Instance 2 would send requests to the load balancer's DNS name or IP address, which then forwards the requests to Instance 1 based on the load balancer's routing rules.
Scenario: In a multi-tier architecture project, I configured an application server in a private subnet behind an Application Load Balancer (ALB). The web server, with a static IP, communicated with the application server via the ALB, ensuring secure and load-balanced communication.

10. For an EC2 instance in a private subnet, how can it verify and download required packages from the internet without using a NAT gateway or bastion host? Are there any other AWS services that can facilitate this?
Answer: An EC2 instance in a private subnet can use an S3 VPC endpoint or AWS PrivateLink to access AWS services privately without a NAT gateway. For accessing public internet resources, another approach is to use an outbound proxy in the public subnet.
Scenario: In a project, I configured an S3 VPC endpoint to allow EC2 instances in private subnets to securely download packages from S3, avoiding the need for a NAT gateway.

11. What is the typical latency for a load balancer, and if you encounter high latency, what monitoring steps would you take?
Answer: The typical latency for a load balancer ranges from milliseconds to a few hundred milliseconds depending on the load and the number of requests. If high latency is encountered:
Monitor CloudWatch Metrics: Check metrics like TargetResponseTime, HealthyHostCount, and UnHealthyHostCount.
Analyze Logs: Review access logs and application logs to identify potential bottlenecks.
Check Backend Performance: Ensure backend instances are not overloaded or experiencing issues.
Scenario: In a previous role, I used CloudWatch to monitor and troubleshoot high latency issues by identifying and addressing performance bottlenecks in the backend instances.

12. If your application is hosted in S3 and users are in different geographic locations, how can you reduce latency?
Answer: To reduce latency, I would use Amazon CloudFront, a Content Delivery Network (CDN), to cache the content at edge locations closer to the users.
Scenario: In a global application deployment, I used CloudFront with S3 as the origin to significantly reduce latency for users by serving cached content from edge locations.

13. Which services can be integrated with a CDN (Content Delivery Network)?
Answer: Services that can be integrated with a CDN include:
S3 Buckets: To serve static content like images, videos, and files.
EC2 Instances: To deliver dynamic content from applications hosted on EC2.
API Gateway: To accelerate API responses.
Load Balancers: To distribute traffic across multiple backend servers.
Scenario: I integrated CloudFront with an S3 bucket to serve static website content, reducing load times for users by caching content at edge locations globally.




