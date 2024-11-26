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
 
 
 
 
 
 
 


