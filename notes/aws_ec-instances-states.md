# Instance Lifecycle

Amazon EC2 instance trasitions through different states, from the moment you launch through its termination.

The illustration below shows the different stages, notice you can't stop and start an instance store-backed.

![Instance lifecycle](https://docs.aws.amazon.com/images/AWSEC2/latest/UserGuide/images/instance_lifecycle.png)

# Instance States

| State          |        Description                       |     Instance Billing    | 
|----------------|------------------------------------------|-------------------------|
| Pending        | Preparing to enter *running* state       |     ***Not Billed***    |
| Running        | Running and ready to use                 |       ***Billed***      |
| Stopping       | Instance is preparing to be stopped      |     ***Not Billed***    |
| Stopped        | Shuting down, can restart any time       |     ***Not Billed***    |
| Shuting-Down   | Instance is preparing to be terminated   |     ***Not Billed***    |
| Terminated     | Instance being permanently deleted       |     ***Not Billed***    |
