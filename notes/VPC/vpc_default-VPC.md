# Default VPC

It's a VPC that comes already configured, when we create a new VPC we, the user, need to set all VPC [components](#default-vpc-components)

In ***04/12/2013*** AWS created a Default VPC in each region with a Sub-Net in each Availability Zone ready for use, making a basic **option** that's **ready-to-use** to all instances.

### Default VPC components

- Default **Sub-net** with the address **172.31.0.0/16**, providing ***65.535*** different private addresses

- An Internet Gateway

- A Default Security Group (Firewall Statefull) and ACL (Firewall Stateless)

- Associates a set of DHCP options:
    - DNS Servers
    - Domain Search
    - Gateway
    - NTP Servers

### Default Sub-net

- Per default, the Sub-net is created of ***public*** type

- Sub-nets allow for IPv4 and IPv6 configuration

- In each Sub-net (172.31.0.0/24 - 256 Addresses), some are ***reserved*** and can't be used, those are:

    - 172.31.0.0 - Network address, this address can't be used in **ANY** host service
    - 172.31.0.1 - ***Reserved by AWS*** for VPC routing
    - 172.31.0.2 - ***Reserved by AWS***. Used as a DNS Server
    - 172.31.0.3 - ***Reserved by AWS*** for future use
    - 172.31.0.255 - Broadcast Address, this address can't be used in **ANY** host service