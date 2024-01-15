# VPC Creation

In the VPC creation menu, in the VPC settings we have 2 main options:
  - VPC only | VPC and more (Default option)

In this VPC and more option, it will create:
  - VPC
  - Subnets
  - Routing Tables
  - Network Connections

Based on the IPv4 CDR block you will have more, or less, amount of available IPs.

We should always work with, at least, 2 availability zones. That we can customize which ones we want.

We can also set teh amount of private and public subnets, that we can also set the CDR blocks.

In the NAT Gateway option, we can set:
  - None
  - Only one gateway
  - One per AZ

Just as a reminder, a NAT Gateway is used to get access to the internet, without exposing any of our private resources to it, it's like a firewall to filter what get's in or out.

We shouldn't use the Default AWS option settings, it's a nice start, but we should always customize it!
Be careful with VPC endpoints and NAT Gateway options, those are paid options, and aren't cheap!

# Subnet creation

- A subnet is a segment of the CIDR block.
- A nice practice is to use tags to categorize public and private subnets

In the subnet creation menu we have some fields to fill.
- Name tag
- The VPC it will be linked to 
- Which AZ to use
- Which IPv4 CIDR block

To determine if a subnet will be private or public is defined by the routing tables
