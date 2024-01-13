# Elastic Load Balancer

***Elastic Load Balancing*** is a service that automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses.

## What are some benefits of ELB?

- ***Enhancing availability and fault tolerance***

- ***Ensures efficient load distribution***

- ***Dynamical application scalability***

- ***Maintains a consistent user experience***

## What it can do?

- It allows to propagate requests across multiple targets.

- It exposes only one DNS acess point, also know as FQDN or ***Fully Qualified Domain Name***.

- Any ELB has a static DNS hostname.

- Allows for tests called [*Health Checks*](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-healthchecks.html) on its targets, this is a check to guarantee instance integrity.

- Makes SSL (HTTPS) available for your applications, making for more secure communications.

- Allows for *public* and *private* ELB.

- The ELB gets "bigger" automatically, but, it isn't instantly.

## What it returns

The ELB works with 3 main types of *HTTP return codes*.

- 200 for successful requisitions.

- 4xx for ***client side error*** requisitions.
    - 400: Bad Request
    - 401: Unauthorized.
    - 403: Forbidden.
    - 404: Not found.

- 5xx for ***server side error*** requisitions.
    - 500: Internal Server Error.
    - 502: Bad Gateway.
    - 503: Service Unavailable.
    - 504: Gateway timeout.

## Creating a Load Balancer Through AWS CLI

### Creating a Elastic Load Balancer

```bash
aws elbv2 create-load-balancer --name "..." --subnets "..." "..." --security-groups "..."
```

### Creating a Target Group

```bash
aws elbv2 create-target-group --name "..." --protocol "..." --port "..." --vpc-id "..."
```

### Creating a Target (Instances) on Target Groups

```bash
aws elbv2 register-targets --target-group-arn "..." --targets Id="..." Id="..."
```

### Creating a Listener and associating to a Target Group ELB

```bash
aws elbv2 create-listener --load-balancer-arn "..." --protocol "..." --port "..."  --default-actions Type="...",TargetGroupArn="..."
```