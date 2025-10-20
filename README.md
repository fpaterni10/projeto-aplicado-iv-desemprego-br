# PROJETO APLICADO IV - Ciência de Dados EaD - 2025/02

<p align="right">
  <img src="docs/figuras/mackenzie_logo.jpg" alt="Universidade Presbiteriana Mackenzie" width="220"/>
</p>

# Previsão da Taxa de Desemprego no Brasil (2012–2025)

Este projeto tem como objetivo prever a **taxa de desocupação no Brasil** com base nos microdados do **Cadastro Geral de Empregados e Desempregados (CAGED)**, em conjunto com variáveis macroeconômicas, como a **taxa SELIC**, além de indicadores da **PNAD Contínua (IBGE)**. O modelo é construído com técnicas de séries temporais (ARIMA, SARIMA, SARIMAX e regressão de gradiente), visando fornecer subsídios para formulação de políticas públicas, análise socioeconômica e apoio à tomada de decisão.

---

## Objetivo Geral
Desenvolver um **modelo preditivo** capaz de estimar a taxa de desocupação no Brasil para o período recente, integrando informações do **mercado formal** (CAGED) e **condições monetárias** (SELIC), com apoio da **PNAD Contínua** para validação e comparação.

## Objetivos Específicos
- Consolidar e tratar uma base **2012–2025** com CAGED, PNAD e SELIC.  
- Incorporar variáveis exógenas (SELIC e derivadas do CAGED) e **engenharia de atributos** (lags, médias móveis, dummies sazonais/estruturais).  
- Verificar propriedades estatísticas (estacionariedade, sazonalidade, autocorrelações) via **ADF, ACF e PACF**.  
- Testar modelos de previsão (**Naive, ARIMA, SARIMA, SARIMAX** e **LGBM Regressor**).  
- Comparar desempenho de **modelos estatísticos** e de **machine learning**.  
- Validar previsões com **RMSE, MAE e MAPE** e análise de resíduos.

---

## ODS Relacionados
O projeto está diretamente alinhado ao **ODS 8 – Trabalho decente e crescimento econômico**, pois a taxa de desemprego é um indicador essencial desse objetivo.

<p align="center">
  <img src="docs/figuras/sdg_08.png" alt="ODS 8 – Trabalho Decente e Crescimento Econômico" width="120"/>
</p>

De forma complementar, também dialoga com:  
- **ODS 9 – Indústria, inovação e infraestrutura:** uso de ciência de dados aplicada como inovação tecnológica.  
- **ODS 11 – Cidades e comunidades sustentáveis:** o desemprego impacta diretamente a qualidade de vida nas cidades.

<p align="center">
  <img src="docs/figuras/sdg_09.png" alt="ODS 9 – Indústria, Inovação e Infraestrutura" width="120"/>
  <img src="docs/figuras/sdg_11.png" alt="ODS 11 – Cidades e Comunidades Sustentáveis" width="120"/>
</p>

---

## 🔗 Notebooks (Etapas)

> Dica: se o *viewer* do GitHub oscilar, use **Colab** ou **nbviewer**.

