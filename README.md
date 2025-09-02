# Projeto Aplicado IV – Previsão da Taxa de Desocupação no Brasil

## 🎯 Objetivo do Projeto
Este projeto tem como objetivo analisar e prever a **taxa de desocupação (desemprego)** no Brasil, com recorte principal por **faixa etária**, utilizando **modelos de séries temporais** e **aprendizado de máquina**.  

O trabalho segue os **Objetivos de Desenvolvimento Sustentável (ODS)**, com foco em:
- **ODS 8**: Trabalho decente e crescimento econômico.  
- **ODS 9**: Indústria, inovação e infraestrutura.  
- **ODS 11**: Cidades e comunidades sustentáveis.  

## ❓ Pergunta de Pesquisa
- Como evolui a taxa de desocupação no Brasil por faixas etárias?  
- É possível prever os próximos períodos com modelos estatísticos (SARIMA/SARIMAX)?  
- Quais variáveis macroeconômicas influenciam diretamente essas taxas (ex.: SELIC, IPCA)?

## 📊 Fontes de Dados
- **IBGE – PNAD Contínua Trimestral (PNADCT / SIDRA)**  
  - Tabela 4094: Taxa de desocupação por grupos de idade.  
  - Tabela 4093: Taxa de desocupação por sexo.  
  - Tabela 4099: Subutilização da força de trabalho.  
  - [Portal PNADCT Brasil](https://sidra.ibge.gov.br/home/pnadct/brasil)  

- **Banco Central do Brasil – API SGS**  
  - SELIC (série 4189).  
  - [SGS API](https://api.bcb.gov.br/dados/serie/bcdata.sgs.4189/dados?formato=json)  

- **IBGE – IPCA (SNIPC/SIDRA)**  

## 🧠 Metodologia
- **Análise Exploratória (EDA):** tendências, sazonalidade e choques (ex.: pandemia).  
- **Modelos de Previsão:**  
  - **SARIMA** (baseline).  
  - **SARIMAX** (com variáveis exógenas: SELIC e IPCA).  
- **Validação:**  
  - Rolling-origin (janela deslizante).  
  - Métricas: MAE, MAPE, sMAPE.  
  - Análise de resíduos (ACF, PACF, Ljung-Box).  

## 📅 Cronograma
- **Etapa 1 (29/08):** Definição do tema, fontes de dados e estrutura do repositório.  
- **Etapa 2 (26/09):** Referencial teórico, metodologia proposta e cronograma detalhado.  
- **Etapa 3 (31/10):** Análise exploratória, implementação inicial do modelo, análise de resíduos.  
- **Etapa 4 (28/11):** Modelos finais, previsões, discussão e entrega do artefato.  

## 📂 Estrutura do Repositório
"'projeto-aplicado-iv-desemprego-br/
│
├── dataset/
│   ├── brutos/              # Dados originais
│   ├── tratados/            # Dados tratados
│   └── exog/                # Variáveis exógenas (ex.: SELIC, IPCA)
│
├── docs/
│   ├── artigo/              # Texto/artigo final
│   └── figuras/             # Figuras e gráficos
│
├── notebooks/
│   ├── entrega1/            # Etapa 1
│   ├── entrega2/            # Etapa 2
│   ├── entrega3/            # Etapa 3
│   ├── entrega4/            # Etapa 4
│   └── 03_modelo_base.ipynb # Modelo inicial
│
├── src/
│   ├── features/            # Scripts de features
│   ├── models/              # Scripts de modelos
│   └── utils/               # Funções auxiliares
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt"'


## 🚀 Execução dos Notebooks no Colab
Clique nos links abaixo para abrir diretamente no Google Colab:

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega1/cd_projeto_aplicado_IV.ipynb) Entrega 1  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega2/cd_projeto_aplicado_IV_entrega_2.ipynb) Entrega 2  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega3/cd_projeto_aplicado_IV_entrega_3.ipynb) Entrega 3  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega4/cd_projeto_aplicado_IV_entrega_4.ipynb) Entrega 4  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/03_modelo_base.ipynb) Modelo Base  

---

## 👥 Autores
- **Franciele do Nascimento Paterni** – Ciência de Dados, Mackenzie.  
- **Professor orientador:** Carlos Scalabrini.  
