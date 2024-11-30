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


