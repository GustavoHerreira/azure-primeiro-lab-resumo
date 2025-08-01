# Resumo do Lab: Conceitos de Nuvem e Deploy Prático

Este repositório contém o resumo dos conceitos de computação em nuvem aprendidos na etapa de Cloud do Bootcamp e demonstra a **aplicação prática** desses conhecimentos através do deploy de uma API na AWS.

## ☁️ 1. Conceitos Teóricos Aprendidos

Durante o lab, foram apresentados os "pilares da computação em nuvem", essenciais para entender como os serviços de provedores (como Microsoft Azure e AWS) funcionam.

### - **Modelos Financeiros (CapEx vs. OpEx):**
A computação em nuvem atualiza o modelo financeiro de TI ao trocar o CapEx pelo OpEx:
- CapEx (Despesa de Capital): É o modelo tradicional de comprar equipamentos caros, como servidores e data centers, exigindo um grande investimento inicial.
- OpEx (Despesa Operacional): É o modelo da nuvem, que funciona como uma assinatura. Não há compra de equipamentos, apenas um custo recorrente baseado no uso.

Isso é possível graças ao modelo baseado em consumo, que significa que a cobrança é feita apenas sobre os recursos que de fato utilizamos, garantindo melhor previsão de custos e evitando desperdícios.


## 🚀 2. Estudo de Caso: Deploy de uma API na AWS

Para apresentar na prática o que foi ensinado, compararei o deploy de um projeto pessoal (uma API .NET) em um ambiente de nuvem real (projeto esse feito no módulo anterior nesse mesmo Bootcamp - "Desafio de projeto - Trabalhando com ASP.NET Minimals APIs"), utilizando a **Amazon Web Services (AWS)**.

A tabela abaixo conecta os conceitos teóricos com as ações práticas que executei:

| Conceito Teórico (Azure/Geral) | Minha Aplicação Prática (AWS) |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **IaaS (Infraestrutura como Serviço)** | Utilizei o serviço **Amazon EC2** para criar uma máquina virtual (servidor Linux). Este serviço é o equivalente direto das **Máquinas Virtuais do Azure**. |
| **Rede e Segurança** | Configurei um **Security Group** na AWS para atuar como um firewall virtual, liberando as portas `HTTP (80)` e `SSH (22)`. O serviço mais parecido equivalente na Azure que encontrei seria **Grupos de Segurança de Rede (NSG)** do Azure. |
| **Contêineres e Orquestração** | Instalei o **Docker** e o **Docker Compose** na instância EC2 para rodar tanto a API quanto o banco de dados PostgreSQL de forma isolada e consistente, exatamente como no meu ambiente de desenvolvimento. |
| **Modelo de Custo (OpEx)** | Todo o projeto foi implementado utilizando o **Nível Gratuito da AWS (Free Tier)**, o que reforça na prática o **modelo de OpEx**, permitindo iniciar um projeto com custo ZERO. |

## 🔗 3. Projeto no Ar!

A API está em execução na nuvem e pode ser acessada publicamente através da documentação interativa do Swagger.

> **Clique no link abaixo para testar a API ao vivo:**
> 
> ### **[http://18.117.216.57/swagger/index.html](http://18.117.216.57/swagger/index.html)**

Código fonte do projeto disponível em: https://github.com/GustavoHerreira/car-rental-api

*(Observação: A aplicação roda em uma instância `t2.micro` do nível gratuito. A primeira requisição pode levar alguns segundos para ser respondida.)*
