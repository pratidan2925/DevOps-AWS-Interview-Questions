1.  What is Jenkins ? 
What: An open-source automation server.
Purpose: Facilitates continuous integration (CI) and continuous delivery (CD) of software.
How: Automates tasks like building, testing, and deploying code changes. Uses pipelines (scripted in a Jenkinsfile) to define these steps.
2.  CI/CD (Continuous Integration/Continuous Delivery or Deployment):
Continuous Integration (CI):
What: A development practice where developers frequently integrate their code changes into a shared repository.
Purpose: Detect and fix integration issues early.
How: Automated builds and tests run every time code is committed, ensuring the codebase is always in a workable state.
Continuous Delivery (CD):
What: An extension of CI where code changes are automatically prepared for a release to production.
Purpose: Ensure that the codebase can be deployed to production anytime.
How: Automates the release process up to the point of deployment, including additional testing and staging steps.
Continuous Deployment (CD):
What: Similar to continuous delivery, every change that passes the automated tests is automatically deployed to production.
Purpose: Minimize manual intervention in the deployment process, delivering new features and updates quickly.
How: Automates the entire process from code commit to production deployment, ensuring rapid and reliable releases.
Overall Purpose: CI/CD aims to improve software quality and speed up the development and deployment process, making it easier to deliver new features and fixes to users frequently and reliably.

3.  What is Jenkins Workspace location
/var/lib/jenkins
4.  How can you take backup of Jenkins
 Thin backup - install plugin thin backup
Server backup - take the backup of the whole server(V.M) .And it is the best way as everything is backuped.
 WorkSpace backup - backup of the jenkins folder is done (/var/lib/jenkins/)

5. Can we change the home directory of jenkins
             Yes , You can change the directory by creating a pipeline .
                     pipeline {
Agent{
node {customWorkspace '/data/mypipeline'}
	}
	stages {
			stage (create file){
				steps{
					sh 'touch NewFile'
				}
			}
		}
           }
6.  Difference between Scripted and Declarative Pipeline
Scripted and Declarative Pipelines are two ways to define Jenkins Pipeline as code. Both are used to create continuous delivery pipelines in Jenkins, but they differ in their syntax and approach.

1. Scripted Pipeline:
   - Scripted Pipeline is based on Groovy scripting language.
   - It uses an imperative programming style, where you write a script using Groovy syntax to define your pipeline stages and steps.
   - Provides a lot of flexibility and allows you to define complex logic easily.
   - Typically, you would use a scripted pipeline when you have complex requirements that cannot be easily expressed with declarative syntax or when you need to do advanced scripting or integration with existing libraries.

Example of Scripted Pipeline:
node {
            stage('Build') {
                      sh 'maven clean package'
                     }
             stage('Test') {
                      sh 'mvn test'
                     }
            stage('Deploy') {
                     sh 'kubectl apply -f deployment.yaml'
                     }
        }

2. Declarative Pipeline:
   - Declarative Pipeline is a more structured and opinionated way to define pipelines.
   - It uses a declarative syntax with a predefined set of keywords to define the pipeline stages and steps.
   - Designed to be more human-readable and easier to understand, especially for those who are not familiar with Groovy or scripting languages.
   - Provides limited flexibility compared to Scripted Pipeline but promotes best practices and helps maintain consistency across pipelines.

Example of Declarative Pipeline:

pipeline {
    agent any
           stages {
                 stage('Build') {
                        steps {
                              sh 'maven clean package'
                               }
                           }
                   stage('Test') {
                         steps {
                                sh 'mvn test'
                                  }
                              }
                    stage('Deploy') {
                            steps {
                                  sh 'kubectl apply -f deployment.yaml'
                                     }
                               }
                        }
                }
7. If your Jenkins master server goes down, here's what happens to your jobs:
Jobs on the Master: These jobs will stop and need to be restarted once the master is back up.
Jobs on Agent Nodes: If the agents can't communicate with the master, these jobs might fail or pause until the master is restored.
Scheduled Jobs: New jobs won't start while the master is down; they'll be queued and will start once the master is back up.
To minimize impact, consider setting up high availability and regular backups.

Explain Master and slave Architecture .

