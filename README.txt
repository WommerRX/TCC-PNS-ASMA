
# Predição de Asma com Aprendizado de Máquina (PNS 2019)

## Objetivo do Estudo

Este projeto tem como objetivo prever a ocorrência de asma com base em dados da Pesquisa Nacional de Saúde (PNS 2019), utilizando algoritmos de aprendizado de máquina. São analisados fatores sociodemográficos, ambientais e de saúde que podem influenciar a incidência da doença.

##  Metodologia

- **Base de dados**: Microdados da PNS 2019
- **Variável-alvo**: asma (1 = sim, 0 = não)
- **Modelos utilizados**: Random Forest, Regressão Logística, XGBoost
- **Pré-processamento**:
  - Seleção e renomeação de variáveis
  - Recodificação com base em dicionário
  - Tratamento de outliers (percentis 1%-99%)
  - Imputação de valores ausentes (KNN e moda)
  - Codificação one-hot
- **Métricas de avaliação**: Accuracy, Recall, Precision, F1-score, ROC-AUC
- **Bibliotecas**: pandas, numpy, sklearn, xgboost, matplotlib, seaborn, scipy

##  Estrutura da Pasta

| Arquivo                           | Descrição |
|----------------------------------|-----------|
| `dt_dados_pns.csv`               | Base com variáveis selecionadas e renomeadas da PNS 2019. |
| `dt_dados_pns_processados.csv`   | Base após imputações, codificação e limpeza. |
| `py_preprocessamento.py`         | Script de pré-processamento completo dos dados. |
| `nb_random_forest.ipynb`         | Modelo de Random Forest aplicado aos dados. |
| `nb_regressao.ipynb`             | Modelo de Regressão Logística. |
| `nb_xgboost.ipynb`               | Modelo de XGBoost. |
| `nb_tarefas.ipynb`               | Planejamento e tarefas do projeto. |
| `dt_dicionario_pns_original.xls` | Dicionário oficial da PNS 2019. |
| `dt_dicionario_variaveis_formatado.xlsx` | Dicionário adaptado com nomes e tipos das variáveis. |

##  `py_preprocessamento.py` – Resumo

Realiza:
- Seleção e renomeação de colunas da PNS 2019
- Recodificação de categorias
- Tratamento de outliers
- Imputação e codificação de dados
- Exporta dados limpos para modelagem

##  Convenções de Nomenclatura

- Prefixos de arquivos:  
  - `dt_` → dados  
  - `py_` → script Python  
  - `nb_` → notebook

- Prefixos de variáveis:  
  - `num_` → numéricas  
  - `catl_` → categóricas (baixa cardinalidade)  
  - `cath_` → categóricas (alta cardinalidade)  
  - `ord_` → ordinais
