# Intro

There are two EC2 instances running on AWS:
1. Jenkins - This is the master node for our Ansible
2. Client1 - This is the slave node for our Ansible

# Task
We want to configure i.e. install apache on our client machine

# How To
We do this with the help of Jenkins Pipeline and Ansible

On Jenkins :
1. Install the Ansible Plugin
2. Configure Ansible on "Global Tools Configuration"
3. Create a new Pipeline job
4. Provide the ssh credentials for the Client node
5. Use the Jenkinsfile_Ansible

The Jenkinsfile_Ansible file will clone this git which has:
1. hosts - here is where we specify the Client config details such as IP, Username and Password.
2. playbook i.e. apache.yml - here we specify all the task, in our case installing apache
3. index.html - this is the file that is displayed after the successful installation of apache on the Client.
