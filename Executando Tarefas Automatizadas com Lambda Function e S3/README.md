# Executando Tarefas Automatizadas com Lambda Function e S3

##  Descrição

Projeto desenvolvido durante o laboratório da DIO com o objetivo de compreender a automação de tarefas utilizando AWS Lambda, Amazon S3 e AWS CloudFormation.

O laboratório demonstra como automatizar a configuração do Amazon S3 Object Lambda utilizando um template do CloudFormation, permitindo criar toda a infraestrutura de forma padronizada.

---

## Objetivos

- Entender o conceito de Serverless.
- Criar recursos automaticamente utilizando CloudFormation.
- Integrar Amazon S3 com AWS Lambda.
- Automatizar o processamento de objetos utilizando S3 Object Lambda.
- Compreender boas práticas de Infraestrutura como Código (IaC).

---

## Serviços AWS Utilizados

- AWS Lambda
- Amazon S3
- Amazon S3 Object Lambda
- AWS CloudFormation
- Amazon CloudWatch
- AWS IAM

---

## Fluxo da Arquitetura

![alt text](image.png)

## Arquitetura Serverless para Processamento de Notas Fiscais

## Objetivo

Este projeto demonstra uma arquitetura serverless na AWS para processar automaticamente arquivos JSON contendo informações de notas fiscais. Após o upload no Amazon S3, uma função AWS Lambda realiza a validação dos dados e os armazena no Amazon DynamoDB. A consulta das informações é realizada por meio do Amazon API Gateway.

## Fluxo da Arquitetura
O usuário envia um arquivo JSON para um bucket Amazon S3.
O evento de upload dispara uma função AWS Lambda.
A Lambda valida o conteúdo do arquivo.
Os dados válidos são gravados no Amazon DynamoDB.
O cliente consulta as informações através do Amazon API Gateway, que aciona uma segunda Lambda para buscar os dados no banco.

## Validações

## Durante o processamento são realizadas as seguintes validações:

Arquivo no formato JSON;
Campos obrigatórios preenchidos;
Estrutura do documento válida;
Dados aptos para gravação no DynamoDB.

Caso alguma validação falhe, o processamento é interrompido e o erro é registrado no CloudWatch.

## Considerações

A arquitetura utiliza uma abordagem orientada a eventos, permitindo processamento automático, escalabilidade e baixo custo operacional por utilizar serviços serverless da AWS.

---

## Principais Conceitos

### AWS Lambda

Permite executar código sem gerenciar servidores.

### Amazon S3

Serviço de armazenamento de objetos altamente escalável.

### S3 Object Lambda

Permite transformar objetos antes de entregá-los ao cliente.

### AWS CloudFormation

Automatiza o provisionamento da infraestrutura utilizando templates YAML ou JSON.

---

## Aprendizados

Durante este laboratório compreendi como o AWS CloudFormation pode automatizar toda a configuração do S3 Object Lambda, reduzindo erros manuais e garantindo padronização da infraestrutura.

Também aprendi que o AWS Lambda pode modificar objetos dinamicamente antes que eles sejam entregues ao usuário, sem alterar o arquivo original armazenado no bucket.

Outro ponto importante foi compreender a integração entre Amazon S3, Lambda, IAM e CloudWatch em uma arquitetura serverless.

---

## Estrutura do Projeto

```text
.
├── README.md
├── docs
├── images
├── lambda
└── template.yaml
```

---

## Evidências

Adicionar nesta pasta:

- Criação da função Lambda
- Bucket S3
- Trigger
- CloudFormation
- CloudWatch

---

## Referências

- AWS CloudFormation
- AWS Lambda
- Amazon S3 Object Lambda
- Documentação Oficial da AWS

---

## Autor

Lucas Alves

AWS Certified Cloud Practitioner