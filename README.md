# Containers and Virtualization

## 🎯 Objetivo

Executar em cluster Kubernetes microserviços em alta disponibilidade. 

## Microserviços / Frontend

1. [Cotacao-crypto-api](https://github.com/AlexDamiao86/trabalho-microservices/tree/main/cotacao-crypto-api) - Microserviço desenvolvido em Node.js com persistência em MySQL. Obtem cotações de criptomoedas por WebSocket API da BitPreço. Disponibiliza CRUD de criptomoedas através de API Rest. É possível interagir com a aplicação através de Swagger pelo endereço "{ip-maquina}:32555/docs".

> **_NOTA:_** Imagem DockerHub: alexdamiao86/cotacao-crypto-api:1.1.0

2. [Carteira-crypto-api](https://github.com/FabioQuimico/carteira-crypto-quarkus) - Microserviço desenvolvido em Quarkus com persistência Postgres. Relaciona as criptomoedas dos clientes. Disponibiliza API Rest para realizar operações CRUD clientes e de operações de compra e venda de criptomoedas. É possível interagir com a aplicação através de Swagger pelo endereço "{ip-maquina}:32080/q/swagger-ui/". 

> **_NOTA:_** Imagem DockerHub: alexdamiao86/carteira-crypto-api:1.0.6

3. [Crypto-app](https://github.com/gabriel2503/Microservices) - Frontend desenvolvido em Angular que consume os dois microserviços anteriores para exibir lista de criptomoedas disponíveis para compra e venda. Registra compra, venda e lista criptomoedas de um cliente. 

> **_NOTA:_** Imagem DockerHub: gabrielobarbosa/crypto:v2

## Topologia



## ⚙️ Executando

A partir de cluster Kubernetes com 1 master e 3 workers em execução. No node master, executar:

1. Componentes do Cotação Crypto:

```bash
git clone https://github.com/AlexDamiao86/containers-kubernetes
```
```bash
cd containers-kubernetes/cotacao-crypto-api 
```
```bash
kubectl create -f manifest.yaml
```

2. Componentes da Carteira Crypto: 

```bash
cd ../carteira-crypto-api
```
```bash
kubectl create -f manifest.yaml
```

