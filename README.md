# CODE-GIRLS-DIO-5
5° DESAFIO DO BOOTCAMP CODE GIRLS DIO:

AUTOMATIZAÇÃO DE TAREFAS COM AWS LAMBDA E S3

## Objetivo
Prática com automatização com Lambda e S3

## Tecnologias Utilizadas
- **AWS Lambda** – Funções serverless para execução automática de código
- **Amazon S3** – Armazenamento de objetos (arquivos)
- **AWS CloudFormation** – Provisionamento automático da infraestrutura como código
- **IAM (Identity and Access Management)** – Controle de permissões para execução segura
- **Python** – Linguagem utilizada na função Lambda

## Como foi feito
1. Criar Bucket no S3
- Criei um bucket chamado "meu-bucket-processamento-dio"
- Configurei permissões públicas/desabilitadas (segurança)
- Habilitei notificações de eventos (upload de arquivo)

2. Criar Função Lambda
- Nome: "processarArquivoS3"
- Linguagem: Python 3.9
- Código: Função que é acionada quando um novo arquivo é enviado ao S3
- Permissões: Role com acesso de leitura ao S3 e logs no CloudWatch

3. Conectar Lambda ao Evento do S3
- Configurei o gatilho para executar a Lambda automaticamente ao receber arquivos `.csv`

4. Teste e Validação
- Fiz upload de arquivos no bucket
- Verifiquei logs no CloudWatch
- A função processou os arquivos corretamente

  ## O que eu aprendi
- Como conectar eventos do S3 com funções Lambda
- Importância de configurar permissões IAM corretamente
- Utilização do CloudFormation para automatizar a criação da infraestrutura
