---
marp: true
theme: uncover
class: invert
---

# S3
Simple Storage Service

---

## O que é?
S3 é um **sistema de armazenamento global** na internet, projetado para trabalhar em alta escala por um interface web simples.

---

## Como funciona?
É usado para guardar ou recuperar qualquer quantidade de dados, a qualquer momento 
em qualquer lugar da internet.

---

## Algumas vantagens do S3
* Criação de buckets

* Armazenamento de dados

* Download de dados

* Gerenciamneto de permissões

---

# Conceitos básicos
Buckets, objetos, chaves e regiões

---

# Buckets

São containers para [***objetos***](#objetos) armazenados no S3, onde cada objeto está em um bucket específico.

<br>

Cada bucket deve ter um ***nome global único***

<br>

Mesmo que um bucket seja um recurso global, um *bucket é um recurso regional*

---

# Buckets

O tamanho máximo de um bucket é de **5TB**.

<br>

Exemplo de bucket no CLI
```bash
s3://my-bucket-s3 
```

Exemplo de bucket no browser
```bash
https://my-bucket-s3.s3.amazon.com/
```

---

# Objetos

* Objetos são entidades fundamentais de dados no S3

* Objetos são compostos por metadados

* A identificação de um objeto é dada por ***um bucket, uma chave e uma chave de versão***

---

# Objetos

Objetos maiores do que 5GB devem ser salvos usando **Multi-part Upload**, mas a Amazon recomenda que objetos a partir de **100MB** devam usa-lo

<br>

* O objeto é endereçado pela combinação de:
    - Um web service endpoint
    - O nome do bucket
    - Uma chave

---

# Chaves

Uma chave é um identificador único de um bucket, cada bucket tem ***apenas uma chave***. Cada chave é composta por um **prefixo**, uma parte default da amazon AWS e um **nome de objeto**

<br>

https://**docs**.s3.amazonaws.com/2024-01-01/**file.txt**

---

# Regiões
<br>

- Podemos escolher a região de criação do bucket.
<br>

- Essa decisão pode ser baseada na latência, corte de custos ou para atender requerimentos regulatórios.
<br>

- Um objeto de uma região **NUNCA** sai dela.