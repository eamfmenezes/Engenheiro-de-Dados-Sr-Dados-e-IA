# 🛰️ Bayer GTM Intelligence AI: Data-to-Agent Platform

![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)
![GenAI](https://img.shields.io/badge/Gemini_1.5_Pro-8E75B2?style=for-the-badge&logo=google-gemini&logoColor=white)
![FinOps](https://img.shields.io/badge/Cloud_Workflows-FF9900?style=for-the-badge&logo=google-cloud&logoColor=white)

## 📖 Visão Geral
Este projeto demonstra a criação de um ecossistema completo de dados e IA para o setor de Go-To-Market (GTM) da Bayer. Através da arquitetura **Medallion**, transformamos dados transacionais brutos em uma base de conhecimento (RAG) para um assistente de IA generativa (Gemini).

## 🎯 Objetivo profissional  
O projeto não é apenas um "exercício", mas uma demonstração da concepção e implementação de uma plataforma de dados de ponta a ponta, comprovando com uma implementação real em cloud, com todas as responsabilidades corporativas de um Engenheiro de Dados Sênior especialista em Dados & IA e pode ser implementado em produção para atender às demandas estratégicas de Go-To-Market (GTM) da Bayer. 

Como responsável pela arquitetura, o foco foi conectar a estratégia de negócio a uma solução técnica robusta, atuando como referência em boas práticas e decisões de design desde a ingestão de dados até a demonstração de experiência com MLOps e projetos de IA, atuando na construção de agentes e soluções baseadas em IA, comprovando a experiência em ambientes com alta maturidade de dados para apoiar e lider times tecnicamente.  
.  

A solução foi construída sob os pilares de performance, qualidade e escalabilidade, cobrindo as seguintes frentes de responsabilidades de atuação:

**Arquitetura Lakehouse:** Evolução de um ambiente Cloud (GCP) utilizando a metodologia Medallion para processar grandes volumes de dados de forma eficiente.

**Engenharia de Pipelines:** Desenvolvimento e otimização de processos de ingestão (Landing), transformação (Silver) e disponibilização (Gold) utilizando Python, SQL e Spark.

**Orquestração de Workflows:** Implementação de fluxos resilientes e serverless, conectando processos de **ETL** pesado ao consumo analítico.

**Inovação em IA:** Condução de iniciativas avançadas de IA Generativa, integrando IA com RAG e com a base de dados estruturada a agentes inteligentes para suporte à decisão, com geração automática de gráficos via prompt, insights, planos de ação e correlação com concorrentes via dados da web se requisitado no prompt.

🛠️ Expertise Aplicada (Requisitos Atendidos)
Este projeto consolida uma experiência sólida em:

Cloud Data Stack: Domínio do ecossistema Google Cloud Platform.

Big Data: Processamento distribuído e arquitetura de tabelas Delta.

BI & Analytics: Estruturação de dados para consumo em ferramentas como Power BI e Tableau, garantindo que o dado chegue pronto para a tomada de decisão.

Liderança Técnica: Demonstração de maturidade arquitetural, desde a escolha do orquestrador (FinOps) até a implementação de soluções de MLOps e IA.

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
