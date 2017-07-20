Requirements: 
  *******************************

Create a simple script, using your language of choice, that creates an AWS EC2 instance and outputs its launch time. The script should:

* Utilize the AWS API

* Accept the arguments: AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_REGION, INSTANCE_TYPE

* Wait for an instance to come online, and then return the instance launch time to STDOUT

*******************************

1. This project is written by Ansible. To install Ansible please follow these steps:

$sudo -i

$apt-get update

$apt-get upgrade -y

$wget http://releases.ansible.com/ansible/ansible-latest.tar.gz

$tar -xzvf ansible-latest.tar.gz

$apt-get install -y python-pip python-setuptools python-yaml python-paramiko python-jinja2 python-httplib2 jq python-mysqldb

$pip install boto boto3 awscli

$pip install --upgrade pip

2. Configure and Run the script. 
- set your desired values on "ec2-vars/vars.yml" file. in vars.yml file you can add the values for these followin variables:

"aws_access_key", "aws_secret_key", "ec2_keypair", "ec2_security_group", "ec2_security_group_description", "ec2_instance_type", "ec2_image", "ec2_region", "ec2_tag_Name" and "ec2_tag_Type". 

 - after inserting these values for variables please run the script using this following command:
   $ansible-playbook provision-ec2.yml
   
   
