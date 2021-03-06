# When we create custom VPC in AWS, by default
- Main Route-Table
- Security Group
- Network ACL will automatically create.

#  If need, have to create following...
1. Subnets, like public subnets and private subnet
2. Custom Route-Table, if need
3. Internet Gateway for public subnets.
4. Default Route to IGW in Route Table
5. NAT Gateway that is internet access for Private subnets.
6. Default Route to NAT Gateway in Route Table that associated with private subnets.

# This project will create following properties...
 - [custom-vpc.yaml](./Templates/custom-vpc.yaml)
```bash
aws cloudformation create-stack --stack-name custom-vpc --template-body file://custom-vpc.yaml
```
1. Custom VPC
2. Public Subnet 1, 2 and 3 in Each AZ. (Note- default associated to Main Route Table.)
3. Custom Route Table and Associate All Public Subnets
4. Crate Internet Gateway
5. Default Route to IGW in Custome Route Table.
6. Create EC2 instance with userdata in custom VPC' zone-A.
