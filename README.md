# PROJETO APLICADO IV - Ciência de Dados EaD - 2025/02

<p align="right">
  <img src="docs/figuras/mackenzie_logo.jpg" alt="Universidade Presbiteriana Mackenzie" width="220"/>
</p>

# Previsão da Taxa de Desemprego no Brasil (2012–2025)

Este projeto tem como objetivo prever mensalmente a taxa de desocupação no Brasil com base nos microdados do **Cadastro Geral de Empregados e Desempregados (CAGED)**, em conjunto com variáveis macroeconômicas, como a **taxa SELIC**. O modelo é construído com técnicas de séries temporais (ARIMA, SARIMA, SARIMAX), visando fornecer subsídios para formulação de políticas públicas, análise socioeconômica e apoio à tomada de decisão.

---

## Objetivo Geral
Desenvolver um modelo preditivo capaz de estimar mensalmente a taxa de desocupação no Brasil para o ano de 2025, utilizando séries temporais alimentadas pelos microdados do CAGED e variáveis exógenas como a taxa SELIC.

## Objetivos Específicos
- Consolidar e tratar uma base mensal do CAGED (2012–2025).  
- Incorporar variáveis macroeconômicas exógenas (SELIC).  
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
- **ODS 9 – Indústria, inovação e infraestrutura**, pela aplicação de ciência de dados e métodos de previsão como instrumentos de inovação analítica.  
- **ODS 11 – Cidades e comunidades sustentáveis**, já que o desemprego impacta diretamente a qualidade de vida nas cidades e a sustentabilidade social.  

<p align="center">
  <img src="docs/figuras/sdg_09.png" alt="ODS 9 – Indústria, Inovação e Infraestrutura" width="120"/>
  <img src="docs/figuras/sdg_11.png" alt="ODS 11 – Cidades e Comunidades Sustentáveis" width="120"/>
</p>

---

## Fontes de Dados
- **Fonte principal:**  
  Cadastro Geral de Empregados e Desempregados (CAGED) – Ministério do Trabalho e Emprego, 2012–2025.  
  [http://pdet.mte.gov.br/](http://pdet.mte.gov.br/)  

- **Formato:** Arquivos `.csv` (microdados mensais).  

- **Fonte complementar:**  
  Taxa SELIC histórica (mensal), disponibilizada pelo **Banco Central do Brasil**.  

---

## Metodologia
- **Aquisição dos dados:** consolidação dos microdados CAGED e da taxa SELIC.  
- **Pré-processamento:** padronização, tratamento de valores ausentes e outliers.  
- **Análise exploratória:** decomposição da série, visualização de tendências e sazonalidade.  
- **Modelagem:**  
  - SARIMA para séries univariadas;  
  - SARIMAX para incluir variáveis exógenas (SELIC).  
- **Avaliação:** métricas RMSE, MAE e MAPE.  
- **Validação temporal:** walk-forward e rolling forecast.  

---


## Cronograma
- **Etapa 1 (07/09):** Definição do tema, fontes de dados e estrutura do repositório.  
- **Etapa 2 (26/09):** Referencial teórico, metodologia proposta e cronograma detalhado.  
- **Etapa 3 (31/10):** Análise exploratória, implementação inicial do modelo, análise de resíduos.  
- **Etapa 4 (28/11):** Modelos finais, previsões, discussão e entrega do artefato.  


## 📂 Estrutura do Repositório

```
projeto-aplicado-iv-desemprego-sp/
│
├── dataset/
│   ├── brutos/
│   ├── tratados/
│   └── exog/
│
├── docs/
│   ├── artigo/
│   └── figuras/
│
├── notebooks/
│   ├── entrega1/
│   ├── entrega2/
│   ├── entrega3/
│   ├── entrega4/
│   └── 03_modelo_base.ipynb
│
├── src/
│   ├── features/
│   ├── models/
│   └── utils/
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

---

## 👥 Autores

Aline Correa de Araújo – RA: 10414773 – 10414773@mackenzista.com.br

Franciele Paterni – RA: 10414598 – 10414598@mackenzista.com.br

Giovanna Sobral da Silva – RA: 10424600 – 10424600@mackenzista.com.br

Guilherme Soares Frota – RA: 10416060 – 10416060@mackenzista.com.br

- **Professor orientador:** Gustavo Scalabrini Sampaio


## Referências

## Referências
- HYNDMAN, R. J.; ATHANASOPOULOS, G. *Forecasting: principles and practice.* 2ª ed. Online.
- OLIVEIRA, R.; ALBARRACIN, O. Y.; SILVA, G. R. *Introdução às Séries Temporais: Uma Abordagem Prática em Python.* 2023.
- CASAGRANDE, D. L.; OLIVEIRA, F. R.; STUDART, G. *Métodos de previsão para a taxa de desemprego mensal: uma análise de séries temporais.* Revista de Economia, 2016.
- BRASIL. Ministério do Trabalho e Emprego. **Cadastro Geral de Empregados e Desempregados – CAGED**. Brasília: MTE, 2012–2025. Disponível em: <http://pdet.mte.gov.br/>. Acesso em: set. 2025.  
- BANCO CENTRAL DO BRASIL. *Taxa SELIC – histórico mensal.* Brasília, 2012–2025.  
