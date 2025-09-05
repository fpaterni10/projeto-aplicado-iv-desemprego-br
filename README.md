# PROJETO APLICADO IV - Ciência de Dados EaD - 2025/02


<p align="right">
  <img src="docs/figuras/mackenzie_logo.jpg" alt="Universidade Presbiteriana Mackenzie" width="220"/>
</p>

# Previsão da Taxa de Desemprego na Região Metropolitana de São Paulo (2015–2019)

Este projeto tem como objetivo prever mensalmente a taxa de desemprego na Região Metropolitana de São Paulo (RMSP) com base nos microdados da Pesquisa de Emprego e Desemprego (PED), em conjunto com variáveis macroeconômicas, como a taxa SELIC. O modelo é construído com técnicas de séries temporais e modelos SARIMA/SARIMAX, visando auxiliar a formulação de políticas públicas de geração de emprego e renda.


**Objetivo Geral:**  
  Desenvolver um modelo preditivo para estimar mensalmente a taxa de desemprego na RMSP, utilizando microdados da PED e variáveis econômicas agregadas.

**Objetivos Específicos:**  
  - Realizar análise exploratória da série temporal (comportamento, sazonalidade, tendências);  
  - Verificar a estacionariedade da série com o teste de Dickey-Fuller;  
  - Aplicar modelagens SARIMA e SARIMAX, comparando desempenho com e sem variáveis exógenas (ex: SELIC);  
  - Avaliar métricas de desempenho das previsões (MAE, RMSE, MAPE).

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


## Fontes de Dados
Descrição da Base de Dados

- **Fonte principal:**  
  Microdados da Pesquisa de Emprego e Desemprego (PED) – Região Metropolitana de São Paulo, disponibilizada pelo DIEESE e Fundação Seade.

- **Formato:** Arquivos `.SAV` (SPSS)

- **Período:** Janeiro de 2015 a Março de 2019

- **Frequência:** Mensal

- **Segmentação:** Dados desagregados por situação de atividade, posição na ocupação, setor de atividade, escolaridade, entre outras variáveis sociodemográficas

- **Fonte complementar:**  
  Taxa SELIC histórica (mensal), disponibilizada via API pelo Banco Central do Brasil


## Metodologia

- Análise exploratória e estatística descritiva da série
- Verificação de:
  - Estacionariedade (ADF test)
  - Linearidade
  - Sazonalidade
  - Média e variância ao longo do tempo
- Modelos aplicados:
  - **SARIMA** (série temporal univariada)
  - **SARIMAX** (com variáveis exógenas, como SELIC)
- Avaliação de desempenho com métricas: RMSE, MAE e MAPE
- Comparações visuais das previsões e valores reais


## Cronograma
- **Etapa 1 (29/08):** Definição do tema, fontes de dados e estrutura do repositório.  
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

DEPARTAMENTO INTERSINDICAL DE ESTATÍSTICA E ESTUDOS SOCIOECONÔMICOS (DIEESE). Microdados da Pesquisa de Emprego e Desemprego – Região Metropolitana de São Paulo. São Paulo: DIEESE, 2020. Disponível em: https://www.dieese.org.br/analiseped/pedRMSP.html. Acesso em: set. 2025.

BANCO CENTRAL DO BRASIL (BACEN). Sistema Gerenciador de Séries Temporais – Taxa SELIC. Disponível em: https://www.bcb.gov.br/estatisticas/sgs. Acesso em: set. 2025.

PREFEITURA DE SÃO PAULO. Relatórios Socioeconômicos da RMSP. Disponível em: https://www.prefeitura.sp.gov.br. Acesso em: set. 2025.
