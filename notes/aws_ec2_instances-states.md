# Instance Lifecycle

Amazon EC2 instance trasitions through different states, from the moment you launch through its termination.

The illustration below shows the different stages, notice you can't stop and start an instance store-backed.

![Instance lifecycle](https://docs.aws.amazon.com/images/AWSEC2/latest/UserGuide/images/instance_lifecycle.png)

# Instance States

| State          |        Description                       |     Instance Billing    | 
|----------------|------------------------------------------|:-----------------------:|
| Pending        | Preparing to enter *running* state       |     ***Not Billed***    |
| Running        | Running and ready to use                 |       ***Billed***      |
| Stopping       | Instance is preparing to be stopped      |     ***Not Billed***    |
| Stopped        | Shuting down, can restart any time       |     ***Not Billed***    |
| Shuting-Down   | Instance is preparing to be terminated   |     ***Not Billed***    |
| Terminated     | Instance being permanently deleted       |     ***Not Billed***    |

# Stop protection

This feature, implemented in May of 2022, blocks attemps to stop EC2 Instances via the console, API or CLI. This, paired with a notification can provide another layer of security to running production instances.

> - You **can't** enable *Stop Protection* for Spot Instances.
> - *Stop Protection* prevents accidental stops and accidental terminations when using console.
> - This doesn't stop AWS from stopping when there's a [*scheduled event.*](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/monitoring-instances-status-check_sched.html)

For the AWS news post, click [here.](https://aws.amazon.com/about-aws/whats-new/2022/05/amazon-ec2-enables-protect-instances-unintentional-stop-actions/s)