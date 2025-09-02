# PROJETO APLICADO IV - Ciência de Dados EaD - 2025/02

<p align="right">
  <img src="docs/figuras/mackenzie_logo.jpg" alt="Universidade Presbiteriana Mackenzie" width="220"/>
</p>

**Objetivo:** Este projeto tem como objetivo analisar e prever a taxa de desocupação (desemprego) no Brasil, com recorte principal por faixa etária, utilizando modelos de séries temporais e aprendizado de máquina.  

## 🌍 ODS Relacionados
O projeto está diretamente alinhado ao **ODS 8 – Trabalho decente e crescimento econômico**, pois a taxa de desemprego é um indicador essencial desse objetivo.  

<p align="center">
  <img src="docs/figuras/sdg_08.png" alt="ODS 8 – Trabalho Decente e Crescimento Econômico" width="120"/>
  </p>

De forma complementar, também dialoga com:  
- **ODS 9 – Indústria, inovação e infraestrutura**, pela aplicação de ciência de dados e métodos de previsão como instrumentos de inovação analítica.  
- **ODS 11 – Cidades e comunidades sustentáveis**, já que o desemprego impacta diretamente a qualidade de vida nas cidades e a sustentabilidade social.  

<p align="center">
  <img src="docs/figuras/sdg_09.png" alt="ODS 9 – Indústria, Inovação e Infraestrutura" width="120"/>
  <img src="docs/figuras/sdg_11.png" alt="ODS 11 – Cidades e Comunidades Sustentáveis" width="120"/>
</p>


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
```
projeto-aplicado-iv-desemprego-br/
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
└── requirements.txt
```


## 🚀 Execução dos Notebooks no Colab
Clique nos links abaixo para abrir diretamente no Google Colab:

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega1/cd_projeto_aplicado_IV.ipynb) Entrega 1  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega2/cd_projeto_aplicado_IV_entrega_2.ipynb) Entrega 2  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega3/cd_projeto_aplicado_IV_entrega_3.ipynb) Entrega 3  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega4/cd_projeto_aplicado_IV_entrega_4.ipynb) Entrega 4  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/03_modelo_base.ipynb) Modelo Base  

---

## 👥 Autores

Aline Correa de Araújo – RA: 10414773 – 10414773@mackenzista.com.br

Franciele Paterni – RA: 10414598 – 10414598@mackenzista.com.br

Giovanna Sobral da Silva – RA: 10424600 – 10424600@mackenzista.com.br

Guilherme Soares Frota – RA: 10416060 – 10416060@mackenzista.com.br

- **Professor orientador:** Carlos Scalabrini.  
