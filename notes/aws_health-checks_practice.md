# Health Checks checking

Basic *Apache* Web Server checking.

## Commands
We go to the directory our SSH key is located, execute a SSH into the instance:

```bash
cd Downloads/  
ssh -i MySSHkey.pem ec2-user@instance_public_ip  
sudo -i
```
After that we can run a simple check on our Apache server and see if our HTTPD is running:

```bash
systemctl status httpd
```

If our HTTPD server is running correctly we can check some logs:

``` bash
cd /var/log/httpd/  
tail -f access_log
```
If we check in our AWS Console, we can see that all Health Checks have passed correctly.

Now, we can force our Apache server to stop and check our ***access_log*** file one more time:  

```bash
systemctl stop httpd  
tail -f access_log
```

After some time, we check our AWS Console and see that our health checks have failed!

Then we can restart our HTTPD server with:
```bash
systemctl start httpd
```

## Conclusion

If we have 2 of our apache servers instances running, both on the same ***target group*** and in a ***load balancer***, when one instance failes it's health check, all the traffic goes to the other instance.