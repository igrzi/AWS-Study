# AWS Target Groups Overview

## What is an AWS Target Group?
An AWS Target Group is a logical grouping of targets, such as Amazon EC2 instances, that receive traffic from a load balancer. Target Groups allow you to route requests to specific sets of instances based on rules defined in the associated listener. They play a crucial role in distributing incoming traffic and ensuring the scalability and availability of your applications.

## Key Concepts

### 1. Targets:
Targets are resources (e.g., EC2 instances, containers) registered with a target group. The load balancer routes traffic to these targets based on the configured rules.

### 2. Health Checks:
Each target within a target group undergoes periodic health checks. If a target is unhealthy, the load balancer automatically diverts traffic away from it until it passes the health check.

### 3. Listener Rules:
Listener rules are conditions specified in the load balancer's listener settings. These rules determine how traffic is distributed to different target groups based on factors like path patterns or hostnames.

## Types of Target Groups

### 1. Instance Target Group:
Targets are specified by instance IDs, and the load balancer routes traffic to individual instances.

### 2. IP Target Group:
Targets are specified by IP addresses, enabling you to route traffic to specific IP addresses rather than instances.

### 3. Lambda Target Group:
Designed for serverless applications, Lambda target groups route traffic to AWS Lambda functions.

## How to Create a Target Group
1. Sign in to the AWS Management Console.

2. Navigate to the EC2 dashboard and choose "Target Groups" from the sidebar.

3. Click "Create Target Group" and configure the basic settings such as name, protocol, and port.

4. Specify the targets for the group (e.g., instances or IP addresses).

5. Configure health checks to ensure the targets are healthy.

6. Review your settings and click "Create" to complete the process.