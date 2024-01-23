# Route 53 Health Checks

Health Checks on Route 53 monitor the ***integrity and performance of our web apps***, web servers and other resources.

## Health Check Types
- Health Checks that monitor an ***endpoint***, like an instance, a load balancer, a S3 buckets, etc.

- Health Checks that monitor ***other health checks*** this makes a [**Calculated Health Check**](https://aws.amazon.com/blogs/aws/route-53-improvements-calculated-health-checks-and-latency-checks/).

- Health Checks that monitor ***CloudWatch Alarms***.

---

You need 3 OK status health checks to be ***approved*** and 3 failed to ***fail***, the default option for health checks is ***one every 30 seconds***, but, if you want you can use ***one every 10 seconds*** but you *will be charged more*.

Health Checks can be done through HTTP/HTTPS protocols or by TCP protocols.