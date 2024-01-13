---
marp: true
theme: uncover
class: invert
---

# Auto Scaling
Solução para escalonamento automático

---

![width:900px](https://storage.googleapis.com/algodailyrandomassets/curriculum/systems-design/aws/asg/IMG_1.png)

---

## Como funciona o Auto Scaling?

O Auto Scaling se baseia no principio de [***escalonamento horizontal***](#escalonamento-horizontal)

---

## Escalonamento Horizontal

Se trata do processo de adicionar mais instâncias a um sistema, distribuindo o workload entre eles.

* ##### Adicionar mais instâncias AWS

* ##### Ideal para lidar com aumento de tráfego e workload de maneira distribuida

---

## Escalonamento Vertical

Se trata do processo de adicionar mais recursos para uma instância, para lidar com workloads mais pesados

* ***Adicionar uma CPU melhor a um servidor***

* ***Adicionar mais memórias RAMs em um servidor***

* ***Adicionar mais armazenamento para um servidor***

---

## Como o Auto Scaling funciona?

O Auto Scaling é uma ferramenta que monitora suas aplicações e ajusta sua capacidade ***[horizontalmente](#escalonamento-horizontal)*** mantendo uma performance previsivel e constante, com a menor quantidade de cobranças possíveis.

---

# Scheduled Action

É uma maneira de agendar o lançamento de instâncias por um preve período de tempo (dias).

- Quantidade mínima de instâncias

- Quantidade máxima de instâncias

- Recorrência dessa ação