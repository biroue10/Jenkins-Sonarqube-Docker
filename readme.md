# DevOps Project for Continuous Integration and Deployment

## Overview

This project sets up a continuous integration and deployment (CI/CD) pipeline using Jenkins, SonarQube, and Docker. The pipeline automates the process of building, testing, and deploying code from a GitHub repository. The project leverages three EC2 instances to host Jenkins, SonarQube, and Docker services, respectively.

## Architecture

- **GitHub**: Source code repository
- **Jenkins**: CI/CD automation server
- **SonarQube**: Code quality and security analysis
- **Docker**: Containerization platform
- **EC2 Instances**: Separate instances for Jenkins, SonarQube, and Docker

## Components

1. **GitHub Repository**
   - Codebase: The project code is hosted on GitHub.
   - URL: *(Provide your GitHub repository URL here)*

2. **Jenkins**
   - CI/CD Automation: Jenkins orchestrates the build, test, and deployment pipelines.
   - URL: https://github.com/biroue10/Jenkins-Sonarqube-Docker.git
   - Configuration: Jenkins is configured to pull code from the GitHub repository, run tests, and build Docker images.

3. **SonarQube**
   - Code Quality: SonarQube analyzes the code for quality and security vulnerabilities.
   - URL: *(Provide SonarQube URL here)*
   - Configuration: Integrated with Jenkins to run code quality checks.

4. **Docker**
   - Containerization: Docker is used to build and run containerized applications.
   - URL: *(Provide Docker instance URL here)*
   - Configuration: Docker containers are deployed and managed based on Jenkins builds.

5. **EC2 Instances**
   - **Jenkins EC2 Instance**: Hosts Jenkins server.
   - **SonarQube EC2 Instance**: Hosts SonarQube server.
   - **Docker EC2 Instance**: Hosts Docker containers.

## Setup Instructions

### Prerequisites

- AWS account with EC2 access
- GitHub account
- Basic knowledge of Jenkins, SonarQube, and Docker

### 1. Set Up EC2 Instances

1. **Launch EC2 Instances**:
   - Create three EC2 instances using Amazon Linux 2 or Ubuntu.
   - Ensure each instance has a security group allowing necessary ports (e.g., Jenkins: 8080, SonarQube: 9000, Docker: 80/443).

2. **Install and Configure Jenkins**:
   - SSH into the Jenkins EC2 instance.
   - Install Jenkins using the official instructions: [Jenkins Installation](https://www.jenkins.io/doc/book/installing/)
   - Configure Jenkins and install necessary plugins for GitHub, Docker, and SonarQube integration.

3. **Install and Configure SonarQube**:
   - SSH into the SonarQube EC2 instance.
   - Install SonarQube using the official guide: [SonarQube Installation](https://docs.sonarqube.org/latest/setup/get-started-2/)
   - Configure SonarQube server settings and create a new project for code analysis.

4. **Install and Configure Docker**:
   - SSH into the Docker EC2 instance.
   - Install Docker following the instructions here: [Docker Installation](https://docs.docker.com/engine/install/)
   - Ensure Docker is running and configured to accept connections from Jenkins.

### 2. Configure Jenkins

1. **Integrate with GitHub**:
   - Create a new Jenkins job (e.g., Pipeline or Freestyle project).
   - Configure the job to pull code from your GitHub repository.

2. **Set Up Build and Deployment Pipeline**:
   - Configure Jenkins to build Docker images using Dockerfile from the repository.
   - Push Docker images to a registry or deploy directly to Docker instance.

3. **Integrate with SonarQube**:
   - Install SonarQube Scanner for Jenkins.
   - Configure the Jenkins pipeline to include SonarQube analysis steps.

4. **Configure Notifications**:
   - Set up email notifications or integrate with other tools to alert on build status.

### 3. Final Steps

1. **Push Code to GitHub**:
   - Ensure your code repository is up-to-date and properly configured for the pipeline.

2. **Test the Pipeline**:
   - Trigger a build in Jenkins and verify that the pipeline correctly builds, tests, and deploys your application.
   - Check SonarQube reports and ensure code quality metrics are being captured.

3. **Monitor and Maintain**:
   - Regularly check Jenkins, SonarQube, and Docker for updates and maintenance.
   - Monitor pipeline performance and adjust configurations as needed.

## Contact

For any questions or support regarding this project, please contact:

- **Name**: Biroue Isaac
- **Email**: biroueisaac@gmail.com

## License

This project is licensed under the [MIT License](LICENSE).
