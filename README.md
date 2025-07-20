# 📊 Análise de Resultados dos Modelos de Churn

## 📌 Introdução

Este projeto apresenta uma análise comparativa de três modelos de Machine Learning — **Random Forest**, **MLP** (Perceptron Multicamadas) e **XGBoost** — treinados para prever o **Churn de clientes**.

A avaliação foi realizada utilizando **validação cruzada com 3 folds**, garantindo uma análise robusta e imparcial da performance de cada modelo. Os modelos foram previamente treinados e salvos, sendo carregados neste notebook exclusivamente para fins de avaliação.

---

## 📈 Objetivos da Avaliação

Avaliamos os modelos com base nas seguintes **métricas e visualizações**:

- **Importância das Features**: Identificação dos principais preditores de Churn.
- **Relatório de Classificação**: Inclui métricas como **precisão**, **recall** e **F1-score**.
- **Curva ROC e AUC**: Avaliação da capacidade discriminativa dos modelos.
- **Estatística KS (Kolmogorov-Smirnov)**: Medida da separação entre distribuições de probabilidade.
- **Matriz de Confusão**: Visualização dos acertos e erros.
- **Análise de Quintis**: Avaliação da performance dos modelos em diferentes faixas de risco (probabilidade predita de Churn).

---

## 🔄 Estrutura de Validação Cruzada

A análise foi conduzida com base em 3 combinações de treino/teste:

- **Modelo 1**: Treinado em folds (2 + 3), testado em (1)
- **Modelo 2**: Treinado em folds (1 + 3), testado em (2)
- **Modelo 3**: Treinado em folds (1 + 2), testado em (3)

Para cada modelo, foram gerados os relatórios, gráficos e análises baseados em seu respectivo conjunto de teste.

---

## 📊 Resultados e Análise

### 🥇 Melhor Modelo: XGBoost

- **AUC e KS mais altos**, indicando excelente capacidade de distinção entre churners e não churners.
- **Performance consistente** entre os folds, demonstrando **robustez e generalização**.

### 🥈 Random Forest

- Resultados muito próximos ao XGBoost.
- Apresenta-se como **alternativa sólida**, especialmente se a interpretabilidade for uma prioridade.

### 🤖 MLP (Rede Neural)

- Desempenho razoável, porém **menos consistente** que os demais.
- Pode ser vantajosa em contextos onde relações não lineares são mais relevantes.

---

## 📉 Análise de Quintis

A análise por quintis confirmou a **eficácia dos modelos em ranquear o risco de churn**:

- **Q1 (menor probabilidade predita)** → Menor taxa de churn real
- **Q5 (maior probabilidade predita)** → Maior concentração de churn real

Essa segmentação permite **ações de retenção mais direcionadas e estratégicas**.

---

## ✅ Conclusão

Tanto o **XGBoost** quanto o **Random Forest** demonstraram ser **modelos robustos e confiáveis** para previsão de churn, com excelente desempenho em métricas clássicas e na análise de risco. O XGBoost se destacou levemente, sendo a melhor opção considerando performance média.

A consistência nos folds e a análise de quintis reforçam a **confiabilidade dos modelos** para aplicação prática em estratégias de retenção de clientes.

---
