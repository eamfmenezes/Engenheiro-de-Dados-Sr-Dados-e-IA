# 🛰️ Bayer GTM Intelligence AI  
## Data Lakehouse to AI Strategic Agent Platform

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

```mermaid
flowchart LR

%% =========================
%% FONTES
%% =========================

A1["Sistemas Transacionais"]
A2["JSON APIs"]
A3["Dados Web & Concorrência"]

%% =========================
%% ORQUESTRAÇÃO
%% =========================

WF["Cloud Workflows\nServerless Orchestration"]
DP["Dataproc Serverless\nPySpark ETL"]

%% =========================
%% LAKEHOUSE
%% =========================

B["Bronze Layer\nRaw JSON"]
C["Silver Layer\nData Cleansing"]
D["Gold Layer\nAnalytics Ready"]

DL["Delta Lake\nACID + Time Travel"]
GCS["Cloud Storage\nLakehouse Storage"]

%% =========================
%% IA
%% =========================

E["Vertex AI Search\nRAG Vector Search"]
F["Gemini Enterprise\nGenAI Agent"]

MLOPS["MLOps\nModel Monitoring"]

%% =========================
%% ANALYTICS
%% =========================

G["Power BI"]
H["Tableau"]

I["Strategic Insights"]
J["Campaign Planning"]
K["AI Graph Generation"]

%% =========================
%% TECNOLOGIAS
%% =========================

P["Python"]
S["PySpark"]
SQL["SQL"]
ETL["ETL Pipelines"]
RAG["RAG Architecture"]

%% =========================
%% FLUXOS
%% =========================

A1 --> WF
A2 --> WF
A3 --> F

WF --> DP

DP --> B
B --> C
C --> D

D --> DL
DL --> GCS

D --> E
E --> F

F --> MLOPS

D --> G
D --> H

F --> I
F --> J
F --> K

DP --> P
DP --> S
DP --> SQL
DP --> ETL

F --> RAG

%% =========================
%% CORES
%% =========================

style A1 fill:#E5E7EB,stroke:#6B7280,stroke-width:2px
style A2 fill:#E5E7EB,stroke:#6B7280,stroke-width:2px
style A3 fill:#E5E7EB,stroke:#6B7280,stroke-width:2px

style WF fill:#FEE2E2,stroke:#EF4444,stroke-width:2px
style DP fill:#FEE2E2,stroke:#EF4444,stroke-width:2px

style B fill:#D1FAE5,stroke:#10B981,stroke-width:2px
style C fill:#DBEAFE,stroke:#3B82F6,stroke-width:2px
style D fill:#FDE68A,stroke:#F59E0B,stroke-width:2px

style DL fill:#FDE68A,stroke:#D97706,stroke-width:2px
style GCS fill:#FDE68A,stroke:#D97706,stroke-width:2px

style E fill:#EDE9FE,stroke:#8B5CF6,stroke-width:2px
style F fill:#EDE9FE,stroke:#8B5CF6,stroke-width:2px
style MLOPS fill:#DDD6FE,stroke:#7C3AED,stroke-width:2px

style G fill:#FBCFE8,stroke:#EC4899,stroke-width:2px
style H fill:#FBCFE8,stroke:#EC4899,stroke-width:2px

style I fill:#C7D2FE,stroke:#6366F1,stroke-width:2px
style J fill:#C7D2FE,stroke:#6366F1,stroke-width:2px
style K fill:#C7D2FE,stroke:#6366F1,stroke-width:2px

style P fill:#DCFCE7,stroke:#16A34A,stroke-width:2px
style S fill:#DCFCE7,stroke:#16A34A,stroke-width:2px
style SQL fill:#DCFCE7,stroke:#16A34A,stroke-width:2px
style ETL fill:#DCFCE7,stroke:#16A34A,stroke-width:2px
style RAG fill:#E9D5FF,stroke:#9333EA,stroke-width:2px
```
---

## 🏗️ Arquitetura do Sistema
## A solução foi desenhada para ser escalável e 100% serverless, minimizando custos operacionais.  

## ⚙️ Orquestração & FinOps
Google Cloud Workflows: O Airflow "custo zero" do GCP. A opção de orquestração pelo GCP Composer tem custo.
O Cloud Workflows é perfeito para esse cenário. Ele orquestra serviços da GCP (Dataproc, Cloud Functions, BigQuery) usando uma estrutura em YAML ou JSON. 


Em vez de utilizar clusters fixos (Airflow), optei pelo **Cloud Workflows**, reduzindo o custo fixo para **zero** durante a ociosidade.

<img width="207" height="600" alt="image" src="https://github.com/user-attachments/assets/7bdc0336-abb2-4646-aa44-5e0914796e7d" />
<img width="300" height="600" alt="image" src="https://github.com/user-attachments/assets/f5be9b51-1b91-4804-ad4f-ffc3eb77bf99" />

---

O intuito é mostrar não ficamos apenas no "fazer o código", mas também pensamos no financeiro (FinOps) e na eficiência da nuvem.  

Para a orquestração, escolhi o Cloud Workflows em vez do Composer. Como a solução é voltada para um modelo SaaS escalável, utilizei uma arquitetura Event-Driven e Serverless.  

Isso reduz o TCO (custo total) para o cliente, já que pagamos apenas pelas execuções, mantendo a visibilidade total do fluxo de dados através do grafo de estados.


