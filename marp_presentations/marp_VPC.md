---
marp: true
theme: uncover
class: invert
---

# AWS Session Manager

---

## O que é?

É uma maneira de acessar suas instâncias sem a necessidade do uso de protocolo SSH

---

## Quais suas vantagens?

* Acesso seguro através de roles do AWS IAM

* Comunicação encriptada através de SSL

* Auditabilidade com logs no AWS CloudWatch

* Não necessidade de abertura de portas inbound

* Não necesidade de um **bastion host**

---

## O que é necessário?

É necessário o AWS Session Manager Agent instalado e configurado em sua instância, permitindo acesso pelo AWS CLI ou o AWS Management Console.

---

# VPC Peering

![VPC Peering Diagram](https://disaster-recovery.workshop.aws/images/vpc-peering-diagram.png)

---

## O que é?

É uma conexão de rede entre duas ou mais VPCs, no qual é permitido o tráfego de dados entre elas usando endereços IPv4 e IPv6 privados!

---


## Pontos importantes

* Permite conexão direta e privada

* [*Peering transitivo*](#o-que-significa-peering-transitivo)

* Permite o uso de SGs e Network ACLs para uma configuração mais segura

* Não permite blocos CIDR sobrepostos

* Possível apenas entre uma mesma região

* É necessária a configuração da tabela de roteamento para comunicação entre as VPCs

---

### O que significa *Peering Transitivo*

Como um exemplo, uma *VPC A* se conecta a uma *VPC B* e essa *VPC B* é conectada a uma *VPC C*.

A *VPC A* poderá se comunicar com a *VPC C* através da relaçaõ transitiva estabelecidade pelo Peering*

---

# Network ACL

---

## O que é?

É uma ***lista de controle de acesso (ACL)***, é uma camada de segurança adicional e opcional para uma VPC, age como um ***Firewall Stateless*** controlando o tráfego de entrada e saída de uma ou mais subnets.

---

## Firewall Stateles

É um tipo de firewall que toma decisões de segurança baseado apenas em informações básicas, como endereço IP, portas e protocolos

<br>

* Não mantém registros

* Não considera o "contexto" de conexões anteriores

