# Virtual Private Cloud

### What it is?

It's a ***Virtual Network Layer*** that allows the user to isolate AWS resources without exterior or interior (other networks/AWS accounts) interference.

This means you can have isolated environments, that **only your AWS account** can have access to those resources. You can also have more than 1 VPC on an environment, separating homolog and production environments without those ***"talking"*** to each other.

### Main VPC Concepts

- **VPC**: Your virtual network account

- **Subnet**: Range of IP addresses

- **Routing Tables**: Set of rules to set where network traffic should be redirected

- **Internet Gateway**: A gateway that allows to access other resources from VPC and the Internet

- **VPC endpoints**: This allows to connect your VPC to other AWS compatible services, and VPC endpoints developed by PrivateLink without having to connect through the internet, NAT device, VPN connection or AWS Direct Connect.
