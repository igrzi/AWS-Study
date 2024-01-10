# Elastic Load Balancer Types

There are 3 different ELB types: 
- [***Application Load Balancer***](#application-load-balancer--http-https)
- [***Network Load Balancer***](#network-load-balancer--tcp-udp)
- [***Gateway Load Balancer***](#)
- [***Classic Load Balancer***](#classic-load-balancer--http-https-tcp)


## Application Load Balancer | (HTTP, HTTPS)
This is a Load Balancer that operates in the 7th layer (Application layer) of the OSI Model.

- Most recommended for HTTP and HTTPS protocols.
- Allow for advanced routing.
- Scales automatically. 
- IP Address ***isn't*** static.
- Client IP Address isn't visible on *Targets*. Only the Load Balancer IP Address is available.
- Multi-AZ 
- Allows for ***stickiness***.

### What is stickiness?

![AWS Stickiness Diagram](https://www.imperva.com/learn/wp-content/uploads/sites/13/2019/01/session-stickiness-diagram.jpg)

It's a feature that enables a load balancer to bind a user's session to a specific instance. This is particularly useful for applications that require **user sessions to be consistently directed to the same server**.

### ALB Routing Algorithms

- [**Round Robin**](https://avinetworks.com/glossary/round-robin-load-balancing/)
- Requisitions based on HTTP Header.
- Requisitions based on paths.
- Requisitions based on source.
- Requisitions based on destination.

## Network Load Balancer | (TCP, UDP)
This is a Load Balancer that operates in the 4th layer (Transport layer) of the OSI Model.

- Most recommended for TCP and UDP protocols.
- Can handle milions of requests per second | Nice for DB requests.
- Scales automatically.
- Allows for ***1 single static IP Address***.
- Multi-AZ
- No SSL terminations.

### NLB Routing Algorithms
Uses [***flow hash***](https://www.linkedin.com/pulse/hash-flow-algorithm-aws-network-load-balancer-nlb-in-depth-mishra) algorithm based on:

- Protocol.
- Source IP Address and port.
- Destination IP Address and port.
- TCP Sequence number.

## Gateway Load Balancer | (IP)
This is a newer addition to AWS, it allows for you to execute, manage and scale ***virtual appliances*** like Firewalls, IDS/IPS and others that support ***GENEVE*** protocol.  
It operates on the 3rd layer (Network layer) of the OSI Model.

- Most recommended for IP protocols.
- Uses [GENEVE](https://www.redhat.com/en/blog/what-geneve) on port 6081 (targets).
- Multi-AZ
- Allows for stickiness.
- Works with ***Health Checks***

## Classic Load Balancer | (HTTP, HTTPS, TCP)
This was the first AWS load balancer, but today it's considered a ***legacy version***.  
Operates in the 7th and *occasionally* 4th OSI layer.

- **Legacy** version for HTTP and HTTPS traffic balancing.
- Doesn't allow for advanced routing.
- Scales automatically.
- IP Address ***isn't*** static.
- Multi-AZ
- Doesn't allow for stickiness.
