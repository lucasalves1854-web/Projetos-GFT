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

```text
Cliente
   │
   ▼
S3 Object Lambda
   │
   ▼
AWS Lambda
   │
   ▼
Supporting Access Point
   │
   ▼
Amazon S3
```

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