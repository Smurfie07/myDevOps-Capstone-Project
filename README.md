# myDevOps-Capstone-Project

## Part 1: Application and Container Building
..1. <http://www.example.com>
..2. <http://www.example.com>

In this part, you will build two containers using Docker, one for the server and another for the client.

Server:
●	Choose an appropriate base image from the Official Images list.
●	Create a Dockerfile for the server container with the following specifications:
●	Use a volume named "servervol" and mount it at "/serverdata" in the container.
●	Install necessary packages and dependencies required for your server application.
●	Write a server application in your preferred language that does the following:
●	Creates a 1KB file with random text data in the "/serverdata" directory.
●	Sends the file and its checksum to the client.
●	Use Docker Compose to define and run the server container.

Client:
●	Choose an appropriate base image from the Official Images list.
●	Create a Dockerfile for the client container with the following specifications:
●	Use a volume named "clientvol" and mount it at "/clientdata" in the container.
●	Install necessary packages and dependencies required for your client application.
●	Write a client application in your preferred language that does the following:
●	Connects to the server and receives the file.
●	Saves the received file in the "/clientdata" directory.
●	Verifies the file's integrity by checking the received checksum.
●	Use Docker Compose to define and run the client container.

Create two separate Git repositories to host the client and server codebases.

## Part 2: Creating VMs, Infra as a Code (IaC)
... <http://www.example.com>

This part has 3 sub parts:
●	2a. Create two AWS EC2 instances (VMs), one for hosting the server container and another for hosting the client container.
●	2b. Configure the VPC and subnets appropriately to allow communication between the two EC2 instances. Use the t2.micro instance type, which is covered in the AWS free tier.
●	2c. Use Terraform for infrastructure automation. Place your Terraform scripts in the "terraform" directory of your client and server GitHub repositories.


## Part 3: Setting up Monitoring Stack
... <http://www.example.com>

●	Set up a monitoring stack (e.g., Grafana) on each VM.
●	Make the Grafana dashboard accessible at port 3020 of each VM (over the internet, if using EC2 instances).
●	Create appropriate dashboards to view host system metrics and Docker container metrics.


## Part 4: Setting up CI/CD Pipelines
... <http://www.example.com>

●	Create two separate Git repositories for the server and client codebases, if not done already.
●	Set up CI/CD pipelines for both repositories to ensure the following:
●	Images are pushed to a public registry like Docker Hub.
●	Configure the corresponding VMs as private Git runners.
●	Update the image tag in Docker Compose, pull the new image, and deploy it as part of the CD process.
●	Integrate a Slack webhook (or another app of your choice) for deployment notifications.

## Part 5: Documentation

●	Include a README file in each repository with all the necessary information to set up the entire infrastructure and pipeline.
●	Document each step, including prerequisites, installation and configuration instructions, usage examples, and troubleshooting tips.
