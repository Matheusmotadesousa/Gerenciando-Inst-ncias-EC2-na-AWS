
---

### 3. docs/passo-a-passo.md (Passo a Passo)

```markdown
# Passo a Passo: Criando sua Primeira Instância EC2

## 🎯 Objetivo

Criar, configurar e acessar uma instância EC2 com Linux, demonstrando todo o processo de gerenciamento.

---

## 📋 Pré-requisitos

- [ ] Conta AWS ativa
- [ ] AWS CLI instalada e configurada
- [ ] Par de chaves (.pem) criado
- [ ] Conhecimento básico de terminal

---

## 🚀 Passo 1: Acessar o Console AWS

1. Faça login no [AWS Management Console](https://console.aws.amazon.com/)
2. No painel, selecione **EC2**
3. Certifique-se de estar na região **us-east-1** (N. Virginia)

![Console AWS](./imagens/console-aws.png)

---

## 🚀 Passo 2: Criar uma Instância

### Pelo Console

1. Clique em **Launch Instance**
2. Configure:
   - **Nome**: `minha-primeira-instancia`
   - **AMI**: Amazon Linux 2023 AMI
   - **Tipo**: `t2.micro` (free tier)
   - **Key Pair**: Selecione seu par de chaves
   - **Security Group**: Permita SSH (porta 22)
3. Clique em **Launch Instance**

### Pela CLI

```bash
aws ec2 run-instances \
    --image-id ami-0c02fb55956c7d316 \
    --instance-type t2.micro \
    --key-name minha-chave \
    --security-group-ids sg-12345678 \
    --tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=minha-primeira-instancia}]'
