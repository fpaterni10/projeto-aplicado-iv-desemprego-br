# PROJETO APLICADO IV - Ciência de Dados EaD - 2025/02

<p align="right">
  <img src="docs/figuras/mackenzie_logo.jpg" alt="Universidade Presbiteriana Mackenzie" width="220"/>
</p>

**Objetivo:** Previsão da Taxa de Desocupação no Estado de São Paulo

Este projeto tem como objetivo prever a taxa de desocupação (desemprego) no estado de São Paulo com base em séries temporais históricas, utilizando modelos estatísticos como Prophet. A intenção é fornecer previsões que orientem políticas públicas, decisões estratégicas e estudos acadêmicos voltados ao mercado de trabalho paulista.

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


## 📊 Fontes de Dados
As informações foram extraídas do site do IBGE (Instituto Brasileiro de Geografia e Estatística), com base na Pesquisa Nacional por Amostra de Domicílios Contínua Trimestral (PNADC-T).

Indicador: Taxa de desocupação no estado de São Paulo (todas as idades, ambos os sexos)
Tabela SIDRA 4095: Taxa de desocupação por UF e trimestres móveis
Formato: .xlsx
Período: 1º trimestre de 2012 a 2º trimestre de 2024
Frequência: Trimestral
Fonte ABNT:

INSTITUTO BRASILEIRO DE GEOGRAFIA E ESTATÍSTICA (IBGE). Pesquisa Nacional por Amostra de Domicílios Contínua – PNADC (trimestral): Tabela 4095 – Taxa de desocupação, por UF. Disponível em: https://sidra.ibge.gov.br/tabela/4095


## 🧠 Metodologia

Etapas:
- Coleta e consolidação da série histórica
- Análise exploratória da série temporal
- Tendência
- Estacionariedade
- Picos atípicos (ex.: pandemia)
- Pré-processamento
- Preenchimento de dados ausentes
- Testes de estacionariedade

Modelagem:
- Prophet (Meta/Facebook)
- Avaliação dos resultados:
- Métricas como MAE, MAPE, RMSE
- Análise de resíduos  


## 📅 Cronograma
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
