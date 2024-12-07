_Este projeto consiste no trabalho final de Machine Learning II da trilha de Data Science do Programa Santander Coders 2024.1._ 

* **Módulo** Machine Learning II
* **Instrutor:** Prof. Rogério Marinardes ([GitHub](https://github.com/milenoepifanio) / [LinkedIn](https://www.linkedin.com/in/rogerioomds/))
* **Grupo**: 
    - Larissa ([GitHub](https://github.com/Larita404) / [LinkedIn](https://www.linkedin.com/in/larissatoscano/));
    - Mileno Epifânio ([GitHub](https://github.com/milenoepifanio) / [LinkedIn](https://www.linkedin.com/in/milenoepifanio/));


## Dataset - Cardiovascular Diseases Risk Prediction

O dataset utilizado é o **2021 BRFSS Dataset** (Behavioral Risk Factor Surveillance System), fornecido pelo **CDC** (Centers for Disease Control and Prevention). Ele contém informações sobre diversos conhecidos fatores de risco para doenças crônicas, incluindo doenças cardiovasculares. 

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

Você pode encontrar o dataset completo no [Kaggle](https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset).


## Problema de Negócio  
As doenças cardiovasculares representam uma das principais causas de mortalidade no mundo, demandando ações preventivas eficazes para 
reduzir seu impacto na saúde pública. O problema que este projeto busca resolver é: **como prever o risco de doenças cardiovasculares em 
indivíduos, permitindo intervenções precoces e personalizadas?**  

Um sistema preditivo eficiente possibilita identificar indivíduos com alto risco, priorizando ações preventivas e reduzindo os custos 
associados ao tratamento de complicações avançadas. Além disso, promove uma abordagem mais direcionada para políticas de saúde pública 
e melhora a qualidade de vida dos pacientes em potencial.  

---

## Objetivos  

### Prever o Risco Cardiovascular  
Desenvolver um modelo de classificação que estime o risco de doenças cardiovasculares em indivíduos com base em fatores relacionados a estilo de vida, histórico médico e dados demográficos.  

### Apoiar Decisões de Intervenção  
Automatizar a identificação de indivíduos de alto risco com o uso de algoritmos preditivos, permitindo intervenções mais rápidas, eficazes e baseadas em evidências.  

### Aprimorar Estratégias de Saúde Preventiva  
Fornecer insights para auxiliar profissionais de saúde e formuladores de políticas na definição de estratégias que reduzam a incidência de doenças cardiovasculares na população.  




## Sobre o projeto

Este projeto visa desenvolver um sistema preditivo focado no risco de doenças cardiovasculares em indivíduos com base em características relacionadas a estilo de vida e saúde. Utilizamos duas abordagens para alcançar esse objetivo:

**Modelo Supervisionado:** Treinamos um ensemble de modelos de boosting (como XGBoost, LightGBM ou AdaBoost) para classificar os indivíduos com maior risco, com ênfase na maximização do recall para detectar corretamente casos positivos (indivíduos de alto risco).

**Modelo Não Supervisionado:** Aplicamos técnicas de clustering (K-means) para descobrir padrões e grupos de indivíduos com características semelhantes, identificando segmentos de alto risco sem a necessidade de rótulos de classe.

## Instalação 

1. Clone o repositório:

```bash
git clone https://github.com/Larita404/Hearth_disease_risk.git
```

## Requisitos
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


## Insights da Análise Exploratória de Dados
- Maioria dos casos diagnósticados são em mulheres
- Usuários diagnósticados tinham a pré-disposição de consumo maior de álcool, mais peso (massa corporal), consumiam do tabagismo e idades mais velhas.


## Features

### Features Categóricas
As features categóricas que precisamos pré-processar foram 'General_Health' 'Checkup', 'Exercise', 'Heart_Disease', 'Skin_Cancer', 'Other_Cancer', 'Depression', 'Diabetes', 'Arthritis', 'Sex', 'Age_Category', 'Smoking_History', nas quais utilizamos One-hot Enconder.

Os dados prontos para treinamento estão salvos em seus devidos diretórios.

### Features Numéricas
As features numericas são Height_(cm), Weight_(kg), BMI, Alcohol_Consumption, Fruit_Consumption, Green_Vegetables_Consumption e FriedPotato_Consumption.  


## Sobre as Métricas

Precision: Mede quantos dos indivíduos identificados como de alto risco realmente possuem doenças cardiovasculares. Alta precision significa que o modelo está focando nos casos mais prováveis de risco, reduzindo falsos positivos.

Impacto: Ajuda a evitar alarmes desnecessários, garantindo diagnósticos mais confiáveis para profissionais de saúde.

Recall: Avalia a proporção de indivíduos com doenças cardiovasculares corretamente identificados pelo modelo. Um recall elevado indica que o sistema é eficaz em não perder casos reais de risco.

Impacto: Essencial para maximizar a detecção de pacientes em potencial, contribuindo para intervenções precoces e maior alcance no cuidado preventivo.