| Etapa | Descrição | GitHub | Colab | nbviewer |
|:--:|---|---|---|---|
| **1** | Escopo, fontes de dados, documento inicial | [Abrir](https://github.com/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega1/cd_projeto_aplicado_IV.ipynb) | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega1/cd_projeto_aplicado_IV.ipynb) | [Ver](https://nbviewer.org/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega1/cd_projeto_aplicado_IV.ipynb) |
| **2** | EDA, componentes da série, pipeline | [Abrir](https://github.com/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega2/cd_projeto_aplicado_IV_entrega_2.ipynb) | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega2/cd_projeto_aplicado_IV_entrega_2.ipynb) | [Ver](https://nbviewer.org/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega2/cd_projeto_aplicado_IV_entrega_2.ipynb) |
| **3** | Modelagem inicial (SARIMAX e LGBM), avaliação e comparação | [Abrir](https://github.com/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega3/cd_projeto_aplicado_IV_entrega_3.ipynb) | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega3/cd_projeto_aplicado_IV_entrega_3.ipynb) | [Ver](https://nbviewer.org/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega3/cd_projeto_aplicado_IV_entrega_3.ipynb) |

---

## Fontes de Dados
- **CAGED – Cadastro Geral de Empregados e Desempregados** (Ministério do Trabalho e Emprego), 2012–2025.  
  Formato: `.csv` (microdados mensais; agregações para análises).  
- **PNAD Contínua – Pesquisa Nacional por Amostra de Domicílios Contínua** (IBGE), 2012–2025.  
  Formato: `.csv`/`.xlsx` (trimestral).  
- **Taxa SELIC – Banco Central do Brasil (SGS)**, 2012–2025.  
  Formato: `.csv` (diária → consolidado mensal/trimestral).

> Harmonização temporal: as séries são **padronizadas para frequência trimestral** quando necessário para comparação e modelagem.

---

## Metodologia (visão geral)

- **Aquisição:** CAGED (admissões, desligamentos, saldo), PNAD (taxa de desocupação) e SELIC (SGS).  
- **Pré-processamento:** padronização de datas; tratamento de ausentes; *outliers*; features derivadas: `saldo`, `caged_roll3`, `caged_roll3_asinh`, **lags**, **dummies sazonais/estruturais**.  
- **EDA e Análise Temporal:** **ADF**, **ACF/PACF**, **decomposição** (tendência, sazonalidade e ruído).  
- **Modelagem:**  
  - **SARIMAX** — (1,1,2)×(1,0,1,4) com exógenas do CAGED;  
  - **LGBM Regressor** — com *lags* e *rolling features*.  
- **Validação:** **holdout temporal** (Etapa 3); comparação por **MAE, RMSE, MAPE**.  
- **Visualização:** gráficos **Real vs. Pred** e **Resíduos**; ACF dos resíduos.

<p align="center">
  <img src="docs/figuras/pipeline_etapa3_v3.png" width="720" alt="Pipeline da Solução - Etapa 3"/>
</p>

---

## Resultados – Etapa 3 (resumo)

| Modelo | MAE | RMSE | MAPE (%) | Observação |
|:--|--:|--:|--:|:--|
| **LGBM (calibrado)** | **0,2966** | **0,3481** | **4,90** | Melhor desempenho geral |
| **SARIMAX (1,1,2)×(1,0,1,4)** | 0,3620 | 0,4330 | 5,54 | Baseline estatístico interpretável |

> Gráficos e detalhes no notebook da **Etapa 3**: Real vs. Pred (calibrado), Resíduos, ACF/PACF e decomposições.

---

## Cronograma

### Etapas 1 e 2: (20/08/2025 — 26/09/2025)
| Nº | Atividade | Responsável(s) | Início | Término | Status |
|----|-----------|----------------|-------|---------|--------|
| 1 | Definição do título e escopo do projeto | Todos | 20/08/2025 | 07/09/2025 | **Concluído** |
| 2 | Identificação do grupo (nomes e matrículas) | Todos | 20/08/2025 | 07/09/2025 | **Concluído** |
| 3 | Introdução, Motivação e Justificativa | Todos | 20/08/2025 | 07/09/2025 | **Concluído** |
| 4 | Objetivo geral e objetivos específicos | Todos | 20/08/2025 | 07/09/2025 | **Concluído** |
| 5 | Descrição da base e variáveis exógenas | Franciele / Guilherme | 20/08/2025 | 07/09/2025 | **Concluído** |
| 6 | Justificativa metodológica e bibliografia inicial | Aline / Giovanna | 20/08/2025 | 07/09/2025 | **Concluído** |
| 7 | Planejamento (pipeline + subetapas) | Todos | 20/08/2025 | 25/09/2025 | **Concluído** |
| 8 | Entrega 2 (introdução, referencial, pipeline, cronograma) | Todos | 10/09/2025 | 25/09/2025 | **Concluído** |

### Etapa 3: Implementação Parcial (25/09/2025 — 31/10/2025)
| Nº | Atividade | Responsável(s) | Início | Término | Status |
|----|-----------|----------------|-------|---------|--------|
| 9 | Aquisição e integração dos brutos (CAGED + SELIC) | Guilherme / Fran | 25/09/2025 | 28/09/2025 | **Concluído** |
| 10 | Pré-processamento e série consolidada | Fran / Aline | 29/09/2025 | 06/10/2025 | **Concluído** |
| 11 | Engenharia de *features* exógenas | Guilherme / Giovanna | 29/09/2025 | 06/10/2025 | **Planejado** |
| 11.1 | **EDA e pré-processamento** | — | 05/10/2025 | 07/10/2025 | **Concluído** |
| 11.2 | **Modelo LGBM** | — | 07/10/2025 | 09/10/2025 | **Concluído** |
| 11.3 | **Modelo SARIMAX** | — | 09/10/2025 | 11/10/2025 | **Concluído** |
| 11.4 | **Comparação e discussão** | — | 11/10/2025 | 12/10/2025 | **Concluído** |
| 11.5 | **Revisão, cronograma e referências** | — | 13/10/2025 | 14/10/2025 | **Concluído** |
| 12 | Visualizações (EDA) | Giovanna / Aline | 07/10/2025 | 13/10/2025 | **Concluído** |
| 13 | Diagrama da solução (pipeline) | Todos | 07/10/2025 | 10/10/2025 | **Concluído** |
| 14 | Definição final dos modelos candidatos | Todos | 14/10/2025 | 16/10/2025 | **Concluído** |
| 15 | Treinamento inicial (clássicos) | Aline / Guilherme | 17/10/2025 | 20/10/2025 | **Planejado** |
| 16 | Avaliação preliminar e ajustes | Giovanna / Fran | 21/10/2025 | 24/10/2025 | **Planejado** |
| 17 | Consolidação da Entrega 3 (notebook) | Todos | 29/10/2025 | 31/10/2025 | **Planejado** |

---

## 📂 Estrutura do Repositório
```
projeto-aplicado-iv-desemprego-br/
├── dataset/
│ ├── brutos/
│ ├── tratados/
│ └── exog/
├── docs/
│ ├── artigo/
│ └── figuras/
├── notebooks/
│ ├── entrega1/
│ ├── entrega2/
│ └── entrega3/
├── src/
│ ├── features/
│ ├── models/
│ └── utils/
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```
---


## 🚀 Execução no Colab (atalhos rápidos)
- **Etapa 1:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega1/cd_projeto_aplicado_IV.ipynb)  
- **Etapa 2:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega2/cd_projeto_aplicado_IV_entrega_2.ipynb)  
- **Etapa 3:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega3/cd_projeto_aplicado_IV_entrega_3.ipynb)  

