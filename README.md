# Mission 2: Parametrized Deployment Pipeline

## Objective
This project evolves the initial deployment pipeline into a flexible, user-friendly system. It allows users to select specific services for deployment through Jenkins parameters, enhancing the scalability and adaptability of the CI/CD process.

## Key Features
* **Parameterized Selection**: Users can choose which service to deploy (e.g., service1, service2) directly from the Jenkins UI.
* **Dynamic Docker Workflow**: Builds, tags, and pushes the Docker image specifically for the selected service.
* **Targeted Ansible Deployment**: Executes the deployment playbook with configurations tailored to the chosen service.

## Pipeline Stages
1. **User Input**: The pipeline prompts or accepts a parameter for the target service.
2. **Service-Specific Build**: Jenkins builds a Docker image based on the selected service's source code.
3. **Registry Update**: The image is tagged for versioning and pushed to DockerHub.
4. **Automated Deployment**: Ansible ensures the selected service is correctly deployed and configured on the host.

## Outcome
A highly adaptable pipeline that supports multiple service deployments from a single interface, reducing manual configuration and improving workflow efficiency.

## How to Use
1. Select "Build with Parameters" in Jenkins.
2. Choose the desired service from the dropdown menu.
3. Click "Build" to trigger the automated flow.