# 📊 IA Gravidez de Risco — Descrição das Etapas do Projeto

## 📌 Visão Geral
Este documento descreve as etapas realizadas no desenvolvimento do projeto de classificação de risco na gravidez utilizando técnicas de mineração de dados e a ferramenta Weka. O objetivo é preparar, analisar e modelar os dados para identificar padrões que ajudem na predição de riscos gestacionais.

---

## 1. 🗂️ Coleta e Compreensão dos Dados
Nesta etapa foi realizada a compreensão inicial do dataset, incluindo:
- Identificação dos atributos disponíveis
- Análise do significado de cada variável
- Verificação do tipo de dado (numérico, categórico, etc.)
- Identificação da variável alvo (classe de risco)

📌 Objetivo: entender o contexto dos dados antes do processamento.

---

## 2. 🧹 Pré-processamento dos Dados
Etapa fundamental para garantir a qualidade dos dados utilizados no modelo.

### 2.1 Limpeza de dados
- Remoção de registros inconsistentes
- Tratamento de valores ausentes
- Correção de dados fora do padrão

### 2.2 Transformação
- Conversão de atributos categóricos quando necessário
- Normalização ou padronização de valores numéricos (quando aplicável)

### 2.3 Seleção de atributos
- Identificação de variáveis mais relevantes
- Remoção de atributos irrelevantes ou redundantes

📌 Objetivo: melhorar a qualidade e eficiência do dataset para modelagem.

---

## 3. 📊 Exploração e Visualização dos Dados
Utilizando recursos do Weka, foram realizadas análises visuais como:
- Distribuição dos atributos
- Relação entre variáveis
- Separação entre classes de risco
- Identificação de padrões iniciais

📌 Objetivo: entender o comportamento dos dados antes da modelagem.

---

## 4. 🤖 Modelagem (Classificação)
Nesta etapa foram aplicados algoritmos de aprendizado de máquina no Weka.

### Algoritmos utilizados (exemplo):
- J48 (Árvore de decisão)
- Naive Bayes
- Random Forest
- Normalize
- Descritive

### Processo:
- Separação dos dados em treino e teste
- Aplicação dos modelos
- Geração de previsões

📌 Objetivo: construir um modelo capaz de prever o risco na gravidez.

---

## 5. 📈 Avaliação dos Modelos
Os modelos foram avaliados com base em métricas como:
- Acurácia
- Matriz de confusão
- Precisão
- Recall
- F1-score

📌 Objetivo: identificar o modelo com melhor desempenho.

---

## 6. 📉 Visualização dos Resultados
Após a modelagem, foram analisados:
- Erros de classificação
- Comparação entre modelos
- Distribuição das previsões corretas e incorretas

📌 Objetivo: interpretar os resultados de forma clara e visual.

---

## 7. 🧠 Conclusão
O processo de mineração de dados permitiu identificar padrões importantes relacionados ao risco gestacional. O modelo final pode ser utilizado como apoio à análise médica, auxiliando na tomada de decisões mais rápidas e precisas.

---

## 📌 Ferramentas Utilizadas
- Weka
- Dataset tabular (CSV/ARFF)
- Técnicas de Machine Learning
- Métodos de pré-processamento de dados

---