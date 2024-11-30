#### What is Maven ? 
What: A build automation tool primarily used for Java projects.
Purpose: Simplifies the build process (compiling code, running tests, packaging, etc.) and manages project dependencies.
How: Uses a pom.xml file to configure projects, list dependencies, and define build steps.


#### Explain the maven goal or lifecycle
1. Validate -   Validation of project. if everything is correct and all necessary information available.
2. Compile - Compile the source code of the project.
3. Test - Test the compiled code using suitable unit testing framework.NOTE- These tests should not require the code to be        packaged.
4. Package -  Take the compiled code and package it in its distributable format. Like JAR, WAR and EAR
5. Verify - Run any check on the result of integration test to ensure quality criteria.
6. Install -  Install packages into local repo, for use as a dependency in another project locally.
7. Deploy - Done in the build env, copies the final package to the remote repo for sharing with other developers and projects.

####  How to Integrate Maven in Jenkins ?
Install Jenkins: Ensure Jenkins is installed and running.
Install Maven: Download and install Maven from Maven's official site.
Configure Maven in Jenkins:
Open Jenkins Dashboard (http://localhost:8080).
Go to Manage Jenkins > Global Tool Configuration.
Under Maven, click Add Maven.
Name it (e.g., Maven 3.6.3).
Check Install automatically or specify the installation path if Maven is installed manually.
Create a New Jenkins Job:
Click New Item.
Name your project and select Freestyle project or Pipeline.
Configure Source Code Management (e.g., Git repository URL).
In the Build section, add Invoke top-level Maven targets.
Enter Maven goals (e.g., clean install).
Build the Job:
Save the configuration.
Click Build Now to start the build.
Check the console output to ensure the build is successful.


#### what are dependencies in maven
   In Maven, dependencies are external libraries or modules that your project needs to compile, build, test, or run. These dependencies are specified in the pom.xml file, which is the project's configuration file. Maven automatically downloads these libraries from a repository and includes them in your project.

#### Explain in short what is setting.xml file in maven
The settings.xml file in Maven is a configuration file used to customize the behavior of Maven for a user or a specific project. There are two locations for this file:
User-specific settings (~/.m2/settings.xml): This file allows individual users to configure their own Maven settings, such as repository locations, server authentication, proxy settings, and profiles.
Global settings (M2_HOME/conf/settings.xml): This file provides a default configuration for all users of a specific Maven installation.
Key uses of settings.xml include:
Defining remote repositories and mirrors for artifact downloads.
Specifying proxy servers for internet access.
Configuring server authentication credentials.
Activating or defining build profiles.
