# CI/CD Pipeline Project

This repository demonstrates a CI/CD pipeline using Jenkins, Ansible, and GitHub.

## Components
1. **Jenkins**: Automates the build and deployment process.
2. **Ansible**: Manages the deployment to the target server.
3. **GitHub**: Stores the source code and triggers the pipeline through webhooks.

## Repository Structure
- `index.html`: The HTML file to be deployed.
- `ansible/web.yaml`: Ansible playbook for deployment.
- `ansible/inventory`: Ansible inventory file to specify the target server.

## How It Works
1. Push changes to this repository.
2. GitHub triggers a Jenkins job via webhook.
3. Jenkins runs the pipeline to:
   - Copy `index.html` to the Ansible server.
   - Trigger the Ansible playbook to deploy the webpage to the target server.
4. The webpage is accessible at the target server's public IP.

## Usage
1. Clone this repository.
2. Update the inventory file with your server details.
3. Push changes to trigger the pipeline.

## Requirements
- Jenkins with the "Publish Over SSH" and "GitHub Integration" plugins.
- Ansible installed on the Ansible server.
- Apache2 installed on the target server.