main:
  params: [event]
  steps:
    - init_variables:
        assign:
          - project_id: ${sys.get_env("GOOGLE_CLOUD_PROJECT_ID")}
          - region: "us-central1" # ajuste para sua região
          - cluster_name: "bayer-gtm-cluster"
          - lakehouse_status: "STARTING"

    - process_bronze_layer:
        try:
          call: googleapis.dataproc.v1.projects.regions.jobs.submit
          args:
            projectId: ${project_id}
            region: ${region}
            body:
              job:
                pysparkJob:
                  mainPythonFileUri: "gs://bayer-artifacts/scripts/ingest_bronze.py"
                placement:
                  clusterName: ${cluster_name}
          result: bronze_result
        retry: ${http.default_retry}

    - transform_silver_to_gold:
        call: googleapis.dataproc.v1.projects.regions.jobs.submit
        args:
          projectId: ${project_id}
          region: ${region}
          body:
            job:
              pysparkJob:
                mainPythonFileUri: "gs://bayer-artifacts/scripts/refine_gold.py"
              placement:
                clusterName: ${cluster_name}
        result: gold_result

    - refresh_vertex_ai_index:
        call: http.post
        args:
          url: ${"https://discoveryengine.googleapis.com/v1/projects/" + project_id + "/locations/global/collections/default_collection/dataStores/bayer-gtm-gold-ds/branches/0/documents:import"}
          auth:
            type: OAuth2
        result: index_status

    - final_check_and_notify:
        switch:
          - condition: ${index_status.code == 200}
            next: success_notification
        next: handle_failure

    - success_notification:
        return: "Pipeline Bayer GTM finalizado: Dados na Gold e Gemini atualizado."

    - handle_failure:
        raise: "Erro crítico no pipeline de dados GTM."
        

<img width="1408" height="768" alt="Gemini_Generated_Image_gtb32fgtb32fgtb3" src="https://github.com/user-attachments/assets/58cff18b-09bb-42f8-aa04-430c14607b50" />

### Fluxo de Dados:
1. **Ingestão (Bronze):** Captura de 500k registros JSON via Spark.
2. **Refino (Silver):** Tratamento de esquemas e limpeza.
3. **Consumo (Gold):** Tabelas agregadas por `regiao`, `fornecedor` e `categoria`.
4. **Busca Vetorial:** Indexação no Vertex AI Search.
5. **LLM Interface:** Gemini Enterprise respondendo com Grounding na Gold.

---

### Amostra do início do data lakehouse em Delta e scripts do pipeline de ingestão e tratamento (ETL) da arquitetura medalhão:
<img width="1616" height="684" alt="image" src="https://github.com/user-attachments/assets/ac6205d1-6472-4827-a07f-e279e1f21568" />

---

### Evidências do lakehouse em Delta com parquet:
<img width="511" height="461" alt="image" src="https://github.com/user-attachments/assets/b94bc61e-f8d5-499b-98b2-4a9aa23a2e56" />

---


# 🤖 Demonstração da IA (Insights Estratégicos)

<img width="1392" height="939" alt="image" src="https://github.com/user-attachments/assets/344e1183-0a89-4cd5-9074-cbada5eb49e0" />

---

## Campos disponíveis para análise estratégica  
O agente é capaz de informar sobre os campos sem precisar de conhecimentos técnicos de SQL por exemplo

<img width="691" height="587" alt="image" src="https://github.com/user-attachments/assets/f990dd9c-eb62-4471-a909-d010b655e1ff" />

---

## Começando a explorar os dados para validar a consistência

### Faturamento: 
<img width="746" height="464" alt="image" src="https://github.com/user-attachments/assets/555d8ee7-b47e-4f11-8f8a-837855e3d6f3" />

---

## Verificando se a capacidade de drill down atende  
### Iniciando análise estratégica com sugestão de diretrizes obedecendo as regras de negócios:
<img width="626" height="764" alt="image" src="https://github.com/user-attachments/assets/1b8db7df-8813-4187-8780-40dfc9e57a4d" />

---

## Performance com faturamento
O assistente é capaz de fazer análises de performance comparando os campos
<img width="708" height="729" alt="image" src="https://github.com/user-attachments/assets/2298160c-9e86-4b2e-ad22-6666acb3d4fd" />

---

### Top 3 com análise estratégica
<img width="713" height="761" alt="image" src="https://github.com/user-attachments/assets/ea0007e5-d35c-41ef-990c-c41e99a317c3" />

---

## Planejamento de campanhas baseado em regras de negócios e dados da web  
Note que "safra integrada" citada pelo agente não está nos dados do Lakehouse.  
Esta feature de consulta na web pode ser ativada ou desativada conforme políticas da empresa.  
  
<img width="533" height="809" alt="image" src="https://github.com/user-attachments/assets/ff2482d2-752a-4dfb-b9df-2d4809a3b440" />

---

### Medindo sucesso da campanha comparando dados do lakehouse com dados da web:
<img width="523" height="760" alt="image" src="https://github.com/user-attachments/assets/2d4dc5b1-30bf-4c00-a191-f73302545f5f" />

---

## Exemplos de geração de gráficos conforme o prompt que você digitar:
<img width="592" height="791" alt="image" src="https://github.com/user-attachments/assets/c9fd6591-8fe8-4638-8468-92e94222a357" />

<img width="602" height="896" alt="image" src="https://github.com/user-attachments/assets/19e38d8f-c2ff-42ca-b6ee-251d8c0af432" />

---

## Procurando oportunidades de negócio

<img width="631" height="421" alt="image" src="https://github.com/user-attachments/assets/69fa8c3f-e7c3-4c1e-9f85-72fbca975d1e" />

---

## Aprofundando o planejamento de campanhas
<img width="623" height="795" alt="image" src="https://github.com/user-attachments/assets/a76efba8-d154-4d7a-98c6-6337e2cbe451" />

---

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
