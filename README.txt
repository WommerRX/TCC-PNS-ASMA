# 🧠 Predição de Asma com Inteligência Artificial  

**Trabalho de Conclusão de Curso (TCC)**  
Este projeto investiga o uso de técnicas de **aprendizado de máquina e redes neurais** para **predição de asma** a partir de dados populacionais e de saúde da **Pesquisa Nacional de Saúde (PNS 2019)**.  
O objetivo é comparar diferentes modelos de IA quanto ao desempenho preditivo e interpretar seus resultados sob a ótica da transparência e do problema da “caixa-preta” em IA aplicada à saúde.

---

## 📁 Estrutura do Projeto

| Tipo de arquivo | Nome | Descrição |
|-----------------|------|------------|
| **Dados brutos e processados** | `dt_pns2019.csv` | Base original da PNS 2019 utilizada para extração das variáveis. |
| | `dt_dados_pns.csv` / `dt_dados_pns_processados.csv` | Dados intermediários utilizados nas etapas de pré-processamento. |
| | `dados_preprocessados.csv` | Base final após limpeza, codificação e normalização das variáveis. |
| | `data_recodificado.csv` | Versão recodificada com variáveis categóricas transformadas para modelagem. |
| **Dicionários de variáveis** | `dicionario_de_variaveis_final_atualizado.xlsx` | Dicionário com descrição, tipo e codificação de cada variável usada. |
| | `dt_dicionario_pns_original.xls` | Dicionário original fornecido pelo IBGE. |
| **Divisão treino/teste** | `X_train.csv`, `X_test.csv`, `y_train.csv`, `y_test.csv` | Bases de treino e teste utilizadas nos modelos tradicionais. |
| | `X_test_keras.csv` | Conjunto de teste separado para modelos de rede neural (Keras). |
| **Modelos e hiperparâmetros** | `logreg_pipeline_trained.joblib` / `logreg_random_search.joblib` | Modelo de Regressão Logística treinado e busca de hiperparâmetros. |
| | `randomforest_pipeline_trained.joblib` / `randomforest_random_search.joblib` | Modelo Random Forest e resultados de otimização. |
| | `xgb_pipeline_trained.joblib` / `xgb_random_search.joblib` | Modelo XGBoost e parâmetros otimizados. |
| | `modelo_rn_keras.h5` | Modelo de Rede Neural salvo em formato Keras. |
| **Notebooks principais** | `nb_preprocessamento.ipynb` | Pré-processamento dos dados, tratamento de missing values e codificação. |
| | `nb_eda.ipynb` | Análise exploratória de dados (EDA) com estatísticas e visualizações. |
| | `nb_regressao_polinomial.ipynb` | Teste de modelo de regressão polinomial como baseline. |
| | `nb_random_forest.ipynb` | Treinamento e avaliação do modelo Random Forest. |
| | `nb_xgboost.ipynb` | Treinamento e avaliação do modelo XGBoost. |
| | `nb_rede_neural.ipynb` | Implementação e treinamento da rede neural com Keras. |
| | `nb_teste_modelos.ipynb` | Comparação de métricas de todos os modelos. |
| **Outros arquivos** | `README.txt` | Notas rápidas sobre a estrutura inicial. |
| | `.joblib` / `.h5` | Pesos e pipelines salvos para reuso e deploy. |

---

## ⚙️ Principais Tecnologias Utilizadas

- **Python 3.11**
- **Bibliotecas**:  
  `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `xgboost`, `keras`, `tensorflow`, `joblib`
- **Ambiente de execução**: Jupyter Notebook (.ipynb)

---

## 🧩 Fluxo do Projeto

1. **Pré-processamento (`nb_preprocessamento.ipynb`)**
   - Limpeza e recodificação das variáveis da PNS 2019  
   - Geração dos arquivos `dados_preprocessados.csv` e `data_recodificado.csv`

2. **Análise Exploratória (`nb_eda.ipynb`)**
   - Estatísticas descritivas, correlação entre variáveis e gráficos  
   - Identificação de possíveis preditores de asma

3. **Treinamento de Modelos**
   - `nb_regressao_polinomial.ipynb` → baseline  
   - `nb_random_forest.ipynb` e `nb_xgboost.ipynb` → modelos de árvore  
   - `nb_rede_neural.ipynb` → rede neural densa em Keras

4. **Validação e Comparação (`nb_teste_modelos.ipynb`)**
   - Métricas: AUC, precisão, recall, F1-score e acurácia  
   - Análise de importância das variáveis e discussão sobre interpretabilidade

---

## 📊 Resultados Esperados

- Identificação das variáveis sociodemográficas, ambientais e de saúde com maior impacto na probabilidade de asma.  
- Comparação de desempenho entre modelos lineares, baseados em árvores e redes neurais.  
- Reflexão sobre **transparência e interpretabilidade** dos modelos em saúde pública.

---

## 🧾 Licença e Citação

Este projeto é de uso acadêmico e pode ser reutilizado para fins educacionais, desde que citada a fonte:

> **Autor:** Henrique Ferrari Wommer s
> **Trabalho de Conclusão de Curso - Atitus-(2025)**  
> Tema: *Predição de Asma com Inteligência Artificial e Aprendizado de Máquina*  
