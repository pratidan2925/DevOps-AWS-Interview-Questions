#### main components of Azure DevOps in brief:
Azure Boards: Agile tools for planning, tracking, and discussing work (e.g., Kanban boards, backlogs).
Azure Repos: Source code management with Git repositories and pull requests.
Azure Pipelines: CI/CD platform to build, test, and deploy code automatically.
Azure Test Plans: Tools for manual and exploratory testing.
Azure Artifacts: Package management for Maven, npm, NuGet, and Python.
Azure DevTest Labs: Environments for development and testing.
Extensions and Marketplace: Add-ons to enhance and integrate with other tools and services.

#### What is Azure DevOps
	Azure DevOps server (formally team Foundation server and Visual Studio team system vsts) is a Microsoft product that provides version control reporting requirements management project management automotive builds testing and release management capabilities.

• This covers the entire application life cycle and enables Devops capabilities.
• Azure Devops is offered Azure Devops services.
• This is a hosted solution on Microsoft Azure.
• Azure Devops server
• This is an installation that can be done on the on premises.
• During the plan phase teams use backlogs or kanban boards to define track
• Azure Devops services - This is a hosted solution on Microsoft azure
• Azure Devops server -This is installation that can be done on the premises.

• During the plan phase, teams use backlogs or kanban boards to define, track and layout the work that needs to be done for application in Azure board. We also create a SCM system that can be github or Azure Git Repos.
• During the development phase we create Azure pipelines to create automated builds from the source code. we can use Visual Studio code to create pipelines for building the code.
• During the delivery phase we deploy applications and services to the target environments we use terraform or ARM templates to create infrastructure.
• During the operating phase, we implement monitoring for application and services.


#### Azure Boards
• They are used to plan, track and discuss work across teams using agile planning tools that are available.
• Teams can manage their software with native support for scrum and kanban.
• You also create customizable dashboards
Work Item
A work item can track various activities, such as:
Tasks to do
Bugs to fix
Issues or any assignable work to track progress
Kanban Board 📃
Kanban is a visual method for managing and optimizing work items. It helps teams keep track of their tasks efficiently. The board is typically divided into stages such as:
To-do
In-progress
Done
Azure Boards Processes
Azure Boards offers several process templates to track work items:
Basic: A simple model with Issues, Tasks, and Epics.
Agile
Scrum
CMMI
#### Work Item Types in Basic Process
Epics: Large work items that group related issues and tasks, e.g., Website updates, Cloud migration, CI/CD implementation.
Issues: Divisions of Epics into more specific items, e.g., Homepage, secure sign-in.
Tasks: Smallest units of work assignable to someone, e.g., designing a homepage header, fixing CSS.
#### Scrum Process Work Items
User Stories: Small pieces of functionality from an end user's perspective.
Tasks: Breakdown of user stories into manageable tasks.
Bugs: Defects or issues identified during development or testing.
Epics: Larger bodies of work that can be broken down into multiple user stories.
Features: Functional groups of user stories or larger pieces of work.
Product Backlog: A prioritized list of all work items for the project.
Sprint Backlog: Subset of the product backlog committed to during a sprint.
Impediments: Obstacles hindering the team's progress.
Test Cases: Conditions to validate system functionality.
#### Defining Sprints 📅
A sprint, also known as an iteration in Azure DevOps, is a set period (typically 2-4 weeks) during which specific work items must be completed. Sprints help maintain focus and culminate in a retrospective meeting to review accomplishments and plan for the next sprint.
Acceptance Criteria
Conditions or requirements a work item must meet to be considered complete in Scrum. They define when a work item is "done."
Key Roles in Agile/Scrum 🕵️‍♂️
Product Owner: Represents the customer, defines product requirements, prioritizes the backlog, and ensures the team focuses on valuable features.
Scrum Master: Facilitates Scrum processes, ensures adherence to rules, removes impediments, and helps the team improve. They also facilitate retrospective meetings.
Development Team: A cross-functional group delivering a potentially shippable product increment each sprint. They self-organize and collaborate to achieve sprint goals.
Stakeholders: Interested individuals or groups providing input and feedback. They may attend sprint reviews and demos to assess progress.
Scrum Team: Comprises the Product Owner, Scrum Master, and Development Team, working together to deliver a product increment.
Customers/Users: The ultimate consumers of the product or service, whose needs and feedback shape the product.
Management: Leadership supporting the Scrum Team, removing organizational impediments, and aligning the project with business goals.
External Vendors/Partners: Entities providing specific components or services integrating into the project.

