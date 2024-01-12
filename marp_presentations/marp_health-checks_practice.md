---
marp: true
theme: uncover
class: invert
---

# Prática Health Checks
Uma checagem básica de um Web Server Apache

---

```bash
ssh -i MySSHkey.pem ec2-user@instance_public_ip  
sudo -i
```

Com isso conectamos na nossa instância

<br>

```bash
systemctl status httpd
```

E checamos o status de nosso server Apache

---

## Checando logs

``` bash
cd /var/log/httpd/  
tail -f access_log
```

---

#### Podemos ver que ambas as nossas instâncias estão passando nos health checks

![width:1000px](../marp_statics/health_checks.jpg)

---

## Forçando a parada

Podemos forçar a parada de nossa instância para averiguar nossos Health Checks falhando

```bash
systemctl stop httpd  
tail -f access_log
```

--- 

#### Podemos ver que uma de nossas instâncias não está passando nos Health Checks

![width:1000px](../marp_statics/failed-health_checks.png)