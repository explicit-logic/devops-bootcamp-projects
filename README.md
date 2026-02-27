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