#### Azure Repos -
• Azure Repos supports two types of version control systems:
#### Git
Git is the most popular distributed version control system. It enables developers to:
Download the entire code repository locally with all versions.
Make changes remotely/offline.
Sync changes to the remote server.
Interacting with Git:
Git Clients: Git for Windows, VSCode, etc.
Hosting Services: To host your codebase (repositories), you can use services like GitHub, Azure Repos, Bitbucket, GitLab, etc.

#### TFVC (Team Foundation Version Control)
TFVC is a centralized version control system. Key features include:
Only a single version of the codebase is downloaded locally.
Historical data is maintained on the central server.
Hosting TFVC:
Hosting services include Perforce, SVC, Azure Repos, etc.
Azure Pipelines -
• We can use Azure pipelines to automatically build, test and deploy code and make it available for other targets.
Azure Test Plans -
• With Azure test plans teams can use features offered to plan manual test exploratory test and user acceptance testing and gathering feedback from stakeholders.
• Tests are organized as test plans and test suites by tester and team leads.

#### Azure artifacts
• Test exploratory tests and user acceptance testing and gathering feedback from stakeholders
• Tests are organized as test plans and test suites by tester and team leads
• With Azure artifacts we can create share nugget npm Python and marvel package from public and private sources with teams in Azure devops extension Marketplace
• With Azure artifacts we can create share nuget npm Python and maven package from public and private sources with teams in Azure devops
• extension Marketplace


 #### Azure Pipelines
• Azure pipeline is a cloud service offered by Azure platform to automate building testing releasing face of your development cycle (CI CD)
• Azure pipeline works with the following schema.
• To use Azure pipelines we need to create a pipeline a pipeline in azure devops can be create in two ways
- 1. Using the classic interface
- 2. Using YAML.
• In Jenkins to define the pipeline we create a Jenkins file where we had option to create a scripted pipeline or declarative pipeline
• In the case of Azure devops we create a Azure pipeline yml file to define the pipeline
• Pipeline starts from a trigger a manual a push inside repository or schedule
• Pipeline is generally composed of one or more stages. Each stage contains one or more jobs.
• Each job runs on a agent and it has steps
• Each steps is composed to task that performs some actions
• The final output of the pipeline is an artifact

#### Build agents-
• To build and deploy code using Azure pipeline we need at least one agent
• Agent is a service that runs the job define in pipeline
• Execution of this jobs occur directly on agents host machine
• When defining agents for the pipeline we have to possible agents

1. Microsoft hosted agents - This is service managed by Microsoft and its cleared on every execution of pipeline

2. Self hosted agents - This is a service which you set up and manage yourself this can be custom VM on Azure or on premise in the self hosted agent you need the install the necessary software’s to perform bills a self hosted agents can be windows Linux, Mac or container



#### How do you create a service connection in Azure DevOps?
To create a service connection in Azure DevOps:
Navigate to the project settings in Azure DevOps.
Select "Service connections" under the Pipelines section.
Click "New service connection" and choose the type of connection (e.g., Azure Resource Manager).
Follow the prompts to authenticate and configure the connection, providing necessary credentials and permissions.
Save the service connection for use in pipelines and other tasks.


#### 3. What were the things that you were doing in Azure DevOps?
In Azure DevOps, I managed CI/CD pipelines, integrated code repositories with Azure Repos, configured build and release pipelines, set up automated testing, managed package dependencies with Azure Artifacts, and used Azure Boards for project management and tracking work items.


#### 4. Can you explain what Azure Boards are and why someone would use them?
Azure Boards is a service in Azure DevOps that provides tools for planning, tracking, and discussing work across teams. It includes features like Kanban boards, backlogs, sprint planning, and work item tracking. Teams use Azure Boards to manage their workflows, prioritize tasks, and ensure visibility and collaboration on project progress.


#### 5. Are there any other containerization tools that Azure DevOps supports besides containers?
Yes, Azure DevOps supports other containerization tools besides Docker, such as Kubernetes (AKS), Helm for managing Kubernetes applications, and OpenShift. It also integrates with container registries like Azure Container Registry and Docker Hub.



Can you walk me through the project you worked on prior to this organization?
In my previous role, I worked on a project to automate the deployment of a microservices-based application using Azure DevOps. I was responsible for setting up CI/CD pipelines, configuring infrastructure as code using Terraform, and monitoring the application's performance with Azure Monitor and Grafana. The project aimed to improve deployment efficiency and reduce downtime.