## 👥 Autores

- **Aline Correa de Araújo** – RA: 10414773 – 10414773@mackenzista.com.br  
- **Franciele Paterni** – RA: 10414598 – 10414598@mackenzista.com.br  
- **Giovanna Sobral da Silva** – RA: 10424600 – 10424600@mackenzista.com.br  
- **Guilherme Soares Frota** – RA: 10416060 – 10416060@mackenzista.com.br  

**Professor orientador:** Gustavo Scalabrini Sampaio

---

## Referências
- HYNDMAN, R. J.; ATHANASOPOULOS, G. *Forecasting: principles and practice.* 2. ed. Melbourne: OTexts, 2021.  
- OLIVEIRA, R.; ALBARRACIN, O. Y.; SILVA, G. R. *Introdução às Séries Temporais: Uma Abordagem Prática em Python.* Rio de Janeiro: Alta Books, 2023.  
- CASAGRANDE, D. L.; OLIVEIRA, F. R.; STUDART, G. *Métodos de previsão para a taxa de desemprego mensal: uma análise de séries temporais.* Revista de Economia, v. 42, n. 2, p. 55–73, 2016.  
- INSTITUTO BRASILEIRO DE GEOGRAFIA E ESTATÍSTICA (IBGE). *Pesquisa Nacional por Amostra de Domicílios Contínua – PNAD Contínua.* Disponível em: <https://www.ibge.gov.br>. Acesso em: 25 set. 2025.  
- MINISTÉRIO DO TRABALHO E EMPREGO (MTE). *Cadastro Geral de Empregados e Desempregados – CAGED.* Disponível em: <http://pdet.mte.gov.br/>. Acesso em: 25 set. 2025.  
- BANCO CENTRAL DO BRASIL (BACEN). *Sistema Gerenciador de Séries Temporais – Taxa SELIC.* Disponível em: <https://www.bcb.gov.br>. Acesso em: 25 set. 2025.  
- AGÊNCIA GOV. *Desocupação cai para 6,4%, segunda menor taxa da série histórica.* Brasília: EBC, 31 out. 2024. Disponível em: <https://agenciagov.ebc.com.br>. Acesso em: 25 set. 2025.  