Jenkins master
This is the primary server of Jenkins.
It handles a number of tasks that include but are not limited to scheduling build jobs, recording and presenting build results, dispatching builds to slaves for execution, monitoring all the slaves offline as well as online, and others.
Master Jenkins is capable of directly executing build jobs.
Jenkins slave
It runs on the remote server.
The Jenkins server follows the requests of the Jenkins master and is compatible with all operating systems.
Building jobs dispatched by the master are executed by the slave.
The project can be suitably configured to choose a specific slave machine. 
Jenkins -Master Connectivity
Using the SSH method: Uses the ssh protocol to connect to the agent. The connection gets initiated from the Jenkins master. There should be connectivity over port 22 between master and agent.
Using the JNLP method: Uses java JNLP protocol (Java Network Launch Protocol).

If one job fails in jenkins but you want to continue with the other job ,is it possible
Yes, it's possible to configure Jenkins to continue with other jobs even if one job fails. Here’s how you can achieve this:
Using Jenkins Pipeline:
Define stages in your Jenkinsfile.
Use try-catch blocks or post conditions to handle failures.
Trigger subsequent jobs using build step with wait: false to continue immediately.
Using Freestyle Projects:
Configure post-build actions to trigger other jobs or execute tasks.
Ensure these actions are set to execute regardless of the build result.

How can you Managing different environments in Jenkins 
Pipeline Jobs:
Use pipelines to define environment-specific steps for build, test, and deployment.
Set environment variables and parameters to handle different environments.
Nodes and Labels:
Assign specific nodes (servers) for different environments, labeled accordingly (e.g., dev, staging, prod).
Direct jobs to the appropriate node based on these labels.
Separate Jobs:
Create distinct Jenkins jobs for each environment, named to reflect their purpose (e.g., project-dev, project-staging, project-prod).
Config Files and Secrets Management:
Use plugins to manage configuration files and securely store environment-specific credentials.
Inject these configurations and credentials into jobs as needed.
Branch Strategies:
Use specific branch naming conventions in your version control system to represent different environments (e.g., dev, staging, main).
These strategies ensure that each environment (development, staging, production) has its own configuration, resources, and deployment processes, allowing for organized and efficient CI/CD pipelines.

Which are options to create the Jenkins 
Freestyle Project: General-purpose, flexible job with configurable build steps and actions.
Pipeline: Scripted continuous delivery pipeline using Groovy and defined in a Jenkinsfile.
Multibranch Pipeline: Automatically creates pipelines for each branch and pulls requests in a repository.
GitHub Organization: Scans a GitHub organization and creates jobs for each repository.
Folder: Organizes jobs into folders for better management of large projects.
Multiconfiguration (Matrix) Project: Runs jobs with different configurations, useful for testing across environments.
External Job: Monitors and tracks the execution of jobs run outside Jenkins.


If i want to check the health  of EC2 instance which notification plugin you have to download.
  To check the health of an EC2 instance and receive notifications in Jenkins, you can use the "Amazon EC2 Fleet Plugin" along     with "CloudBees Disk Usage Simple Plugin". However, for notifications specifically, you should use the "Amazon SNS Notification Plugin". This combination allows you to monitor the health of your EC2 instances and send notifications when specific events occur.
Amazon EC2 Fleet Plugin: Manages EC2 instances as Jenkins agents.
Amazon SNS Notification Plugin: Sends notifications to an SNS topic, which can then trigger alerts via email, SMS, or other endpoints.
Which types of parameters the used for CI-CD pipeline 
In CI/CD pipelines, various types of parameters can be used to customize and control the build, test, and deployment processes. These parameters allow for dynamic and flexible pipelines that can adapt to different scenarios and requirements. Here are some common types of parameters used in CI/CD pipelines:
String Parameter:
A simple text input that can be used to pass arbitrary strings.
Example: Branch name, version number.
Boolean Parameter:
A checkbox that represents true or false values.
Example: Toggle a feature on or off during the build.
Choice Parameter:
A dropdown list allowing the user to select one option from a predefined list.
Example: Environment selection (development, staging, production).
File Parameter:
Allows the user to upload a file that can be used during the build.
Example: Configuration files or test data.
Password Parameter:
A masked input field for sensitive information.
Example: API keys, passwords.
Run Parameter:
Allows selecting a specific run of a job to use as a reference.
Example: Use artifacts from a specific build.

