# Auto Scalling 

### Vertical Scalability
- Adding capacity to a single resource to handle higher workloads
    - Adding better CPU to an existing server
    - Adding more RAM to a server
    - Adding more SSD storage capacity to a server
- Use case: Suitable when the application's performance can be improved by enhancing the capabilities of a single machine.

### Horizontal Scalability 
- Adding more capacity by adding more instances or machines to a system, distributing the workload across them
    - Adding more AWS instances to distribute traffic
    - Scaling out by deploying additional servers in a data center
- Use Case: Ideal for handling increased traffic and workload by distributing it across multiple nodes.

## What is *AWS Auto Scaling*?

It's a tool that monitors your applications/instances and adjusts it's capacity (Horizontally) automatically to keep a constant and predictable perfomance with the least amount of expenses possible.

![AWS Auto Scaling Group Diagram](https://storage.googleapis.com/algodailyrandomassets/curriculum/systems-design/aws/asg/IMG_1.png)

### Important points!
- Which AZ the Auto Scaling group should include
- Which existing resources can be used, like security groups, AMIs, etc
- If you want to raise or lower you capacity, or if you want only to guarantee a specific number of servers in execution. It can do both at the same time!
- Which metrics are more relevant for your application performance
- You need to be conscious about the time it takes to iniciate and configure a new server instance