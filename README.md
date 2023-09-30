# Terraform
Terraform scripts and how to install terraform on linux
Terraform Installation And Setup In AWS EC2 Redhat Instnace.
Prerequisite
AWS Acccount.
Create Redhat EC2 Instnace.
Create IAM Role With Required Polocies.
VPCFullAccess
EC2FullAcces
S3FullAccess ..etc
Attach IAM Role to EC2 Instance.
Install Terraform
$ sudo yum install wget unzip -y
$ wget https://releases.hashicorp.com/terraform/0.12.26/terraform_0.12.26_linux_amd64.zip
$ sudo unzip terraform_0.12.26_linux_amd64.zip -d /usr/local/bin/
# Export terraform binary path temporally
$ export PATH=$PATH:/usr/local/bin
# Add path permanently for current user.By Exporting path in .bashrc file at end of file.
$ vi .bashrc
   export PATH="$PATH:/usr/local/bin"
# Source .bashrc to reflect for current session
$ source ~/.bashrc   
Clone terraform scripts
$ git clone https://github.com/MithunTechnologiesDevOps/Terraform_Scripts.git
$ cd Terraform_Scripts
Update Your Key Name in variables.tf file before executing terraform script.
Infrastructure As A Code
Create Infrastructure(VPC,Subnets,Route Tables,EC2 Instnaces ..etc) As A Code Using Terraform Scripts
# Initialise to install plugins
$ terraform init VPC/
# Validate teffaform scripts
$ terraform validate VPC/
# Plan terraform scripts which will list resources which is going  be created.
$ terraform plan VPC/
# Apply to create resources
$ terraform apply --auto-approve VPC/
Destroy Infrastructure
$ terraform destroy --auto-approve VPC/
