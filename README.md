# Jenkkins-Notes
## 🧩 What is Jenkins..?
### Ans: Jenkins is an open-source automation tool written in Java, used mainly for Continuous Integration (CI) and Continuous Delivery (CD) — together called CI/CD pipeline.

## 💡 Simple Definition: 
### Jenkins automates the process of building, testing, and deploying your code — so developers can focus on writing code instead of manually deploying or testing.

## ⚙️ Why Use Jenkins?
### Main Features In Jenkins
* Automation	👉 Builds, tests, and deploys automatically when code changes
* Plugins	👉 1,800+ plugins for integration (Git, Docker, Kubernetes, etc.)
* CI/CD Pipeline	👉 Automates the entire development workflow
* Integration	👉 Works with Git, GitHub, Maven, Docker, Terraform, etc.
* Scalability	👉 Can distribute builds across multiple nodes (Master–Slave setup)

## 🧱 Jenkins Architecture
### Main Components Of Architechture
* Jenkins Master	>>>>>> Controls the entire process — schedules jobs, monitors nodes
* Jenkins Agent/Slave	>>>>>>> Executes the build jobs assigned by the master
* Job/Pipeline	>>>>>>> A defined process (like build → test → deploy)
* Plugin	>>>>>> Adds extra features (e.g., Docker plugin, Git plugin)

## 🧰 Basic Jenkins Commands
### Jenkins is mainly managed via a web interface, but here are some useful CLI (Command Line Interface) and service-level commands.

## 🔹 Start, Stop, Restart Jenkins (Linux)
* sudo systemctl start jenkins
* sudo systemctl stop jenkins
* sudo systemctl restart jenkins
* sudo systemctl status jenkins

## 🔹 Access Jenkins
### Open a browser and go to:
* 👉 http://localhost:8080 or http://<server-ip>:8080

## 🔹 Unlock Jenkins (First Time Login)
* sudo cat /var/lib/jenkins/secrets/initialAdminPassword
* 👉 Copy this password and paste it into the Jenkins web interface to unlock.

## 🔹 Jenkins CLI Commands
### (You can run these using jenkins-cli.jar)
### 👉 Connect to Jenkins CLI
* java -jar jenkins-cli.jar -s http://localhost:8080/ list-jobs
### 👉 Create a new job
* java -jar jenkins-cli.jar -s http://localhost:8080/ create-job my-job < config.xml
### 👉 Build a job
* java -jar jenkins-cli.jar -s http://localhost:8080/ build my-job
### 👉 Check job status
* java -jar jenkins-cli.jar -s http://localhost:8080/ get-job my-job

## 🧩 Common Jenkins Tasks:-
### Task In Jenkins
* Create Job	👉 Automate a task (build, deploy, etc.)
* Add Node	👉 Add new build agents/slaves
* Install Plugin	👉 Add integrations like Git, Docker
* Configure Webhooks	👉 Trigger builds automatically when code changes (e.g., from GitHub)
* View Console Output	👉 Check logs of running jobs
