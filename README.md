# 🛰️ Bayer GTM Intelligence AI: Data-to-Agent Platform

![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)
![GenAI](https://img.shields.io/badge/Gemini_1.5_Pro-8E75B2?style=for-the-badge&logo=google-gemini&logoColor=white)
![FinOps](https://img.shields.io/badge/Cloud_Workflows-FF9900?style=for-the-badge&logo=google-cloud&logoColor=white)

## 📖 Visão Geral
Este projeto demonstra a criação de um ecossistema completo de dados e IA para o setor de Go-To-Market (GTM) da Bayer. Através da arquitetura **Medallion**, transformamos dados transacionais brutos em uma base de conhecimento (RAG) para um assistente de IA generativa (Gemini).

---

## 🏗️ Arquitetura do Sistema
A solução foi desenhada para ser escalável e 100% serverless, minimizando custos operacionais.

<img width="1408" height="768" alt="Gemini_Generated_Image_gtb32fgtb32fgtb3" src="https://github.com/user-attachments/assets/58cff18b-09bb-42f8-aa04-430c14607b50" />

### Fluxo de Dados:
1. **Ingestão (Bronze):** Captura de 500k registros JSON via Spark.
2. **Refino (Silver):** Tratamento de esquemas e limpeza.
3. **Consumo (Gold):** Tabelas agregadas por `regiao`, `fornecedor` e `categoria`.
4. **Busca Vetorial:** Indexação no Vertex AI Search.
5. **LLM Interface:** Gemini Enterprise respondendo com Grounding na Gold.

---

## ⚙️ Orquestração & FinOps
Em vez de utilizar clusters fixos (Airflow), optei pelo **Cloud Workflows**, reduzindo o custo fixo para **zero** durante a ociosidade.

<img width="318" height="724" alt="workflow1" src="https://github.com/user-attachments/assets/4bf21c69-2935-4f37-ad16-ff5af873acf9" />
<img width="309" height="437" alt="workflow2" src="https://github.com/user-attachments/assets/4c5c578d-4e83-4553-9640-11298e9b2f5b" />


---

## 🤖 Demonstração da IA (Insights Estratégicos)

### Performance por Categoria e Região
O assistente é capaz de cruzar dados de vendas de *Crop Protection* e *Híbridos de Sementes* instantaneamente.

> **[INSERIR PRINT DO CHAT: "Qual a performance de híbridos no Centro-Oeste?"]**

### Ranking de Distribuidores
Identificação rápida de gaps de mercado e performance de fornecedores.

> **[INSERIR PRINT DO CHAT: "Quais os top 5 fornecedores por volume total?"]**

---

## 🛠️ Como Executar
1. Clone o repositório.
2. Configure o Bucket no GCS conforme a estrutura Medallion.
3. Deploy do script Spark no Dataproc.
4. Importação do `workflow.yaml` no Cloud Workflows.

---
**Eduardo Menezes** *Senior Data Engineer | especialista em AI & Cloud*
