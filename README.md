# Jenkins Remoting Project

## Overview

This project sets up a Jenkins master-agent architecture using AWS EC2 instances.

## Prerequisites

- AWS Account
- Two Ubuntu EC2 Instances (Master & Agent)
- SSH Key for AWS

## Setup Steps

### 1. Configure the Master Node

1. SSH into the master instance

2. Run the Jenkins installation script

3. Get the initial admin password:
   
4. Open Jenkins on `http://<master-public-ip>:8080` and complete setup.

### 2. Configure the Agent Node

1. SSH into the agent instance:
 
2. Run the agent configuration script:
   
3. Copy the public key and add it to the master node's authorized keys:
   

### 3. Register the Agent in Jenkins

1. In Jenkins UI, go to Manage Jenkins → Manage Nodes and Clouds.

2. Click New Node, name it.

3. Choose Permanent Agent, configure:
   Remote root directory: /home/jenkins
   Launch method: Launch agent via SSH
   Host: <agent-private-ip>
   Credentials: Add SSH private key

4. Click Save and Connect. The agent should appear as Online.

### 4. Running Builds and Jobs 

shell command - apply and save to check it build in agent node.
