# Intro

We create EC2 Instances with the help of Ansible playbook i.e. ec2_play.yml

# Understanding the ec2_play.yml

1. Here the hosts is localhost, because we are creating ec2 Instances from this server machine only.
2. It has 2 tasks:
    A) Creating set of ec2 Instances
    B) Creating debug
    
  # A) Creating set of ec2 Instances:
        i. Group means security group of the server machine.
       ii. exact_count means No. of ec2 Instances to create.
      iii. Register means to save all the information related to the results of this playbook.
       iv. Point to note is that, the Group name and the Image name must match the region.
      
  # B) Creating debug:
        i. "msg" this is used to display all the data that is stored in the Register.

# Note:

Here, we are assigning a Role to our ec2 instance(Ansible) Master that has a policy attached "AdministratorAccess",
so that this ec2 can log-in to the AWS, as we are not using the key parameter here for security reasons.