What is shared library in Jenkins
In Jenkins, a shared library is a reusable code repository that you can use across multiple Jenkins pipelines to maintain consistency and reduce redundancy. Key features include:
Reusability: Write common functions, variables, and classes once and use them in multiple pipelines.
Modularity: Organize code into components for better maintenance.
Version Control: Store and manage the library in a version-controlled repository like Git.
Standardization: Enforce best practices and coding standards.
Structure:
src/: Groovy classes and scripts.
vars/: Global Groovy scripts/functions.
resources/: Static resources (e.g., config files).
Example Usage:
Define functions in vars/.
Define classes in src/.
Use the library in Jenkinsfile with the @Library('my-shared-library') _ annotation.
Setup:
Create the library repository with the appropriate structure.
Configure the library in Jenkins under Manage Jenkins > Configure System > Global Pipeline Libraries.
Include the library in your pipelines using the @Library annotation.
Shared libraries help in centralizing and reusing code, making Jenkins pipelines more efficient and easier to manage.



 Stages in a Jenkins Pipeline:
Checkout/Source:
Purpose: To check out the source code from the version control system (e.g., Git).
Typical Steps: Cloning the repository, checking out a specific branch or tag.
Build:
Purpose: To compile or build the application from the source code.
Typical Steps: Running build tools like Maven, Gradle, or npm to compile the code and generate artifacts.
Test:
Purpose: To run automated tests to ensure the code works as expected.
Typical Steps: Executing unit tests, integration tests, or end-to-end tests using testing frameworks like JUnit, TestNG, or Selenium.
Deploy/Package:
Purpose: To package the built application for deployment.
Typical Steps: Creating deployment packages (e.g., JAR, WAR, Docker images), and storing them in an artifact repository.
Deploy to Environment:
Purpose: To deploy the application to different environments such as development, staging, or production.
Typical Steps: Deploying to a server, cloud environment, or Kubernetes cluster using deployment scripts or tools like Ansible, Terraform, or Helm.
Approval/Manual Intervention:
Purpose: To pause the pipeline and wait for manual approval before proceeding to the next stage.
Typical Steps: Sending notifications for approval, waiting for user input.
Post-Deployment Verification:
Purpose: To verify the deployment and ensure the application is running correctly in the target environment.
Typical Steps: Running smoke tests, health checks, or monitoring scripts.
Notification:
Purpose: To send notifications about the pipeline status to relevant stakeholders.
Typical Steps: Sending emails, Slack messages, or updating a dashboard with the build status and results.

How to change the port number of jenkins
1.Locate Jenkins Installation Directory
Linux: /var/lib/jenkins
Windows: C:\Program Files (x86)\Jenkins
Mac: /usr/local/Cellar/jenkins-lts/<version>/libexec
Linux:
Navigate to Jenkins Directory: cd /var/lib/jenkins
Open jenkins.xml:  sudo vim jenkins.xml
Modify Port Number: Find --httpPort=8080 and change to --httpPort=9090.
Save Changes: Press Esc, type :wq, press Enter.
Restart Jenkins: sudo service jenkins restart
Windows:
Navigate to Jenkins Directory:
Open File Explorer, go to C:\Program Files (x86)\Jenkins.
Open jenkins.xml:
Right-click jenkins.xml, select Open with, choose Notepad.
Modify Port Number:
Find --httpPort=8080 and change to --httpPort=9090.
Save Changes:
Save and close Notepad.
Restart Jenkins Service:
Open Run (Windows Key + R), type services.msc, press Enter.
Right-click Jenkins, select Restart.
Mac:
Navigate to Jenkins Directory: cd /usr/local/Cellar/jenkins-lts/<version>/libexec
Open jenkins.xml: sudo vim jenkins.xml
Modify Port Number: Find --httpPort=8080 and change to --httpPort=9090.
Save Changes: Press Esc, type :wq, press Enter.
Restart Jenkins: brew services restart jenkins-lts
Verify Changes
Open a web browser and enter: http://<your-server-ip>:9090
Additional Configurations
Firewall Rules: Ensure the new port is allowed through your firewall.
Reverse Proxy: Update any reverse proxy configurations if Jenkins is behind one.

