 Guia Prático: Gerenciamento de Instâncias EC2 na AWS

![AWS](https://img.shields.io/badge/AWS-EC2-orange?style=flat&logo=amazon-aws)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-concluído-brightgreen)

 Sobre o Projeto

Este repositório documenta meu aprendizado e prática no gerenciamento de instâncias EC2 na AWS, como parte do desafio da DIO. O conteúdo aborda desde conceitos básicos até estratégias avançadas de otimização de custos e escalabilidade.

 Objetivos de Aprendizagem

- ✅ Aplicar conceitos do EC2 em ambiente prático
- ✅ Documentar processos técnicos de forma estruturada
- ✅ Utilizar GitHub como ferramenta de documentação


 Começo Rápido

 Pré-requisitos

- Conta AWS ativa
- AWS CLI configurada
- Conhecimento básico de terminal

 Comandos Básicos

```bash
 Listar instâncias
aws ec2 describe-instances

 Criar uma instância (Linux)
aws ec2 run-instances \
    --image-id ami-0c02fb55956c7d316 \
    --instance-type t2.micro \
    --key-name sua-chave \
    --security-group-ids sg-xxxxx

 Parar uma instância
aws ec2 stop-instances --instance-ids i-xxxxxxxx

 Iniciar uma instância
aws ec2 start-instances --instance-ids i-xxxxxxxx
