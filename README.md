# How to use a Terraform module 

In this repository you will create an AWS VPC using a module from the [Terraform Registry](https://registry.terraform.io/modules/terraform-aws-modules/vpc/aws/2.21.0?tab=inputs). 

This will show you how to simply use the modules other people build and provided for you.

This Repository is based on the following [tutorial](https://learn.hashicorp.com/tutorials/terraform/module-use?in=terraform/modules). 


# Prerequisites
Install terraform [See documentation](https://learn.hashicorp.com/tutorials/terraform/install-cli?in=terraform/aws-get-started)

Install AWS cli [See documentation](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

# How to

## create the infrastructure
1. Clone the repository to your local machine
```
git clone https://github.com/munnep/learn-terraform-modules-use.git
```
2. Change your directory
```
cd learn-terraform-modules-use
```
3. Notice the use of the module being used in the ```main.tf```
```
module "vpc" {
  source  = "terraform-aws-modules/vpc/aws"
  version = "2.21.0"

```  
4. Terraform initialize
```
terraform init
```
5. Notice the download of the module 
```
Initializing modules...
Downloading terraform-aws-modules/ec2-instance/aws 2.12.0 for ec2_instances...
- ec2_instances in .terraform/modules/ec2_instances
Downloading terraform-aws-modules/vpc/aws 2.21.0 for vpc...
- vpc in .terraform/modules/vpc
```
6. Terraform plan
```
terraform plan
```
7. Terraform apply
```
terraform apply
```
8. destroy the infrastructure
```
terraform destroy
```