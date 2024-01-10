---
marp: true
theme: uncover
class: invert
---

# O que são *ELB*s?
Elastic Load Balancer

---

# Elastic Load Balancer

É um serviço fornecido pela AWS, projetado para distribuir o tráfego de aplicativos entre várias instâncias ou servidores.

---

# Tipos de ELB

- [Application Load Balancer](#application-load-balancer)

- [Network Load Balancer](#network-load-balancer)

- [Gateway Load Balancer](#gateway-load-balancer)

- [Classic Load Balancer](#classic-load-balancer)

---

# Application Load Balancer

* Recomendado para protocolos HTTP e HTTPS

* Permite roteamento avançado

* Escalabidade automatica

* Endereço IP não-estático

* Multi-AZ

* Permite [stickiness](#stickiness)

---

![bg left height:450px](https://www.imperva.com/learn/wp-content/uploads/sites/13/2019/01/session-stickiness-diagram.jpg)

## Stickiness

* Opção que anexa a sessão de um usuário a uma isntância específica.

---

## Algoritmo de roteamento ALB
#### Algoritmo baseado em:


- [Round Robin]()

- Requisições baseadas em Header HTTP

- Requisições baseadas em paths

- Requisições baseadas em origem

- Requisições baseadas em destino

---

# Network Load Balancer

* Recomendado para protocolos TCP e UDP

* Capaz de lidar com milhões de requisições por segundos

* Escalabilidade automática

* Permite 1 único endereço IP estático

* Sem terminações SSL*

---

## Algoritmo de roteamento NLB

Faz uso do algoritmo [flow hash](https://www.linkedin.com/pulse/hash-flow-algorithm-aws-network-load-balancer-nlb-in-depth-mishra) baseado em:

- Protocolo

- IP e porta de origem

- IP e pora de destino

- Número de sequência TCP.

---

# Gateway Load Balancer

Permite executar, gerenciar e escalar ***appliances virtuais*** como Firewalls, IDS/IPS* entre outros

---

# Gateway Load Balancer

* Recomendado para protocolos IP

* Usa protocolo ***GENEVE*** de encapsulamento

* Multi-AZ

* Permite [stickiness](#stickiness)

* Permite relatórios *Health Check*

---

# Classic Load Balancer

Esse foi o primeiro Load Balancer da AWS, considerado ***legacy*** nos dias atuais.

<br>

- Legacy para HTTP e HTTPS
- Não permite roteamento avançado
- Escalamento automático
- Endereço IP não estático
- Multi-AZ
- Não permite stickiness