How to change the Jenkins backend 
1.Change Jenkins Home Directory
Stop Jenkins Service: sudo systemctl stop jenkins
Copy Jenkins Home Directory to New Location: sudo cp -r /var/lib/jenkins /new/path/to/jenkins_home
Update Jenkins Configuration: Open the Jenkins configuration file: sudo nano /etc/default/jenkins
Find the line with JENKINS_HOME= and update it to: JENKINS_HOME="/new/path/to/jenkins_home"
Start Jenkins Service: sudo systemctl start jenkins
2. Change Authentication Backend to LDAP
Configure LDAP in Jenkins:
Open Jenkins in your web browser.
Navigate to Manage Jenkins > Configure Global Security.
Select LDAP under Security Realm.
Enter LDAP server details (URL, user search base, manager DN, etc.).
Save the configuration.
3. Change Storage Backend (e.g., Database)
Install Database Plugin:
Go to Jenkins Dashboard.
Navigate to Manage Jenkins > Manage Plugins.
Install the relevant database plugin (e.g., MySQL, PostgreSQL).
Configure Database Connection:
Go to Manage Jenkins > Configure System.
Find the section for the installed database plugin.
Enter database connection details (driver, URL, username, password).

What is Jenkinsfile  ?
A Jenkinsfile is a text file that contains the definition of a Jenkins pipeline. It is written using a Domain Specific Language (DSL) based on Groovy. The Jenkinsfile defines the steps to be run in the pipeline, which can include building, testing, and deploying the application. There are two types of syntax for Jenkinsfiles: Declarative and Scripted.
What is a cron job in Jenkins ? /What is 5 star Strategy .Explain
A cron job in Jenkins refers to the scheduled execution of Jenkins jobs at specific intervals using a cron-like syntax. This can be set up in the "Build Triggers" section of a Jenkins job configuration.
Cron Syntax:   MINUTE   HOUR   DOM   MONTH   DOW
MINUTE: Minutes (0 - 59)
HOUR: Hours (0 - 23)
DOM: Day of the month (1 - 31)
MONTH: Month (1 - 12)
DOW: Day of the week (0 - 7, with 0 and 7 representing Sunday)



How to store credentials in Jenkins Security 
To store credentials:
Go to Manage Jenkins > Manage Credentials.
Select the appropriate domain.
Click Add Credentials.
Fill in the fields and save.

How to check Jenkins COnfiguration
To check Jenkins configuration:
Go to Manage Jenkins > Configure System.
Review and modify settings as needed.

What is Poll SCM
Poll SCM is a build trigger that checks the source code repository for changes at specified intervals using cron syntax. If changes are found, a build is triggered.
Suppose I have 2 Jobs , I want to trigger One job after the 2 nd job is complete.How will you trigger that job.
o trigger one job after another:
In Job 2 configuration, go to Post-build Actions.
Select Build other projects and enter Job 1. This ensures Job 1 runs after Job 2 completes.






**1. Explain your current CI/CD setup elaborately.**
- CI/CD stands for Continuous Integration and Continuous Delivery. We use GitHub and Jenkins for automation.
- We have set up a webhook in GitHub triggering a CI Pipeline on Jenkins for each commit.

**2. Key components of a Jenkins pipeline**
- Explaining the different stages of the pipeline - build, test, and deployment, as well as the activities within each stage like code analysis, testing, building, and deployment.
- Emphasizing the importance of handling secrets in the CI/CD process, including SSH keys, API keys, and login credentials for Kubernetes.

**3. Securing secrets in CI/CD tools**
- Different options for securing secrets in CI/CD tools like GitHub, GitLab, AWS Systems Manager, Azure Vault, and HashiCorp Vault
- Importance of being prepared for both continuous integration (CI) and continuous delivery (CD) aspects in interviews

**4. Key Deployment Strategies in CD**
- Blue Green Deployment involves switching traffic from old version to new version gradually
- Canary Deployment involves gradually rolling out new version to a small subset of users

**5. Difference between blue-green deployment and canary deployment**
- Blue-green deployment involves switching traffic from old to new versions instantly.
- Canary deployment gradually shifts traffic to the new version to minimize risk.

**6. Blue green deployment for rolling back faulty applications**
- Blue green deployment allows easy rollback by pointing load balancer to the healthy version
- Other deployment strategies require careful explanation and rollback strategies

**7. Jenkins is the most popular CI tool with 90% usage.**
- Jenkins setup is easy, with installation possible through Docker or a simple curl command.
- Important to understand how to take backups for Jenkins logs or artifacts and how to scale up or down based on build volume.

