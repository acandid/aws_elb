# Ansible Role: aws_ec2
=========

A simple Ansible role for Create Load Balancer and Add existing EC2 instance to the ELB


Requirements
------------
Before starting you need the following packages on your ansible server
- epel-release
- python2-pip
- boto
- boto3


Role Variables
--------------


None of the variables below are required

| Variables                                    | Default                       | Comments                                                                                |
| :---                                         | :---                          | :---
| `AWS_ACCESS_KEY`			       |			       | Inform AWS ACCESS KEY
|
| `AWS_SECRET_KEY`			       |			       | Inform AWS SECRET KEY
|                                                                                    
| `VPC_ID`                                     |                               | Inform VPC ID
|
| `INSTANCE_TAG`         		       |                               | Inform Instance tag
|
| `AWS_ZONE`                                   |                               | Inform Availability Zone examplo: us-east-1a                                            |
| `AWS_REGION`				       |			       | Inform AWS Region exemplo: us-east-1 # N. Virginia
|						
| `SG_NAME`      			       |			       | Inform Security Group name
|
| `DESC`				       |			       | Inform description for Security Group
| 
| `SRC_IP`      			       |			       | Inform the IP allowed for web site access examplo anywhere: 0.0.0.0/0
|
| `ELB_NAME`     			       |			       | Inform Load Balancer name
| 
| `LB_PROTO`     			       |			       | Inform Load Balancer protocol example: http
|
| `LB_PORT`                                    |                               | Inform Load Balancer http port example: 80
|				               
| `INSTANCE_PORT`                              |                               | Inform Instance EC2 http port example: 80
|
| `LB_SSL_PROTO`                               |                               | Inform Load Balancer protocol example: http
|
| `LB_SSL_PORT`				       |			       | Inform Load Balancer https port example: 443
|
| `FILE_FOR_CHECK`                             |                               | Inform File for healthy check for example: "/index.php"

Dependencies
------------

No dependencies.


Example Inventory File
----------------------

Example Playbook
----------------

---
- hosts: localhost
  connection: local
  gather_facts: false
  roles:
    - /path/aws_elb
...


## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://br.linkedin.com/in/almircandido
