# Routing Policies

### Simple routing policy

Used for a single resource that performs a given function, for example a simple webserver that servers content

### Weighted routing policy

Used to route traffic to multiple resources in different proportions — 90% to an instance, 10% to other — that you especify.

### Latency routing policy

Used when you have resources in multiple AWS Regions, used when you want to provide the best latency.

### Failover routing policy

Used when you want to ***configure active-passive failover mechanisms***.

### Geolocation routing policy

Used when you want to route traffic ***based on user location***.

### Geoproximity routing policy

Used when you want to ***route traffic based on resource location***, with intent to shift traffic from one location to other.

### Multivalue answer routing policy

Used when you want Route 53 to respond to DNS queries with up to eight healthy records selected at random.
