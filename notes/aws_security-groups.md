# Security Groups

![Security Group Overview](https://docs.aws.amazon.com/images/vpc/latest/userguide/images/security-group-overview.png)

A *security group* is like a virtual firewall that controlls all traffic for one or more instances. The ***Security Group Rules*** controlls all ***incoming and outgoing*** traffic that have permission to reach all instances affected by this security group.

All rules are of ***permissive*** type and are **stateful**. This works in compliance with the National Institute of Standards and Technology (NIST).


## Security Group Components
Each *Security Group Rule* has a set of components, some of them are:

- **Protocol**: 6 (TCP), 17 (UDP), 1 (ICMP) or other.

- **Port Range**: 22 (SSH), or for example the interval 2000-3000, separated by a hyphen.

- **ICMP Code Types**: echo-reply or echo-request for example.

- **Origin or Destination**: The source (inbound rules) or destination (outbound rules) for the traffic to allow.

- **(Optional) Description**: A description for this rule, up to 255 characters in length.

For more detailed explanation, refer [here](https://docs.aws.amazon.com/vpc/latest/userguide/security-group-rules.html).

When creating security group rules always try to pass the maximum amount of information possible, this is to avoid leaving security holes. We also try to avoid ***any-to-any*** permissions, like the all ... in the inbound rules.