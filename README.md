# My AWS Infrastructure and Application Stack

This repository contains the code for setting up an AWS infrastructure stack and deploying a web application stack on top of it using Ansible.

## Infrastructure Stack

The infrastructure stack consists of the following components:

- A VPC with 6 subnets (3 public, 3 private)
- An Internet Gateway (IGW)
- Route tables for the subnets
- NAT gateways and Elastic IPs (EIPs) for the private subnets
- Security groups for the bastion host and EC2 instances

To set up the infrastructure stack, follow these steps:

1. Configure your AWS credentials

2. Set up the Site.yaml for VPC and Bastion Host


## Application Stack

The application stack consists of the following components:

- A MySQL database server
- A Memcached server
- A RabbitMQ server
- A Tomcat application server
- An Nginx web server

To set up the application stack, follow these steps:

1. Edit the `output_vars` file to replace the placeholder values with the actual IDs of the resources created in the infrastructure stack.

2. Set up the MySQL database server


3. Set up the Memcached server


4. Set up the RabbitMQ server


5. Set up the Tomcat application server


6. Set up the Nginx web server

## Templates

The `templates` folder contains the Jinja2 templates used by the Ansible playbooks to generate configuration files for the various components of the application stack:

- `appication.j2`: Template for the Tomcat server.xml file
- `nginx.j2`: Template for the Nginx default.conf file
- `tomcat8-ubuntu.j2`: Template for the Tomcat setenv.sh file

You can modify these templates as needed to customize the configuration of your application stack.
