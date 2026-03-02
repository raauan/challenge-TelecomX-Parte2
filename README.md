# 📊 Customer Churn Prediction - Telecom X Parte 2

## 📌 Sobre o Projeto

Este projeto foi desenvolvido como parte do desafio de Data Science proposto no programa **Oracle Next Education (ONE)**, realizado em parceria com a **Alura**.

O desafio consistiu na construção de um modelo preditivo capaz de identificar clientes com maior probabilidade de churn (evasão), utilizando dados da empresa fictícia Telecom X.

Os dados utilizados para a realização da Parte 2 do projeto TelecomX estão disponíveis em:
[https://raw.githubusercontent.com/raauan/challenge-TelecomX-Parte2/refs/heads/main/dados_tratados.csv] ou através de download no repositório.

---

## 🎯 Objetivo

O objetivo deste projeto é desenvolver um modelo de Machine Learning capaz de prever a probabilidade de churn de clientes, permitindo que a empresa antecipe ações de retenção e reduza perdas financeiras.

A evasão de clientes representa impacto direto na receita e aumenta o custo de aquisição de novos consumidores. Dessa forma, identificar clientes em risco é uma estratégia fundamental para sustentabilidade e competitividade do negócio.

---

## 🏢 Contexto de Negócio

Empresas de telecomunicações enfrentam alta competitividade e baixo custo de migração entre concorrentes. Nesse cenário, a retenção de clientes torna-se tão importante quanto a aquisição de novos consumidores.

Este projeto busca responder à seguinte pergunta:

> Quais clientes possuem maior probabilidade de cancelar seus serviços?

---

## 📊 Dataset

O conjunto de dados contém informações sobre clientes da Telecom X, incluindo:

- Dados demográficos (gênero, parceiro, dependentes, senioridade)
- Informações contratuais (tipo de contrato, método de pagamento)
- Serviços contratados (internet, suporte técnico, segurança online)
- Informações financeiras (cobrança mensal e total)
- Variável alvo: **Churn (0 = permanece, 1 = evasão)**

---

## 🔎 Metodologia

O projeto foi estruturado nas seguintes etapas:

### 1️⃣ Extração dos Dados e Análise Exploratória (EDA)
- Identificação de padrões de churn
- Avaliação de distribuição de variáveis
- Padronização dos dados
- Remoção de colunas irrelevantes
- Análise de correlações
- Análises direcionadas

### 2️⃣ Pré-processamento - Correlação e Seleção de Variáveis
- Tratamento de variáveis categóricas (One-Hot Encoding)
- Padronização para Regressão Logística
- Tratamento de valores ausentes
- Separação em treino e teste
- Insights iniciais

### 3️⃣ Modelagem
Foram avaliados dois modelos:

- **Regressão Logística**
- **Random Forest**

Ambos foram treinados com `class_weight="balanced"` para lidar com leve desbalanceamento da classe churn.

### 4️⃣ Avaliação
Foram utilizadas as seguintes métricas:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Curva ROC
- Curva Precision-Recall

---

## 🤖 Resultados

### 📌 Regressão Logística
- Maior Recall para churn
- Melhor desempenho em ROC-AUC
- Alta interpretabilidade

### 📌 Random Forest
- Maior Accuracy geral
- Boa capacidade de modelar relações não lineares

A análise das curvas ROC e Precision-Recall indicou que a **Regressão Logística apresentou desempenho superior na identificação de clientes em risco**, sendo mais adequada para estratégias de retenção.

---

## 📈 Principais Insights

Os principais fatores associados ao churn foram:

- 🔹 Baixo tempo de permanência (Tenure)
- 🔹 Contratos mensais (Month-to-month)
- 🔹 Valores mensais elevados
- 🔹 Serviço de internet Fiber Optic
- 🔹 Método de pagamento Electronic Check

Observou-se que fatores contratuais e financeiros têm maior impacto no churn do que variáveis demográficas.

---

## 🎯 Modelo Recomendado

Considerando o contexto de retenção de clientes, onde o custo de não identificar um cliente em risco é elevado, a **Regressão Logística foi escolhida como modelo recomendado para implementação inicial**, devido a:

- Maior Recall
- Melhor equilíbrio na Curva Precision-Recall
- Maior interpretabilidade

---

## 🚀 Próximos Passos

Possíveis evoluções do projeto:

- Implementação de um sistema de score de risco
- Ajuste de threshold para otimização estratégica
- Teste com modelos de Gradient Boosting
- Desenvolvimento de dashboard interativo (Streamlit ou Plotly)
- Criação de API para previsão em tempo real

---

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Seaborn

---

## 📌 Conclusão

O projeto demonstrou que é possível identificar padrões consistentes de churn a partir de variáveis contratuais e financeiras.

A combinação de análise exploratória, modelagem preditiva e interpretação estratégica permitiu transformar dados em recomendações práticas para retenção de clientes.

---

## 👨‍💻 Autor: Rauan Siqueira Pereira

Obs: em certas partes do projeto foi utilizado o auxílio da inteligência artifical do próprio Google Colab para transformação e explicação de erros em códigos.
