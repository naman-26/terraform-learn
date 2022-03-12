# Learning Terraform 
This is a repository which showcase my work during the learning process of Terraform.
Different branch of the repository represent different Services implemented through Terraform.
### main branch:
Initialised a VPC, subnet, internet-gateway, and a default route-table on AWS.
### deploy-to-ec2-default-components branch:
Initialised a EC2 server(Amazon Linux), VPC, subnet, internet-gateway, default route-table, security group on AWS.
### eks branch:
Initialised a EKS cluster with worker-groups and kubernetes provider on AWS.
### modules branch: 
Modularized the Terraform files to webserver(create a EC2 instance) and subnet(initialise a subnet). By using modules we can save time and reduce costly errors by re-using configuration written either by ourself, other members of our team, or other Terraform practitioners who have published modules for us to use.
### provisioners branch:
In this branch, I used provisioners for executing entry-srcipt.sh file on the remote EC2 server.
## Initialise
```bash
terraform init
```
## Preview terraform action
```bash
terraform plan
```
## Apply configuration with variables
```bash
terraform apply -var-file terraform-dev.tfvars
```
## Show resources and components from current state
```bash
terraform state list
```
## Destroy a single resource
```bash
terraform destroy -target aws_vpc.myapp-vpc
```
## Destroy everything from tf files
```bash
terraform destroy
```
 
