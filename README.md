# CI/CD Project - Jenkins and tools

# Scenario

- Agile SDLC inactive
- Developers make multiple changes in the codebase per day
- These commits need to be built and tested
- Usually, the Build and Release team need to do these jobs

# Problem

- But Testing is not as frequent as code commits
- Issues and bugs compile up
- Developers need to rework to fix these bugs and error
- A lot of delays due to manual work

# Solution

- Build and test for every commit
- Automated Process
- Notify for every build status
- It will require us to  fix the error and bugs as soon as it  appears

# Benefits

- Short Mean to Repair - no error or bugs compiles up
- No Human intervention   - all steps are automated and don’t need any extra time
- Jenkins - Continous Integration Server
- Git - Version Control System
- Maven - Build Tool
- Check Style - Code analysis
- Slack - Notification
- Nexus - Download and Store versioned artifact / Software repository
- SonarQube - Code analysis server
- We’ll use AWS EC2 instances to setup these servers

# Objective

- Fault Isolation
- Short Mean Time to Repair
- Fast Turn around on feature changes

# Architecture


    

# Flow of Execution

- Create a Key Pair
- Create a Security Group for each Jenkins, Nexus, and SonarQube
- Create EC2 Instances with user data which will provide all required servers
- Post Setup
- Jenkins setup and plugin
- Nexus setup and repo setup
- SonarQube login test
- Git -  Create a GitHub repo and setup a local setup
- Build Job with Nexus Integration
- GitHub Webhook - triggers the job
- SonarQube server Integration Stage
- Nexus artifact upload stage
- Slack Notification