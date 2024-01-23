---
marp: true
theme: uncover
class: invert
---

# Route 53
![height:275px](https://d2908q01vomqb2.cloudfront.net/da4b9237bacccdf19c0760cab7aec4a8359010b0/2020/08/12/Screen-Shot-2020-08-12-at-9.51.17-AM.png)

---

## O que é?

É um serviço de DNS web que disponibiliza algumas funcionalidades, como ***registro de dominio, gerenciamento de rotas DNS e verificação de integridade (Health Checks)***

---

## Outras Funcionalidades
* Load Balancing

* Roteamento de Tráfego

* Monitoramento e Logs

---

# DNS

Domain Name System

---

# Qual sua função?<br>

O *DNS* tem a função de converter um nome de domínio legível, como **www.ovver.com.br**, em um endereço IP!

---

## Procuras DNS

* #### Direct Lookup
    - Converte um hostname para um endereço IP

<br>

* #### Reverse Lookup
    - Converte um endereço IP em um hostname

--- 

## Tipos de registros DNS

---

### SOA (Start Of Authority)
Primeiro registro em uma zona DNS, possui informação sobre o domínio, como servidor primário e secundário, TTL, arquivos de zona e outros.

<br>

### MX (Maix eXchange)
Define os servidores de email e suas prioridades.

---

### NS (Name Server)
Define qual servidor DNS tem permissão para responder ao lookup.

<br>

### CNAME (Alias - Canonical Name)
Define um pseudônimo para vários hostnames do mesmo domínio.

---

### A (Host)
Mapeia os hostnames a um endereço IP

<br>

### PTR (Pointer - Reverse)
Função reversa do tipo A, mapeia o IP a um hostname

--- 

# CNAME x ALIAS

- Ambos permitem a criação de pseudônimos

- Registros do tipo Alias do Route 53, permite o roteamento do tráfego para recursos AWS.

- Alias são gratuítos. CNAME são pagos

- Alias possuem Health Checks nativos.