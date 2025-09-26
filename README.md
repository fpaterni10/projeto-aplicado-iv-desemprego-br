# PROJETO APLICADO IV - Ciência de Dados EaD - 2025/02

<p align="right">
  <img src="docs/figuras/mackenzie_logo.jpg" alt="Universidade Presbiteriana Mackenzie" width="220"/>
</p>

# Previsão da Taxa de Desemprego no Brasil (2012–2025)

Este projeto tem como objetivo prever mensalmente a taxa de desocupação no Brasil com base nos microdados do **Cadastro Geral de Empregados e Desempregados (CAGED)**, em conjunto com variáveis macroeconômicas, como a **taxa SELIC**, além de indicadores da **PNAD Contínua (IBGE)**. O modelo é construído com técnicas de séries temporais (ARIMA, SARIMA, SARIMAX), visando fornecer subsídios para formulação de políticas públicas, análise socioeconômica e apoio à tomada de decisão.

---

## Objetivo Geral
Desenvolver um modelo preditivo capaz de estimar mensalmente a taxa de desocupação no Brasil para o ano de 2025, utilizando séries temporais alimentadas pelos microdados do CAGED e variáveis exógenas como a taxa SELIC.

## Objetivos Específicos
- Consolidar e tratar uma base mensal do CAGED (2012–2025).  
- Incorporar variáveis macroeconômicas exógenas (SELIC e PNAD Contínua).  
- Verificar propriedades estatísticas da série (estacionariedade, sazonalidade, autocorrelações).  
- Testar modelos de previsão (Naive, ARIMA, SARIMA e SARIMAX).  
- Comparar o desempenho entre modelos univariados e multivariados.  
- Validar previsões para 2025 com métricas de erro (RMSE, MAE, MAPE).  

---

## ODS Relacionados
O projeto está diretamente alinhado ao **ODS 8 – Trabalho decente e crescimento econômico**, pois a taxa de desemprego é um indicador essencial desse objetivo.  

<p align="center">
  <img src="docs/figuras/sdg_08.png" alt="ODS 8 – Trabalho Decente e Crescimento Econômico" width="120"/>
</p>

De forma complementar, também dialoga com:  
- **ODS 9 – Indústria, inovação e infraestrutura**: uso de ciência de dados aplicada como inovação tecnológica.  
- **ODS 11 – Cidades e comunidades sustentáveis**: o desemprego impacta diretamente a qualidade de vida nas cidades e a sustentabilidade social.  

<p align="center">
  <img src="docs/figuras/sdg_09.png" alt="ODS 9 – Indústria, Inovação e Infraestrutura" width="120"/>
  <img src="docs/figuras/sdg_11.png" alt="ODS 11 – Cidades e Comunidades Sustentáveis" width="120"/>
</p>

---

## Fontes de Dados
- **CAGED – Cadastro Geral de Empregados e Desempregados** (Ministério do Trabalho e Emprego), 2012–2025.  
  Formato: `.csv` (microdados mensais e trimestrais).  
  Disponível em: <http://pdet.mte.gov.br/>  

- **PNAD Contínua – Pesquisa Nacional por Amostra de Domicílios Contínua** (IBGE), 2012–2025.  
  Formato: `.csv` e `.xlsx` (trimestral).  
  Disponível em: <https://www.ibge.gov.br>  

- **Taxa SELIC – Banco Central do Brasil**, 2012–2025.  
  Formato: `.csv` (dados diários, consolidados em mensal e trimestral).  
  Disponível em: <https://www.bcb.gov.br>  

---

## Metodologia
- **Aquisição dos dados:** consolidação dos microdados CAGED, PNAD Contínua e da taxa SELIC.  
- **Pré-processamento:** padronização, tratamento de valores ausentes e outliers.  
- **Análise exploratória:** decomposição da série, visualização de tendências e sazonalidade.  
- **Modelagem:**  
  - SARIMA para séries univariadas;  
  - SARIMAX para incluir variáveis exógenas (SELIC e PNAD).  
- **Avaliação:** métricas RMSE, MAE e MAPE.  
- **Validação temporal:** walk-forward e rolling forecast.  

---

## Cronograma

### Etapas 1 e 2: (20/08/2025 — 26/09/2025)
| Nº | Atividade | Responsável(s) | Data início | Data término | Status |
|----|-----------|----------------|-------------|--------------|--------|
| 1 | Definição do título e escopo do projeto | Todos | 20/08/2025 | 07/09/2025 | Concluído |
| 2 | Identificação do grupo (nomes e matrículas) | Todos | 20/08/2025 | 07/09/2025 | Concluído |
| 3 | Redação da Introdução, Motivação e Justificativa | Todos | 20/08/2025 | 07/09/2025 | Concluído |
| 4 | Formulação de Objetivo Geral e Objetivos Específicos | Todos | 20/08/2025 | 07/09/2025 | Concluído |
| 5 | Descrição da base de dados e variáveis exógenas (CAGED, SELIC, PNAD) | Franciele / Guilherme | 20/08/2025 | 07/09/2025 | Concluído |
| 6 | Justificativa metodológica e bibliografia inicial | Aline / Giovanna | 20/08/2025 | 07/09/2025 | Concluído |
| 7 | Planejamento inicial (pipeline + subetapas) | Todos | 20/08/2025 | 25/09/2025 | Concluído |
| 8 | Elaboração da Entrega 2 (introdução, referencial, pipeline, cronograma) | Todos | 10/09/2025 | 25/09/2025 | Concluído |

