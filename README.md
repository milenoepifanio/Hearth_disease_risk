# Cardiovascular Diseases Risk Prediction

Este repositório contém dois modelos principais para prever o risco de doenças cardiovasculares usando o Cardiovascular Diseases Risk Prediction Dataset, que é baseado no conjunto de dados BRFSS 2021 (Behavioral Risk Factor Surveillance System), fornecido pelos Centers for Disease Control and Prevention (CDC).

O projeto utiliza duas abordagens de aprendizado de máquina:

Modelo Supervisionado baseado em Ensemble de Boosting, otimizado para maximizar o recall na previsão do risco de doenças cardiovasculares.
Modelo Não Supervisionado de Classificação para identificar padrões e grupos de risco sem a necessidade de rótulos.

## Objetivo

O principal objetivo deste projeto é prever o risco de doenças cardiovasculares em indivíduos com base em características relacionadas a estilo de vida e saúde. Utilizamos duas abordagens para alcançar esse objetivo:

**Modelo Supervisionado:** Treinamos um ensemble de modelos de boosting (como XGBoost, LightGBM ou AdaBoost) para classificar os indivíduos com maior risco de doenças cardiovasculares, com ênfase na maximização do recall para detectar corretamente casos positivos (indivíduos de alto risco).

**Modelo Não Supervisionado:** Aplicamos técnicas de clustering (K-means) para descobrir padrões e grupos de indivíduos com características semelhantes, identificando segmentos de alto risco sem a necessidade de rótulos de classe.

## Dataset

O dataset utilizado é o **2021 BRFSS Dataset** (Behavioral Risk Factor Surveillance System), fornecido pelo **CDC**. Ele contém informações sobre diversos conhecidos fatores de risco para doenças crônicas, incluindo doenças cardiovasculares:

- Idade
- Gênero
- Índice de Massa Corporal (IMC)
- Pressão arterial
- Níveis de atividade física
- Histórico de tabagismo
- Consumo de álcool
- Entre outros fatores.

Você pode encontrar o dataset completo no [Kaggle](https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset).

### Estrutura do Dataset

O dataset contém as seguintes colunas:

        - General_Health (Saúde Geral): Autoavaliação da saúde geral do indivíduo (excelente, boa, regular, ruim).
        - Checkup (Exame de Check-up): Se o participante realizou um check-up médico nos últimos 12 meses.
        - Exercise (Exercício): Frequência de prática de atividades físicas ou exercícios.
        - Heart_Disease (Doença Cardiovascular): Indicação de diagnóstico de doença cardiovascular.
        - Skin_Cancer (Câncer de Pele): Indicação de diagnóstico de câncer de pele.
        - Other_Cancer (Outro Câncer): Indicação de diagnóstico de outros tipos de câncer, exceto pele.
        - Depression (Depressão): Indicação de diagnóstico de depressão.
        - Diabetes (Diabetes): Indicação de diagnóstico de diabetes
        - Arthritis (Artrite): Indicação de diagnóstico de artrite.
        - Sex (Sexo): Gênero do participante (masculino ou feminino).
        - Age_Category (Categoria de Idade): Faixa etária do participante.
        - Height_(cm) (Altura em cm): Altura do participante em centímetros.
        - Weight_(kg) (Peso em kg): Peso do participante em quilogramas.
        - BMI (Índice de Massa Corporal): Índice de massa corporal calculado a partir da altura e peso.
        - Smoking_History (Histórico de Tabagismo): Histórico de tabagismo do participante.
        - Alcohol_Consumption (Consumo de Álcool): Frequência de consumo de álcool pelo participante.
        - Fruit_Consumption (Consumo de Frutas): Frequência de consumo de frutas pelo participante.
        - Green_Vegetables_Consumption (Consumo de Legumes Verdes): Frequência de consumo de vegetais verdes.
        - FriedPotato_Consumption (Consumo de Batata Frita): Frequência de consumo de batatas fritas.

##Requisitos
Para executar este projeto, você precisará de:

- Python 3.8+
- Bibliotecas:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `xgboost` (opcional para modelos avançados)

Você pode instalar as dependências necessárias utilizando o arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

## Estrutura do Projeto

A estrutura do repositório é a seguinte:

```
.
├── data/
│   └── df_preprocessed.csv       # Dataset Pré-processado e balanceado
|   └── CVD_cleaned.csv           # Dataset limpo, como disponibilizado no Kaggle
├── src/
│   ├── EDA.py                    # Análise exploratória dos dados
│   ├── model_preprocess.py       # Pré-processamento do modelo
│   ├── model_training.py         # treinamento e avaliação do modelo
│   ├── results_analysis.py       # Avaliação do modelo
├── requirements.txt              # Dependências do projeto
└── README.md                     # Este arquivo
```
  
