# Containers and Virtualization

## 🎯 Objetivo

Executar em cluster Kubernetes microserviços em alta disponibilidade. 

## Microserviços 

1. [Cotacao-crypto-api](https://github.com/AlexDamiao86/trabalho-microservices/tree/main/cotacao-crypto-api) - Microserviço desenvolvido em Node.js com persistência em MySQL. Obtem cotações de criptomoedas por WebSocket API da BitPreço. Disponibiliza CRUD de criptomoedas através de API Rest. É possível interagir pela aplicação através do Swagger pelo endereço "{ip-maquina}:32555/docs".

## ⚙️ Executando

A partir de cluster Kubernetes com 1 master e 3 workers em execução: 

```bash
git clone https://github.com/AlexDamiao86/containers-kubernetes

cd containers-kubernetes/cotacao-crypto-api 

kubectl create -f manifest.yaml
```
