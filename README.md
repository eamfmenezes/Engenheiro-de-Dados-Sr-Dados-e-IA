# 🛰️ Bayer GTM Intelligence AI: Data Lakehouse to AI Strategic Agent Platform

![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)
![GenAI](https://img.shields.io/badge/Gemini_1.5_Pro-8E75B2?style=for-the-badge&logo=google-gemini&logoColor=white)
![FinOps](https://img.shields.io/badge/Cloud_Workflows-FF9900?style=for-the-badge&logo=google-cloud&logoColor=white)
![MLOps](https://img.shields.io/badge/MLOps-000000?style=for-the-badge&logo=micropython&logoColor=white)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-CC2927?style=for-the-badge&logo=postgresql&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta_Lake-00ADD8?style=for-the-badge&logo=linux-foundation&logoColor=white)
![Apache Airflow](https://img.shields.io/badge/Apache_Airflow-017CEE?style=for-the-badge&logo=apache-airflow&logoColor=white)


![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)


## 📖 Visão Geral
Este projeto demonstra a criação de um ecossistema completo de dados e IA para o setor de Go-To-Market (GTM) da Bayer. Através da arquitetura **Medallion**, transformamos dados transacionais brutos em uma base de conhecimento (RAG) para um assistente de IA generativa (Gemini).

## 🎯 Objetivo profissional  
O projeto não é apenas um "exercício", mas uma demonstração da concepção e implementação de uma plataforma de dados de ponta a ponta, comprovando com uma implementação real em cloud, com todas as responsabilidades corporativas de um Engenheiro de Dados Sênior especialista em Dados & IA e pode ser implementado em produção para atender às demandas estratégicas de Go-To-Market (GTM) da Bayer. 

Como responsável pela arquitetura, o foco foi conectar a estratégia de negócio a uma solução técnica robusta, atuando como referência em boas práticas e decisões de design desde a ingestão de dados até a demonstração de experiência com MLOps e projetos de IA, atuando na construção de agentes e soluções baseadas em IA, comprovando a experiência em ambientes com alta maturidade de dados para apoiar e lider times tecnicamente.  

A solução foi construída sob os pilares de performance, qualidade e escalabilidade, cobrindo as seguintes frentes de responsabilidades de atuação:

**Arquitetura Lakehouse:** Evolução de um ambiente Cloud (GCP) utilizando a metodologia Medallion em Delta para processar grandes volumes de dados de forma eficiente.

**Engenharia de Pipelines:** Desenvolvimento e otimização de processos de ingestão (Landing), transformação (Silver) e disponibilização (Gold) utilizando Python, SQL e Spark com entrada em Json, saída e disponibilização em Parquet.

**Orquestração de Workflows:** Implementação de fluxos resilientes e serverless, conectando processos de **ETL** pesado ao consumo analítico.

**Inovação em IA:** Condução de iniciativas avançadas de IA Generativa, integrando IA com RAG e com a base de dados estruturada a agentes inteligentes para suporte à decisão, com geração automática de gráficos via prompt, insights, planos de ação e correlação com concorrentes via dados da web se requisitado no prompt.

## 🛠️ Expertise Aplicada (Requisitos Atendidos)
Este projeto consolida uma experiência sólida em:

**Cloud Data Stack**: Domínio do ecossistema Google Cloud Platform (GCP).

**Big Data**: Processamento distribuído com PySpark e arquitetura de tabelas Delta.

**BI & Analytics**: Estruturação de dados para consumo em ferramentas como Power BI e Tableau, garantindo que o dado chegue pronto para a tomada de decisão.

**Agentes de IA e GenAI com RAG**: Configuração e deploy de modelos de ML, Agentes de IA e IA generativa para predição e insights de performance de parceiros comerciais para movimentação de acesso

**Liderança Técnica**: Demonstração de maturidade arquitetural, desde a escolha do orquestrador (FinOps) até a implementação de soluções de MLOps e IA.

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

<img width="207" height="765" alt="image" src="https://github.com/user-attachments/assets/7bdc0336-abb2-4646-aa44-5e0914796e7d" />
<img width="390" height="674" alt="image" src="https://github.com/user-attachments/assets/f5be9b51-1b91-4804-ad4f-ffc3eb77bf99" />

---

# 🤖 Demonstração da IA (Insights Estratégicos)

## Campos disponíveis para análise estratégica  
O agente é capaz de informar sobre os campos sem precisar de conhecimentos técnicos de SQL por exemplo

<img width="691" height="587" alt="image" src="https://github.com/user-attachments/assets/f990dd9c-eb62-4471-a909-d010b655e1ff" />

## Começando a explorar os dados para validar a consistência

### Faturamento: 
<img width="746" height="464" alt="image" src="https://github.com/user-attachments/assets/555d8ee7-b47e-4f11-8f8a-837855e3d6f3" />

## Verificando se a capacidade de drill down atende  
### Iniciando análise estratégica com sugestão de diretrizes obedecendo as regras de negócios:
<img width="626" height="764" alt="image" src="https://github.com/user-attachments/assets/1b8db7df-8813-4187-8780-40dfc9e57a4d" />

## Performance com faturamento
O assistente é capaz de fazer análises de performance comparando os campos
<img width="708" height="729" alt="image" src="https://github.com/user-attachments/assets/2298160c-9e86-4b2e-ad22-6666acb3d4fd" />

### Top 3 com anállise estratégica
<img width="713" height="761" alt="image" src="https://github.com/user-attachments/assets/ea0007e5-d35c-41ef-990c-c41e99a317c3" />

## Planejamento de campanhas baseado em regras de negócios e dados da web  
Note que "safra integrada" citada pelo agente não está nos dados do Lakehouse.  
Esta feature de consulta na web pode ser ativada ou desativada conforme políticas da empresa.  
  
<img width="533" height="809" alt="image" src="https://github.com/user-attachments/assets/ff2482d2-752a-4dfb-b9df-2d4809a3b440" />

### Medindo sucesso da campanha comparando dados do lakehouse com dados da web:
<img width="523" height="760" alt="image" src="https://github.com/user-attachments/assets/2d4dc5b1-30bf-4c00-a191-f73302545f5f" />

## Exemplos de geração de gráficos conforme o prompt que você digitar:
<img width="592" height="791" alt="image" src="https://github.com/user-attachments/assets/c9fd6591-8fe8-4638-8468-92e94222a357" />

<img width="602" height="896" alt="image" src="https://github.com/user-attachments/assets/19e38d8f-c2ff-42ca-b6ee-251d8c0af432" />

## Procurando oportunidades de negócio

<img width="631" height="421" alt="image" src="https://github.com/user-attachments/assets/69fa8c3f-e7c3-4c1e-9f85-72fbca975d1e" />

## Aprofundando o planejamento de campanhas
<img width="623" height="795" alt="image" src="https://github.com/user-attachments/assets/a76efba8-d154-4d7a-98c6-6337e2cbe451" />

## Otimização da movimentação de acesso com proposta de redistribuição estratégica

<img width="694" height="750" alt="image" src="https://github.com/user-attachments/assets/c42a38a5-e325-4476-93fc-970839e600c3" />
<img width="710" height="805" alt="image" src="https://github.com/user-attachments/assets/37e6ac8c-bb8d-4732-a501-6cd5b304ed27" />


---

## 🛠️ Como Executar
1. Clone o repositório.
2. Configure o Bucket no GCS conforme a estrutura Medallion.
3. Deploy do script Spark no Dataproc.
4. Importação do `workflow.yaml` no Cloud Workflows.

---
**Eduardo Menezes** *Senior Data Engineer | especialista em Dados: Engenharia de dados, BI, AI & Cloud*