6. Have you ever worked on any Java-based projects?
Yes, I have worked on Java-based projects where I set up CI/CD pipelines using Maven and Gradle for build automation, configured unit and integration tests, and deployed applications to environments like Tomcat and JBoss servers using Azure DevOps.
7. Consider a scenario where a person from the development team is writing code in C# or .NET and he's putting his code into repositories.
In this scenario, I would ensure that the code repository (e.g., Azure Repos or GitHub) is set up and configured correctly. I would then create a CI/CD pipeline in Azure DevOps to automate the build, test, and deployment processes for the C# or .NET application, ensuring that code quality and deployment consistency are maintained.
8. Can you create a pipeline till production and walk me through the steps involved?
To create a pipeline till production:
Set up Source Control: Connect the repository (e.g., Azure Repos or GitHub) to Azure DevOps.
Build Pipeline: Define a build pipeline to compile the code, run unit tests, and generate build artifacts.
Release Pipeline: Create a release pipeline to deploy the build artifacts to different environments (e.g., dev, staging, production).
Deploy to Production: Configure the final stage of the release pipeline to deploy to the production environment, including necessary approvals and pre-deployment checks.
Monitor and Rollback: Set up monitoring and alerting to track the deployment and configure rollback mechanisms in case of issues.
9. Can you explain a situation where you had to troubleshoot a problem with an Azure DevOps pipeline?
I once encountered an issue where a build pipeline was failing due to missing dependencies. I reviewed the pipeline logs to identify the error, updated the pipeline configuration to include the necessary dependency installation steps, and tested the pipeline to ensure it completed successfully.
10. How do you use Azure DevOps to collaborate with other developers on a project?
Azure DevOps facilitates collaboration through Azure Repos for code sharing, Azure Boards for tracking tasks and work items, and Azure Pipelines for continuous integration and deployment. Pull requests are used for code reviews, and discussions and comments help maintain communication. Additionally, Azure DevOps integrates with tools like Microsoft Teams and Slack for real-time collaboration.
11. How do you measure the success of an Azure DevOps pipeline? What metrics do you track?
Success is measured by tracking metrics such as build success rate, deployment frequency, mean time to recovery (MTTR), lead time for changes, and change failure rate. These metrics help evaluate the efficiency and reliability of the CI/CD processes and identify areas for improvement.
12. Your team is developing a new microservices application. Describe how you would configure Azure DevOps pipelines to automate building, testing, and deploying the application to different environments with separate configurations.
I would configure a multi-stage pipeline in Azure DevOps:
Build Stage: Compile the code, run unit tests, and create Docker images for the microservices.
Test Stage: Deploy the microservices to a test environment, run integration and end-to-end tests.
Staging Stage: Deploy to a staging environment with configurations matching production, run additional tests.
Production Stage: Deploy to the production environment with separate configuration settings, using approvals and gated deployments to ensure stability.
13. How would you handle a scenario where a developer accidentally deletes a critical commit from the Git repository?
I would use Git reflog to recover the deleted commit. Reflog keeps a record of all references to the commits in the repository, allowing us to identify and restore the missing commit. If necessary, I would also check the backups or use Azure DevOps features like branch policies and pull requests to prevent such incidents in the future.


38. Did you use an Azure pipeline?
Yes, I have used Azure Pipelines for CI/CD purposes.
39. Did you use YAML or normal scripts to write the pipeline?
I used YAML to define Azure Pipelines, as it provides a declarative way to specify the pipeline configuration.
40. If possible, give me an overview of the Azure pipeline.
An Azure pipeline typically consists of the following components:
Pipeline: The top-level component that defines the process of building, testing, and deploying code.
Stages: Logical phases of the CI/CD process, such as build, test, and deploy.
Jobs: A collection of steps that run sequentially within a stage. Each job runs on an agent.
Steps: Individual tasks or scripts that are executed in a job. Common steps include checkout, script, and task.
Triggers: Conditions that trigger the pipeline, such as code commits, pull requests, or schedule-based triggers.
Example of a simple Azure pipeline defined in YAML:
trigger:
- main
pool:
  vmImage: 'ubuntu-latest'

steps:
- task: UsePythonVersion@0
  inputs:
    versionSpec: '3.x'
    addToPath: true

- script: |
    python -m pip install --upgrade pip
    pip install -r requirements.txt
  displayName: 'Install dependencies'

- script: |
    python -m unittest discover
  displayName: 'Run tests'



51. What are the advantages of Azure DevOps?
Integration with Azure: Seamless integration with other Azure services.
Pipeline Automation: Build, test, and deploy automatically.
Collaboration Tools: Work items, boards, and repos help teams collaborate effectively.



