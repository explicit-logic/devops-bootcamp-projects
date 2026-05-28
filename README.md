# DevOps Bootcamp Projects

A list of demo projects completed during the [TechWorld with Nana – DevOps Bootcamp](https://www.techworld-with-nana.com/devops-bootcamp). These projects demonstrate practical implementations of core DevOps concepts, tools, and workflows.

### 1. Create server and deploy application on DigitalOcean

**Module:** 5 - Cloud & IaaS Basics - DigitalOcean

**Repository:** https://github.com/explicit-logic/iaas-module-5

**Technologies:** `DigitalOcean` `Linux` `Java` `Gradle`

**Project Description:** This project demonstrates how to deploy a Java Gradle application to a DigitalOcean droplet using basic cloud and Linux concepts.

---

### 2. Run Nexus on Droplet and Publish Artifacts to Nexus

**Module:** 6 - Artifact Repository Manager with Nexus

**Repository:** https://github.com/explicit-logic/artifact-module-6

**Technologies used:** `Nexus` `DigitalOcean` `Linux` `Java` `Gradle` `Maven`

**Project Description:**
- Install and configure Nexus from scratch on a cloud server
- Create new User on Nexus with relevant permissions
- Java Gradle Project: Build Jar & Upload to Nexus
- Java Maven Project: Build Jar & Upload to Nexus

---

### 3. Use Docker for local development

**Module:** 7 - Containers with Docker

**Repository:** https://github.com/explicit-logic/docker-module-7.1

**Technologies used:** `Docker` `Node.js` `MongoDB` `MongoExpress`

**Project Description:**
- Create `Dockerfile` for Nodejs application and build Docker image
- Run Nodejs application in Docker container and connect to `MongoDB` database container locally.
- Also run `MongoExpress` container as a UI of the `MongoDB` database.

---

### 4. Create Docker repository on Nexus and push to it

**Module:** 7 - Containers with Docker

**Repository:** https://github.com/explicit-logic/docker-module-7.5

**Technologies used:** Docker, Nexus, DigitalOcean, Linux

**Project Description:**

- Create Docker hosted repository on Nexus
- Create Docker repository role on Nexus
- Configure Nexus, DigitalOcean Droplet and Docker to be able to push to Docker repository
- Build and Push Docker image to Docker repository on Nexus

---

### 5. Deploy Docker application on a server with Docker Compose

**Module:** 7 - Containers with Docker

**Repository:** https://github.com/explicit-logic/docker-module-7.6

**Technologies used:** Docker, Nexus, Node.js, MongoDB, MongoExpress

**Project Description:**

- Copy Docker-compose file to remote server
- Login to private Docker registry on remote server to fetch our app image
- Start our application container with MongoDB and
- MongoExpress services using docker compose

---

### 6. Deploy Nexus as Docker container

**Module:** 7 - Containers with Docker

**Repository:** https://github.com/explicit-logic/docker-module-7.7

**Technologies used:** Docker, Nexus, DigitalOcean, Linux

**Project Description:**

- Create and Configure Droplet
- Set up and run Nexus as a Docker container

---

### 7. Install Jenkins on DigitalOcean

**Module:** 8 - Build Automation & CI/CD with Jenkins

**Repository:** https://github.com/explicit-logic/jenkins-module-8.1

**Technologies used:** Jenkins, Docker, DigitalOcean, Linux

**Project Description:**

- Create an Ubuntu server on DigitalOcean
- Set up and run Jenkins as Docker container
- Initialize Jenkins

---

### 8. Create a CI Pipeline with Jenkinsfile (Freestyle, Pipeline, Multibranch Pipeline)

**Module:** 8 - Build Automation & CI/CD with Jenkins

**Repository:** https://github.com/explicit-logic/jenkins-module-8.2

**Technologies used:** Jenkins, Docker, Linux, Git, Java, Maven

**Project Description:**

- Install Build Tools (Maven, Node) in Jenkins
- Make Docker available on Jenkins server
- Create Jenkins credentials for a git repository
- Create different Jenkins job types (Freestyle, Pipeline, Multibranch pipeline) for the Java Maven project with Jenkinsfile to:
  - a. Connect to the application’s git repository
  - b. Build Jar
  - c. Build Docker Image
  - d. Push to private DockerHub repository

---

### 9. Create a Jenkins Shared Library

**Module:** 8 - Build Automation & CI/CD with Jenkins

**Repository:** https://github.com/explicit-logic/jenkins-module-8.3

**Technologies used:** Jenkins, Groovy, Docker, Git, Java, Maven

**Project Description:**

Create a Jenkins Shared Library to extract common build logic:

- Create separate Git repository for Jenkins Shared Library project
- Create functions in the JSL to use in the Jenkins pipeline
- Integrate and use the JSL in Jenkins Pipeline (globally and for a specific project in Jenkinsfile)

---

### 10. Configure Webhook to trigger CI Pipeline automatically on every change

**Module:** 8 - Build Automation & CI/CD with Jenkins

**Repository:** https://github.com/explicit-logic/jenkins-module-8.4

**Technologies used:** Jenkins, GitHub, Git, Docker, Java, Maven

**Project Description:**

- Install GitHub Plugin in Jenkins
- Configure GitHub access token and connection to Jenkins in GitHub project settings
- Configure Jenkins to trigger the CI pipeline, whenever a change is pushed to GitHub

---

### 11. Dynamically Increment Application version in Jenkins Pipeline

**Module:** 8 - Build Automation & CI/CD with Jenkins

**Repository:** https://github.com/explicit-logic/jenkins-module-8.5

**Technologies used:** Jenkins, Docker, GitHub, Git, Java, Maven

**Project Description:**

- Configure CI step:Increment patch version
- Configure CI step: Build Java application and clean old artifacts
- Configure CI step: Build Image with dynamic Docker Image Tag
- Configure CI step: Push Image to private DockerHub repository
- Configure CI step: Commit version update of Jenkins back to Git repository
- Configure Jenkins pipeline to not trigger automatically on CI build commit to avoid commit loop

---

### 12. Deploy Web Application on EC2 Instance (manually)

**Module:** 9 - AWS Services

**Repository:** https://github.com/explicit-logic/aws-module-9.1

**Technologies used:** AWS, Docker, Linux

**Project Description:**

- Create and configure an EC2 Instance on AWS
- Install Docker on remote EC2 Instance
- Deploy Docker image from private Docker repository on EC2 Instance

---

### 13. CD - Deploy Application from Jenkins Pipeline to EC2 Instance (automatically with docker)

**Module:** 9 - AWS Services

**Repository:** https://github.com/explicit-logic/aws-module-9.2

**Technologies used:** AWS, Jenkins, Docker, Linux, Git, Java, Maven, Docker Hub

**Project Description:**

- Prepare AWS EC2 Instance for deployment (Install Docker)
- Create ssh key credentials for EC2 server on Jenkins
- Extend the previous CI pipeline with deploy step to ssh into the remote EC2 instance and deploy newly built image from Jenkins server
- Configure security group on EC2 Instance to allow access to our web application

---

### 14. CD - Deploy Application from Jenkins Pipeline on EC2 Instance (automatically with docker-compose)

**Module:** 9 - AWS Services

**Repository:** https://github.com/explicit-logic/aws-module-9.3

**Technologies used:** AWS, Jenkins, Docker, Linux, Git, Java, Maven, Docker Hub

**Project Description:**

- Install Docker Compose on AWS EC2 Instance
- Create `docker-compose.yml` file that deploys our web application image
- Configure Jenkins pipeline to deploy newly built image using Docker Compose on EC2 server
- Improvement: Extract multiple Linux commands that are executed on remote server into a separate shell script and execute the script from Jenkinsfile

---

### 15. Complete the CI/CD Pipeline (Docker-Compose, Dynamic versioning)

**Module:** 9 - AWS Services

**Repository:** https://github.com/explicit-logic/aws-module-9.4

**Technologies used:** AWS, Jenkins, Docker, Linux, Git, Java, Maven, Docker Hub

**Project Description:**

- CI step: Increment version
- CI step: Build artifact for Java Maven application
- CI step: Build and push Docker image to Docker Hub
- CD step: Deploy new application version with Docker Compose
- CD step: Commit the version update

---

### 16. Create repository on AWS and push to private Docker registry

**Module:** 9 - AWS Services

**Repository:** https://github.com/explicit-logic/aws-module-9.5

**Technologies used:** Docker, Amazon ECR

**Project Description:**

- Create private Docker registry on AWS (Amazon ECR)
- Tag and Push Docker image to this private repository

---

### 17. Interacting with AWS CLI

**Module:** 9 - AWS Services

**Repository:** https://github.com/explicit-logic/aws-module-9.6

**Technologies used:** AWS, Linux

**Project Description:**

- Install & configure AWS CLI to connect to our AWS account
- Create EC2 Instance using AWS CLI with all configurations like Security Group
- Create SSH key pair
- Create IAM resources like User, Group, Policy using the AWS CLI
- List and browse AWS resources using the AWS CLI

---

### 18. Deploy MongoDB and Mongo Express into local K8s cluster

**Module:** 10 - Container Orchestration with Kubernetes

**Repository:** https://github.com/explicit-logic/kubernetes-module-10.1

**Technologies used:** Kubernetes, Docker, MongoDB, Mongo Express

**Project Description:**

- Setup local K8s cluster with Minikube
- Deploy MongoDB and MongoExpress with configuration and credentials extracted into ConfigMap and Secret

---

### 19. Deploy Mosquitto message broker with ConfigMap and Secret Volume Types

**Module:** 10 - Container Orchestration with Kubernetes

**Repository:** https://github.com/explicit-logic/kubernetes-module-10.2

**Technologies used:** Kubernetes, Docker, Mosquitto

**Project Description:**

- Define configuration and passwords for Mosquitto message broker with ConfigMap and Secret Volume types

---

### 20. Install a stateful service (MongoDB) on Kubernetes using Helm

**Module:** 10 - Container Orchestration with Kubernetes

**Repository:** https://github.com/explicit-logic/kubernetes-module-10.3

**Technologies used:** K8s, Helm, MongoDB, Mongo Express, DigitalOcean Kubernetes, Linux

**Project Description:**

- Create a managed K8s cluster with DigitalOcean Kubernetes
- Deploy replicated MongoDB service in DOKS cluster using a Helm chart
- Configure data persistence for MongoDB with DigitalOcean block storage
- Deploy UI client Mongo Express for MongoDB
- Deploy and configure nginx ingress to access the UI application from browser

---

### 21. Deploy NodeJS application in K8s cluster from private Docker registry

**Module:** 10 - Container Orchestration with Kubernetes

**Repository:** https://github.com/explicit-logic/kubernetes-module-10.4

**Technologies used:** Kubernetes, Helm, AWS ECR, Docker

**Project Description:**

- Create Secret for credentials for the private Docker registry
- Configure the Docker registry secret in application Deployment component
- Deploy web application image from AWS ECR in K8s cluster

---

### 22. Deploy a Microservices Application on Kubernetes with Production & Security Best Practices

**Module:** 10 - Container Orchestration with Kubernetes

**Repository:** https://github.com/explicit-logic/kubernetes-module-10.5

**Technologies used:** Kubernetes, Redis, Linux, DigitalOcean Managed Kubernetes

**Project Description:**

- Create Kubernetes manifests (Deployments and Services) for all microservices of an online shop application
- Deploy the full microservices stack to a DigitalOcean managed Kubernetes cluster

---

### 23. Create Helm Chart for Microservices

**Module:** 10 - Container Orchestration with Kubernetes

**Repository:** https://github.com/explicit-logic/kubernetes-module-10.6

**Technologies used:** Kubernetes, Helm

**Project Description:**

- Create 1 shared Helm Chart for all microservices, to reuse common Deployment and Service configurations for the services

---

### 24. Deploy Microservices with Helmfile

**Module:** 10 - Container Orchestration with Kubernetes

**Repository:** https://github.com/explicit-logic/kubernetes-module-10.7

**Technologies used:** Kubernetes, Helm, Helmfile

**Project Description:**

- Deploy Microservices with Helm
- Deploy Microservices with Helmfile

---

### 25. Create AWS EKS cluster with a Node Group

**Module:** 11 - Kubernetes on AWS - EKS

**Repository:** https://github.com/explicit-logic/eks-module-11.1

**Technologies used:** Kubernetes, AWS EKS

**Project Description:**

- Configure necessary IAM Roles
- Create VPC with CloudFormation Template for Worker Nodes
- Create EKS cluster (Control Plane Nodes)
- Create Node Group for Worker Nodes and attach to EKS cluster
- Configure Auto-Scaling of worker nodes
- Deploy a sample application to EKS cluster

---

### 26. Create EKS cluster with Fargate profile

**Module:** 11 - Kubernetes on AWS - EKS

**Repository:** https://github.com/explicit-logic/eks-module-11.2

**Technologies used:** Kubernetes, AWS EKS, AWS Fargate

**Project Description:**

- Create Fargate IAM Role
- Create Fargate Profile
- Deploy an example application to EKS cluster using Fargate profile

---

### 27. Create EKS cluster with eksctl

**Module:** 11 - Kubernetes on AWS - EKS

**Repository:** https://github.com/explicit-logic/eks-module-11.3

**Technologies used:** `Kubernetes`, `AWS EKS`, `eksctl`, `Linux`

**Project Description:**

- Create EKS cluster using eksctl tool that reduces the manual effort of creating an EKS cluster

---

### 28. CD - Deploy to EKS cluster from Jenkins Pipeline

**Module:** 11 - Kubernetes on AWS - EKS

**Repository:** https://github.com/explicit-logic/eks-module-11.4

**Technologies used:** `Kubernetes`, `Jenkins`, `AWS EKS`, `Docker`, `Linux`

**Project Description:**

- Install `kubectl` and `aws-iam-authenticator` on a Jenkins server
- Create `kubeconfig` file to connect to EKS cluster and add it on Jenkins server
- Add AWS credentials on Jenkins for AWS account authentication
- Extend and adjust `Jenkinsfile` of the previous CI/CD pipeline to configure connection to EKS cluster

---

### 29. CD - Deploy to DigitalOcean Kubernetes cluster from Jenkins Pipeline

**Module:** 11 - Kubernetes on AWS - EKS

**Repository:** https://github.com/explicit-logic/eks-module-11.5

**Technologies used:** `Kubernetes`, `Jenkins`, `DigitalOcean Kubernetes`, `Docker`, `Linux`

**Project Description:**

- Create K8s cluster on DigitalOcean
- Install `kubectl` as Jenkins Plugin
- Adjust `Jenkinsfile` to use Plugin and deploy to DigitalOcean Kubernetes cluster

---

### 30. Complete CI/CD Pipeline with EKS and private DockerHub registry

**Module:** 11 - Kubernetes on AWS - EKS

**Repository:** https://github.com/explicit-logic/eks-module-11.6

**Technologies used:** `Kubernetes`, `Jenkins`, `AWS EKS`, `Docker Hub`, `Java, Maven`, `Linux`, `Docker`, `Git`

**Project Description:**

- Write K8s manifest files for Deployment and Service configuration
- Integrate deploy step in the CI/CD pipeline to deploy newly built application image from DockerHub private registry to the EKS cluster
- So the complete CI/CD project we build has the following configuration:
   - a. CI step: Increment version
   - b. CI step: Build artifact for Java Maven application
   - c. CI step: Build and push Docker image to DockerHub
   - d. CD step: Deploy new application version to EKS cluster
   - e. CD step: Commit the version update

---

### 31. Complete CI/CD Pipeline with EKS and AWS ECR

**Module:** 11 - Kubernetes on AWS - EKS

**Repository:** https://github.com/explicit-logic/eks-module-11.7

**Technologies used:** `Kubernetes`, `Jenkins`, `AWS EKS`, `AWS ECR`, `Java`, `Maven`, `Linux`, `Docker`, `Git`

**Project Description:**

- Create private AWS ECR Docker repository
- Adjust Jenkinsfile to build and push Docker Image to AWS ECR
- Integrate deploying to K8s cluster in the CI/CD pipeline from AWS ECR private registry
- So the complete CI/CD project we build has the following configuration:
   - a.CI step:Increment version
   - b.CI step: Build artifact for Java Maven application
   - c.CI step: Build and push Docker image to AWS ECR
   - d.CD step: Deploy new application version to EKS cluster
   - e.CD step: Commit the version update

---

### 32. Automate AWS Infrastructure

**Module:** 12 - Infrastructure as Code with Terraform

**Repository:** https://github.com/explicit-logic/terraform-module-12.1

**Technologies used:** `Terraform`, `AWS`, `Docker`, `Linux`, `Git`

**Project Description:**

- Create TF project to automate provisioning AWS Infrastructure and its components, such as: VPC, Subnet, Route Table, Internet Gateway, EC2, Security Group
- Configure TF script to automate deploying Docker container to EC2 instance

---

### 33. Modularize Project

**Module:** 12 - Infrastructure as Code with Terraform

**Repository:** https://github.com/explicit-logic/terraform-module-12.2

**Technologies used:** `Terraform`, `AWS`, `Docker`, `Linux`, `Git`

**Project Description:**

- Divide Terraform resources into reusable modules

---

### 34. Terraform & AWS EKS

**Module:** 12 - Infrastructure as Code with Terraform

**Repository:** https://github.com/explicit-logic/terraform-module-12.3

**Technologies used:** `Terraform`, `AWS EKS`, `Docker`, `Linux`, `Git`

**Project Description:**

- Automate provisioning EKS cluster with Terraform

---

### 35. Complete CI/CD with Terraform

**Module:** 12 - Infrastructure as Code with Terraform

**Repository:** https://github.com/explicit-logic/terraform-module-12.5

**Technologies used:** `Terraform`, `Jenkins`, `Docker`, `AWS`, `Git`, `Java`, `Maven`, `Linux`, `Docker Hub`

**Project Description:**

Integrate provisioning stage into complete CI/CD Pipeline to automate provisioning server instead of deploying to an existing server.

- Create SSH Key Pair
- Install Terraform inside Jenkins container
- Add Terraform configuration to application’s git repository
- Adjust Jenkinsfile to add “provision” step to the CI/CD pipeline that provisions EC2 instance
- So the complete CI/CD project we build has the following configuration:
  - a.CI step: Build artifact for Java Maven application
  - b.CI step: Build and push Docker image to Docker Hub
  - c.CD step: Automatically provision EC2 instance using TF
  - d.CD step: Deploy new application version on the provisioned EC2 instance with Docker Compose

---

### 36. Configure a Shared Remote State

**Module:** 12 - Infrastructure as Code with Terraform

**Repository:** https://github.com/explicit-logic/terraform-module-12.4

**Technologies used:** `Terraform`, `AWS S3`

**Project Description:**

- Configure Amazon S3 as remote storage for Terraform state

---

### 37. Write Countdown Application

**Module:** 13 - Programming with Python

**Repository:** https://github.com/explicit-logic/python-module-13.1

**Technologies used:** `Python`, `PyCharm`, `Git`

**Project Description:**

- Write an application that accepts a user input of a goal and a deadline (date). Print the remaining time until that deadline

---

### 38. Automation with Python — Working with Spreadsheets

**Module:** 13 - Programming with Python

**Repository:** https://github.com/explicit-logic/python-module-13.2

**Technologies used:** `Python`, `PyCharm`, `Git`

**Project Description:**

- Write an application that reads a spreadsheet file and process and manipulate the spreadsheet

---

### 39. API Request to GitHub

**Module:** 13 - Programming with Python

**Repository:** https://github.com/explicit-logic/python-module-13.3

**Technologies used:** `Python`, `PyCharm`, `Git`

**Project Description:**

- Write an application that talks to an API of an external application (GitHub) and lists all the public GitHub repositories for a specified user

---

### 40. Health Check: EC2 Status Checks

**Module:** 14 - Automation with Python

**Repository:** https://github.com/explicit-logic/python-module-14.1

**Technologies used:** `Python`, `Boto3`, `AWS`, `Terraform`

**Project Description:**

- Create EC2 Instances with Terraform
- Write a Python script that fetches statuses of EC2 Instances and prints to the console
- Extend the Python script to continuously check the status of EC2 Instances in a specific interval

---

### 41. Automate configuring EC2 Server Instances

**Module:** 14 - Automation with Python

**Repository:** https://github.com/explicit-logic/python-module-14.2

**Technologies used:** `Python`, `Boto3`, `AWS`

**Project Description:**

- Write a Python script that automates adding environment tags to all EC2 Server instances