---

### Etapa 3: Implementação Parcial (25/09/2025 — 31/10/2025)
| Nº | Atividade | Responsável(s) | Data início | Data término | Status |
|----|-----------|----------------|-------------|--------------|--------|
| 9 | Aquisição e integração dos arquivos brutos (CAGED, PNAD, SELIC) | Guilherme / Fran | 25/09/2025 | 28/09/2025 | Em andamento |
| 10 | Pré-processamento e montagem da série mensal consolidada | Fran / Aline | 29/09/2025 | 06/10/2025 | Planejado |
| 11 | Engenharia de features exógenas (SELIC, PNAD, lags, médias móveis) | Guilherme / Giovanna | 29/09/2025 | 06/10/2025 | Planejado |
| 12 | Análise Exploratória de Dados (EDA) e visualizações | Giovanna / Aline | 07/10/2025 | 13/10/2025 | Planejado |
| 13 | Diagrama da solução (fluxo visual do pipeline) | Todos | 07/10/2025 | 10/10/2025 | Planejado |
| 14 | Definição final dos modelos candidatos (ARIMA, SARIMA, SARIMAX) | Todos | 14/10/2025 | 16/10/2025 | Planejado |
| 15 | Treinamento inicial dos modelos clássicos | Aline / Guilherme | 17/10/2025 | 20/10/2025 | Planejado |
| 16 | Treinamento de baseline com redes neurais (opcional) | Giovanna / Fran | 21/10/2025 | 24/10/2025 | Planejado |
| 17 | Avaliação preliminar e ajustes iniciais | Todos | 25/10/2025 | 28/10/2025 | Planejado |
| 18 | Consolidação da Entrega 3 (notebook parcial) | Todos | 29/10/2025 | 31/10/2025 | Planejado |

---

### Etapa 4: Implementação Final (01/11/2025 — 28/11/2025)
| Nº | Atividade | Responsável(s) | Data início | Data término | Status |
|----|-----------|----------------|-------------|--------------|--------|
| 19 | Avaliação final e tuning dos modelos | Todos | 01/11/2025 | 05/11/2025 | Planejado |
| 20 | Geração dos resultados finais (métricas + gráficos + forecast 2025) | Fran / Aline | 06/11/2025 | 10/11/2025 | Planejado |
| 21 | Discussão e conclusão crítica (qualidades, limitações, melhorias) | Giovanna / Guilherme | 11/11/2025 | 15/11/2025 | Planejado |
| 22 | Redação dos resultados e organização no notebook | Todos | 16/11/2025 | 20/11/2025 | Planejado |
| 23 | Revisão final e formatação ABNT nas referências | Todos | 21/11/2025 | 23/11/2025 | Planejado |
| 24 | Preparação da apresentação (slides + vídeo) | Todos | 24/11/2025 | 26/11/2025 | Planejado |
| 25 | Submissão final no GitHub + vídeo | Todos | 27/11/2025 | 28/11/2025 | Planejado |

---


## 📂 Estrutura do Repositório
```
projeto-aplicado-iv-desemprego-br/
│
├── dataset/
│ ├── brutos/
│ ├── tratados/
│ └── exog/
│
├── docs/
│ ├── artigo/
│ └── figuras/
│
├── notebooks/
│ ├── entrega1/
│ ├── entrega2/
│ ├── entrega3/
│ ├── entrega4/
│ └── 03_modelo_base.ipynb
│
├── src/
│ ├── features/
│ ├── models/
│ └── utils/
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt

projeto-aplicado-iv-desemprego-br/
│
├── dataset/
│ ├── brutos/
│ ├── tratados/
│ └── exog/
│
├── docs/
│ ├── artigo/
│ └── figuras/
│
├── notebooks/
│ ├── entrega1/
│ ├── entrega2/
│ ├── entrega3/
│ ├── entrega4/
│ └── 03_modelo_base.ipynb
│
├── src/
│ ├── features/
│ ├── models/
│ └── utils/
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```
---

---

## 🚀 Execução dos Notebooks no Colab
Clique nos links abaixo para abrir diretamente no Google Colab:

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega1/cd_projeto_aplicado_IV.ipynb) Entrega 1  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega2/cd_projeto_aplicado_IV_entrega_2.ipynb) Entrega 2  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega3/cd_projeto_aplicado_IV_entrega_3.ipynb) Entrega 3  
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fpaterni10/projeto-aplicado-iv-desemprego-br/blob/main/notebooks/entrega4/cd_projeto_aplicado_IV_entrega_4.ipynb) Entrega 4  

---

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


