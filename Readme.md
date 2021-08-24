# When we cureate custom VPC in AWS,
- Main Route-Table, Security Group and Network ACL will automatically create. Next need to create 
0. Subnets, like public subnets and private subnet
1. Custom Route-Table, if need
2. Internet Gateway for public instances
3. Default Route to IGW in Route Table
4. NAT Gateway for Private instances
5. Default Route to NAT Gateway

This project will create 
1. Custom VPC
2. Public Subnet 1, 2 and 3 in Each AZ. (Note- default associated to Main Route Table.)
3. Custom Route Table and Associate All Public Subnets
4. Crate Internet Gateway
5. Default Route to IGW in Custome Route Table.
6. Create EC2 instance With userdata in custom VPC' zone-A.
