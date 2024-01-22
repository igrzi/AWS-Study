# Virtual Private Networks

## What is a VPN

A ***Virtual Private Network (VPN)*** is a technology that allows for secure connections between two distinct points, isolating all traffic through private and encrypted tunnel

## What types of VPNs we have on AWS

### ***Site-to-site***:

A IPsec VPN is created between our VPCs and a remote network. It allows you to extend your on-premises network to the AWS cloud.

### ***VPN Client***:

It's a VPN Service managed on the client, allowing you to securely use AWS in your local network through configured endpoints with a VPN with TLS protocol.

### ***CloudHub***:

This is used when you have more than one remote network, you can create ***multiple AWS Site-to-site VPNs through a virtual private gateway*** allowing the communication between networks.

### ***3rd party softwares***:

You can create a VPN connection to our remote network using an **Amazon EC2 instance** that is running a 3rd party VPN Software. **This is the cheapest option on most of the time**.
