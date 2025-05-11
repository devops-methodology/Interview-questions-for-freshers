# Interview-questions-for-freshers(MUST ASKED QUESTIONS)


🎯 Objective:
Hire a fresher DevOps Engineer who understands core DevOps concepts, has hands-on practice with tools, and is eager to learn and grow.
________________________________________
📋 Step-by-Step Recruitment Process:
________________________________________
✅ Step 1: Job Description & Role Definition
Role: Junior DevOps Engineer / DevOps Intern
Team: Infrastructure / Platform / CI/CD
Key Responsibilities:
•	Assist in setting up and managing CI/CD pipelines
•	Work with cloud services (mainly AWS/Azure/GCP)
•	Learn and support containerization (Docker) and orchestration (Kubernetes)
•	Basic infrastructure as code (e.g., Terraform)
•	Monitor system health and automate routine tasks
Skills Required:
•	Linux fundamentals
•	Basic scripting (Bash or Python)
•	Git & GitHub workflow
•	CI/CD basics (Jenkins, GitHub Actions)
•	Understanding of containers (Docker)
•	Familiarity with any cloud platform (preferably AWS)
•	Willingness to learn tools like Terraform, Prometheus, Trivy, etc.
________________________________________
✅ Step 2: Resume Screening
What I look for in a fresher:
•	Personal or academic DevOps projects (hosted on GitHub)
•	Hands-on labs/certifications (AWS Cloud Practitioner, DevOps Bootcamps, etc.)
•	Contribution to open source or blogs
•	Curiosity (e.g., home lab, tinkering with Raspberry Pi, etc.)
________________________________________
✅ Step 3: Technical Screening (MCQ / Online Test)
Platform: HackerRank, Codility, or Google Forms
Sections:
•	Linux commands (e.g., grep, chmod, top)
•	Git basics (e.g., git clone, merge, revert)
•	CI/CD flow understanding
•	Basic cloud (e.g., EC2, S3, IAM roles)
•	Debugging simple YAML/JSON files
________________________________________
✅ Step 4: Interview (30–45 min)
Split into 3 rounds:
________________________________________
🔍 Round 1: Technical (Foundational Knowledge)
Topics:
•	Linux commands
•	Git branching & workflow
•	Docker basics (image vs container, Dockerfile)
•	CI/CD concept
•	Cloud basics (e.g., difference between EC2 and Lambda)
Sample Questions:
1.	What happens when you run git pull origin main?
2.	What is a Dockerfile and why do we use it?
3.	Explain a simple CI/CD pipeline you have worked on or read about.
4.	What is the purpose of .gitignore?
5.	Can you explain what “infrastructure as code” means?
________________________________________
🔧 Round 2: Hands-on Task or Take-Home Assignment
Task Options (pick one):
•	Create a simple CI/CD pipeline using GitHub Actions that builds a Docker image and pushes it to Docker Hub
•	Write a Terraform file to deploy an EC2 instance
•	Containerize a basic Node.js/Python app using Docker
Evaluation Criteria:
•	Folder structure
•	Clean and working code
•	Documentation (README)
•	Use of best practices
________________________________________
🤝 Round 3: Culture Fit & Communication
Questions:
1.	Tell me about a time you struggled with a technical problem — how did you solve it?
2.	Why DevOps?
3.	What DevOps tools are you most curious about?
4.	How do you stay updated with technology?
________________________________________
🛠️ Tech Stack & Tools to Learn (as a Fresher):
Area	Tools/Tech
OS & CLI	Linux (Ubuntu), Bash
Version Control	Git, GitHub
Scripting	Bash, Python (basics)
Containers	Docker
CI/CD	GitHub Actions, Jenkins
IaC	Terraform (basic setup of AWS resources)
Cloud	AWS (EC2, S3, IAM, VPC)
Monitoring	Prometheus, Grafana (intro level)
Security	Trivy (for scanning images)
________________________________________
🧠 Bonus Tips for Candidates:
•	Build a GitHub portfolio with at least 3 projects: Dockerize an app, set up CI/CD, deploy to AWS.
•	Document your learning in blogs or LinkedIn posts.
•	Get AWS Cloud Practitioner certification (great signal for recruiters).
Great! Here's a DevOps Fresher Mock Interview Question Set you can practice with. It covers foundational areas like Linux, Git, CI/CD, Docker, AWS, and Terraform.
________________________________________
🧪 DevOps Fresher – Mock Interview Questions
________________________________________
🐧 Section 1: Linux Basics (5 questions)
1.	What does the command chmod +x script.sh do?
•  chmod: stands for change mode – it modifies file permissions.
•  +x: adds the execute (x) permission.
•  script.sh: the name of the shell script file you're modifying.