**8. Setting up Jenkins on AWS with Auto Scaling Group**
- Utilizing predictive scaling for traffic prediction and scaling up/down EC2 instances.
- Regularly backing up Jenkins with dot Jenkins folder for data security.

**9: Can you explain the CICD process in your current project ? or Can you talk about any CICD process that you have implemented ?**
A: In the current project we use the following tools orchestrated with Jenkins to achieve CICD.
Maven, Sonar, AppScan, ArgoCD, and Kubernetes
Coming to the implementation, the entire process takes place in 8 steps
1. Code Commit: Developers commit code changes to a Git repository hosted on GitHub.
2. Jenkins Build: Jenkins is triggered to build the code using Maven. Maven builds the code and runs unit tests.
3. Code Analysis: Sonar is used to perform static code analysis to identify any code quality issues, security vulnerabilities, and bugs.
4. Security Scan: AppScan is used to perform a security scan on the application to identify any security vulnerabilities.
5. Deploy to Dev Environment: If the build and scans pass, Jenkins deploys the code to a development environment managed by Kubernetes.
6. Continuous Deployment: ArgoCD is used to manage continuous deployment. ArgoCD watches the Git repository and automatically deploys new changes to the development environment as soon as they are committed.
7. Promote to Production: When the code is ready for production, it is manually promoted using ArgoCD to the production environment.
8. Monitoring: The application is monitored for performance and availability using Kubernetes tools and other monitoring tools.

**10: What are the different ways to trigger jenkins pipelines ?**
A: This can be done in multiple ways, To briefly explain about the different options,
 - Poll SCM: Jenkins can periodically check the repository for changes and automatically build if changes are detected. 
              This can be configured in the "Build Triggers" section of a job.
              
  - Build Triggers: Jenkins can be configured to use the Git plugin, which allows you to specify a Git repository and branch to build. 
              The plugin can be configured to automatically build when changes are pushed to the repository.
              
  - Webhooks: A webhook can be created in GitHub to notify Jenkins when changes are pushed to the repository. 
              Jenkins can then automatically build the updated code. This can be set up in the "Build Triggers" section of a job and in the GitHub repository settings.

**11: How to backup Jenkins ?**
A: Backing up Jenkins is a very easy process, there are multiple default and configured files and folders in Jenkins that you might want to backup.
 - Configuration: The `~/.jenkins` folder. You can use a tool like rsync to backup the entire directory to another location.
  
    - Plugins: Backup the plugins installed in Jenkins by copying the plugins directory located in JENKINS_HOME/plugins to another location.
    
    - Jobs: Backup the Jenkins jobs by copying the jobs directory located in JENKINS_HOME/jobs to another location.
    
    - User Content: If you have added any custom content, such as build artifacts, scripts, or job configurations, to the Jenkins environment, make sure to backup those as well.
    
    - Database Backup: If you are using a database to store information such as build results, you will need to backup the database separately. This typically involves using a database backup tool, such as mysqldump for MySQL, to export the data to another location.

One can schedule the backups to occur regularly, such as daily or weekly, to ensure that you always have a recent copy of your Jenkins environment available. You can use tools such as cron or Windows Task Scheduler to automate the backup process.


**12: How do you store/secure/handle secrets in Jenkins ?**
A: Again, there are multiple ways to achieve this, Let me give you a brief explanation of all the posible options.
  - Credentials Plugin: Jenkins provides a credentials plugin that can be used to store secrets such as passwords, API keys, and certificates. The secrets are encrypted and stored securely within Jenkins, and can be easily retrieved in build scripts or used in other plugins.
   
   - Environment Variables: Secrets can be stored as environment variables in Jenkins and referenced in build scripts. However, this method is less secure because environment variables are visible in the build logs.
   
   - Hashicorp Vault: Jenkins can be integrated with Hashicorp Vault, which is a secure secrets management tool. Vault can be used to store and manage sensitive information, and Jenkins can retrieve the secrets as needed for builds.
   
   - Third-party Secret Management Tools: Jenkins can also be integrated with third-party secret management tools such as AWS Secrets Manager, Google Cloud Key Management Service, and Azure Key Vault.

**13: What is latest version of Jenkins or which version of Jenkins are you using ?**
A: 2.319.1


