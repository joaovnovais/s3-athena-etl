# 🟩 Projeto – ETL de Histórico de Vendas para Data Lake

Este projeto demonstra um pipeline de **ETL tradicional** (lote) usando Python e serviços da AWS. Ele simula um cenário real onde uma empresa precisa processar diariamente seu histórico de vendas e armazenar os dados em um **Data Lake (Amazon S3)**, permitindo análise posterior com **Amazon Athena**.

---

## 🎯 Objetivo

Extrair dados históricos de vendas de um arquivo CSV, realizar transformações simples com Python (pandas) e armazenar os dados no formato Parquet em um bucket Amazon S3, permitindo consultas eficientes com o Amazon Athena.

---

## 🧰 Tecnologias e Ferramentas

- 🐍 **Python** (`pandas`, `boto3`, `awswrangler`)
- ☁️ **Amazon S3**
- 📊 **Amazon Athena**
- 📓 **Google Colab** (ambiente de desenvolvimento)
- 🔐 **AWS IAM** (configuração de credenciais)

---

## ⚙️ Pipeline ETL

1. **Extração:**
   - Dataset em CSV obtido do Kaggle.
   - Dataset: [EUA Compras Online](https://www.kaggle.com/datasets/zahidmughal2343/usa-online-shopping)

2. **Transformação:**
   - Renomeação e padronização de colunas.
   - Conversão de tipos de dados.
   - Limpeza básica.

3. **Carga:**
   - Salvamento dos dados transformados no formato `.parquet`.
   - Upload para o bucket Amazon S3:  
     `s3://data-engineer-projects-jota/projeto1/historico_compras.parquet`

---

## 🔍 Consultas com Amazon Athena

- Criada tabela no Athena com base nos dados armazenados no S3.
- Consultas SQL realizadas diretamente via `awswrangler` no Google Colab.

---

## 📊 Resultado Esperado

- ✔ Arquivo `.parquet` salvo no S3 com os dados transformados.
- ✔ Tabela disponível no Athena para análise com SQL.
- ✔ Pipeline replicável e escalável para futuras entradas de dados.

---

## 📚 Aprendizados

- ✅ Conexão segura com AWS usando `boto3` e `awswrangler`
- ✅ Boas práticas de transformação com `pandas`
- ✅ Armazenamento eficiente em Data Lake com Amazon S3
- ✅ Análise de dados usando SQL com Amazon Athena

---