2.	How would you find a specific word in a log file using the command line?
grep "error" app.log
🔍 Explanation:
grep: searches for patterns in text.

"error": the word you're searching for (case-sensitive).

app.log: the log file to search in.

3.	What is the difference between top, htop, and ps?
top: display real time information about cpu, memory tasks and processes
htop: more visually indicators—cpu bar,memory graphs,scrollable lists,(f9) easy to kill process.
ps: show a snapshot of running processes.  

4.	What does the command df -h show?
df: disk file systems
-h : human readable format(mb,kb or gb)
5.	How do you list all the environment variables in Linux?

printenv: to list all environment variables in linux
env: also shows all env variables
export: list all exported environment variables
$HOME: to view specific variables 
________________________________________
🧪 Section 2: Git & Version Control (5 questions)
1.	Explain the difference between git pull and git fetch.
 Git fetch: Download all the commits,branches and tags but don’t merge
                 You can see before merging
                git fetch origin
git pull:
download and merge (combines git fetch and git merge)
it pulls the latest changes and merges in the current branch
git pull origin main
2.	How do you undo the last commit in Git without deleting your changes?
git reset --soft head~1
git reset: moves your current branch to different commit
--soft: keep all your changes staged
head~1:commit before the last one
(the last commit is removed from the history and you can recommit,fix the changes with a message)

But if you want to unstage the changes (only keep the code)
git reset --mixed head~1

3.	What is a merge conflict and how do you resolve it?

Lets say you and your team mate both are editing same line in app.py in two different branches ,so then there will be conflict.
You can edit it manually.
(Note:
Carefull: always talk with the team pull regularly before pushing)
4.	What is the purpose of .gitignore?
Ignore that file or env variables to commit,it keeps repository clean any unnecessary commits.
5.	How do you clone a repository and switch to a specific branch?
git clone –b main<any branch-name you want to jump> https://github.com/devops-methodology/Interview-questions-for-freshers.git
________________________________________
⚙️ Section 3: CI/CD Concepts (5 questions)
1.	What is CI/CD and why is it important?
CI(Continous integration): it is the automation of building and testing of a code when the developer commits the code, early detection of bugs.
CD(continous deployment/delivery):automatically delivers the code to production/staging(will be deployment and if manually then delivery).
Faster development,reduce manual errors ,faster software releases,improves code quality


2.	What are the main stages in a typical CI/CD pipeline?
Git Checkout:cloned the git repo
mvn compile :compile the code ,any syntax based error or something
mvn test: runs unit tests for the functionality of the code(means wheather the code behaves as expected)
trivy fs scan: scan the file system that any vulnerabilities in dependencies and config files. 
Sonarqube analysis:from that report it checks any code bugs,code smells or any security issues (also analyzes code quality)
Code bugs:programming errors may cause app crash
Code smells: issuing poor code practices,later on we can extend or code hard to maintain
Sonarqube quality gate check: code meets the predefined quality which was mentioned in quality gate.
mvn package: package the compiled code into distributed files like war or jar to 
mvn deploy: deploy the build packages to remote maven repo/nexus repo(where versioning can be possible)
maven-snapshots:for development server
maven-releases: for production server
docker build image and tag that for versioning.
Trivy image scan: before deploying for any security issues we have to scan
Any vulnerabilities/big image.
Deploy to kubernetes: deploy the containerized application to k8s for execution.
Install Prometheus and grafana using helm which is very easy for using that..
Then use an ingress or kubectl-port-forward 
Then use grafana alerts (via emai)


