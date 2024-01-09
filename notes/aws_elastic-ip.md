# [Elastic IP](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html)

When you restart an instance, sometimes your public IPv4/IPv6 will change, but if you need a fixed **Public IP Address** you can use the ***Elastic IP*** tool, you just need to allocate a IP address from the AWS IP pool.

When you *allocate and associate* an IP Adress you **aren't charged** for it. But if you *allocate and don't associate* it with any instance you **will be charged** for it.

After allocating an Elastic IP Address you should:  
Select the public IPv4 address > Actions > Associate Elastic IP address > Choose an instance.