**14: What is shared modules in Jenkins ?**
A: Shared modules in Jenkins refer to a collection of reusable code and resources that can be shared across multiple Jenkins jobs. This allows for easier maintenance, reduced duplication, and improved consistency across multiple build processes. For example, shared modules can be used in cases like:
       - Libraries: Custom Java libraries, shell scripts, and other resources that can be reused across multiple jobs.
        
        - Jenkinsfile: A shared Jenkinsfile can be used to define the build process for multiple jobs, reducing duplication and making it easier to manage the build process for multiple projects.
        
        - Plugins: Common plugins can be installed once as a shared module and reused across multiple jobs, reducing the overhead of managing plugins on individual jobs.
        
        - Global Variables: Shared global variables can be defined and used across multiple jobs, making it easier to manage common build parameters such as version numbers, artifact repositories, and environment variables.

**15: can you use Jenkins to build applications with multiple programming languages using different agents in different stages ?**
A: Yes, Jenkins can be used to build applications with multiple programming languages by using different build agents in different stages of the build process.
Jenkins supports multiple build agents, which can be used to run build jobs on different platforms and with different configurations. By using different agents in different stages of the build process, you can build applications with multiple programming languages and ensure that the appropriate tools and libraries are available for each language.
For example, you can use one agent for compiling Java code and another agent for building a Node.js application. The agents can be configured to use different operating systems, different versions of programming languages, and different libraries and tools.
Jenkins also provides a wide range of plugins that can be used to support multiple programming languages and build tools, making it easy to integrate different parts of the build process and manage the dependencies required for each stage.
Overall, Jenkins is a flexible and powerful tool that can be used to build applications with multiple programming languages and support different stages of the build process.


**16: How to setup auto-scaling group for Jenkins in AWS ?**
A: Here is a high-level overview of how to set up an autoscaling group for Jenkins in Amazon Web Services (AWS):
   - Launch EC2 instances: Create an Amazon Elastic Compute Cloud (EC2) instance with the desired configuration and install Jenkins on it. This instance will be used as the base image for the autoscaling group.
    
    - Create Launch Configuration: Create a launch configuration in AWS Auto Scaling that specifies the EC2 instance type, the base image (created in step 1), and any additional configuration settings such as storage, security groups, and key pairs.
    
    - Create Autoscaling Group: Create an autoscaling group in AWS Auto Scaling and specify the launch configuration created in step 2. Also, specify the desired number of instances, the minimum number of instances, and the maximum number of instances for the autoscaling group.
    
    - Configure Scaling Policy: Configure a scaling policy for the autoscaling group to determine when new instances should be added or removed from the group. This can be based on the average CPU utilization of the instances or other performance metrics.
    
    - Load Balancer: Create a load balancer in Amazon Elastic Load Balancer (ELB) and configure it to forward traffic to the autoscaling group.
    
    - Connect to Jenkins: Connect to the Jenkins instance using the load balancer endpoint or the public IP address of one of the instances in the autoscaling group.
    
    - Monitoring: Monitor the instances in the autoscaling group using Amazon CloudWatch to ensure that they are healthy and that the autoscaling policy is functioning as expected.

 By using an autoscaling group for Jenkins, you can ensure that you have the appropriate number of instances available to handle the load on your build processes, and that new instances can be added or removed automatically as needed. This helps to ensure the reliability and scalability of your Jenkins environment.

**17: How to add a new worker node in Jenkins ?**
A: Log into the Jenkins master and navigate to Manage Jenkins > Manage Nodes > New Node. Enter a name for the new node and select Permanent Agent. Configure SSH and click on Launch.


**18: How to add a new plugin in Jenkins ?**
A: Using the CLI, java -jar jenkins-cli.jar install-plugin <PLUGIN_NAME>
Using the UI,
Click on the "Manage Jenkins" link in the left-side menu.
Click on the "Manage Plugins" link.


**19: What is JNLP and why is it used in Jenkins ?**
A: In Jenkins, JNLP is used to allow agents (also known as "slave nodes") to be launched and managed remotely by the Jenkins master instance. This allows Jenkins to distribute build tasks to multiple agents, providing scalability and improving performance.
When a Jenkins agent is launched using JNLP, it connects to the Jenkins master and receives build tasks, which it then executes. The results of the build are then sent back to the master and displayed in the Jenkins user interface.


**20: What are some of the common plugins that you use in Jenkins ?**
A: Be prepared for answer, you need to have atleast 3-4 on top of your head, so that interview feels you use jenkins on a day-to-day basis.