3.	How would you set up a CI/CD pipeline for a Node.js or Python project in Jenkins?
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Lint Code') {
            steps {
                sh 'npm run lint'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy to server or Kubernetes here'
                // Example: sh 'kubectl apply -f k8s.yaml'
            }
        }
    }
}
4.	What’s the difference between build, test, and deploy stages?
Build: converts the source code into executable package (jar,zip or docker images)
Test: run automated checks (unit/integration test),code is working as expected or not
UNIT TESTS:Checks individual tests at the same time lets say testing individual functions at the same time in an isolation.
Integration test:it tests multiple components lets say api with another api or db with api working properly or not.
Deploy: delivers the build and tested application to an environment like (production,stag or kubernetes)

________________________________________
🐳 Section 4: Docker & Containers (5 questions)
1.	What is the difference between an image and a container?
Image is a static,read only template with application code and dependencies while container is the running instance of that image.
2.	What does this Dockerfile line do: FROM python:3.8-slim?
Means the base image should be python:3.8 and slim means:slim downed version to the reduce the image size with some provided python environment.

3.	How do you build and run a Docker image?
docker build –t <image-name> .(for build)
docker run –d/-it --name <container-name >  -p hostport:container port <container-image>
4.	What command would you use to see all running containers?
docker ps 
docker ps –a(including stopped ones)
5.	How do you expose a port in Docker?
Docker run –p hostport:containerport <image-name>

________________________________________
☁️ Section 5: Cloud Basics (AWS-focused) (5 questions)
1.	What is EC2 and how is it different from Lambda?
Ec2 is a virtual server which is fully managed by you, there you can fully manage over networking,storage and environment,,you pay for the computing capacity wheather you use or not,it is usually used for long running tasks.
Where lambda is used for specific functions and you are billed when ever the computing capacity is used(only the resources you used during execution)without managing the infrastructure,also the workload scales up accord to the requirement,used for short driven events or short tasks like any tests.
2.	What’s the purpose of IAM roles in AWS?
IAM roles gives the temporary access to resources or services without giving credentials for long terms..
3.	What’s the difference between S3 and EBS?
S3 is an object storage service which stores unstructured data like files,images and backups.
EBS:elastic block storage stores for ec2 instance like databases,apps,os files also.
4.	How would you deploy a static website on AWS?
Create an s3 bucket,then enable static website hosting in bucket settings,upload your static files(html,css,etc),set bucket policy allow public for read access(for website content),access the site through static website endpoint 
5.	What is the purpose of security groups?
Control inbound and outbound traffic to ec2 instances and other resources by allowing or denying specific IP address,ports and protocols.
________________________________________
📜 Section 6: Terraform & Infrastructure as Code (3 questions)
1.	What is Terraform and why do we use it?
It’s a IAS(infrastructure as code)used to manage,provision and version cloud infrastructure like AWS,GCP or azure cloud).
Used:automated and consistent infrasture deployment.
           Support version control and repeated environments.
            Works across multiple cloud providers in one language.
simple Terraform example to deploy an AWS EC2 instance?
main.tf
provider “aws” {
 region = “ap-south-1”
resource = “aws_instance”  {
ami  = ami-i(lets say amazon lixnu2)
instance_type = t2-medium
tags {
Name = “first -instance”
}
}
terraform init:to initialize the directory
terraform plan: it will give the structure what it will create accord your requirement
terraform apply –auto-approve: apply the configuration which you have defined in main.tf file
terraform destroy :it will destroy all the resources/services which you have created.

2.	What are providers and resources in Terraform?
providers: cloud platforms interact with the services like aws,azure or kubernetes
resources: infrastructure components which will created or managed like ec2-instances,s3 bucket or vpc
3.	How do you initialize and apply a Terraform script?
Terraform init
Terraform apply
________________________________________
🧠 Bonus: Behavioral Questions (2–3 questions)
1.	Tell me about a DevOps project you’ve worked on (even if it’s personal or academic).
2.	What tools are you currently learning and why?
3.	How do you approach learning a new tool or solving a technical problem?

Similar questions asked almost in any interviews
