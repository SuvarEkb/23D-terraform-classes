terraform-task1
TASK #1:

With Terraform:

Create a VPC named ‘wordpress-vpc’ (add name tag).

Create an Internet Gateway named ‘wordpress_igw’ (add name tag).

Create a route table named ‘wordpess-rt’ and add Internet Gateway route to it (add name tag).

Create 3 public and 3 private subnets in the us-east region (add name tag). Associate them with the ‘wordpess-rt’ route table. What subnets should be associated with the ‘wordpess-rt’ route table? What about other subnets? Use AWS documentation.

Create a security group named ‘wordpress-sg’ and open HTTP, HTTPS, SSH ports to the Internet (add name tag). Define port numbers in a variable named ‘ingress_ports’.

Create a key pair named ‘ssh-key’ (you can use your public key).

Create an EC2 instance named ‘wordpress-ec2’ (add name tag). Use Amazon Linux 2 AMI (can store AMI in a variable), t2.micro, ‘wordpress-sg’ security group, ‘ssh-key’ key pair, public subnet 1.

Create a security group named ‘rds-sg’ and open MySQL port and allow traffic only from ‘wordpress-sg’ security group (add name tag).

Create a MySQL DB instance named ‘mysql’: 20GB, gp2, t2.micro instance class, username=admin, password=adminadmin. Use ‘aws_db_subnet_group’ resource to define private subnets where the DB instance will be created.

You have to install wordpress on 'wordpress-ec2'. Desired result: on wordpress-ec2-public-ip/blog address, you have to see wordpress installation page. You can install wordpress manually or through user_data.

Submit your Terraform code.

Helpful resources:

Deploy WordPress with Amazon RDS https://aws.amazon.com/getting-started/hands-on/deploy-wordpress-with-amazon-rds/

Install LAMP on Amazon Linux 2 - Amazon Elastic Compute Cloud https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-lamp-amazon-linux-2.html
