# Análise Inicial do Dataset

## Introdução

Antes da aplicação das técnicas de aprendizado de máquina, foi realizada uma análise exploratória inicial do dataset utilizando a ferramenta WEKA. Essa etapa teve como objetivo compreender a estrutura dos dados, identificar possíveis inconsistências e levantar hipóteses que orientassem as etapas posteriores de pré-processamento e modelagem.

O dataset utilizado representa informações clínicas relacionadas à gravidez de risco, contendo atributos numéricos e nominais associados às condições de saúde das gestantes.

---

# Estrutura do Dataset

O conjunto de dados possui atributos relacionados a fatores clínicos e comportamentais das pacientes.

## Atributos presentes no dataset

| Atributo                  | Tipo     |
| ------------------------- | -------- |
| idade                     | Numérico |
| pressao_arterial          | Numérico |
| glicose                   | Numérico |
| imc                       | Numérico |
| consultas_pre_natal       | Numérico |
| semanas_gestacao          | Numérico |
| frequencia_cardiaca_fetal | Numérico |
| nivel_estresse            | Numérico |
| fumante                   | Nominal  |
| diabetes                  | Nominal  |
| cor_favorita              | Nominal  |
| risco_gravidez            | Classe   |

O atributo `risco_gravidez` foi definido como classe principal do problema, sendo responsável pela categorização das gestantes em níveis de risco.

---

# Objetivo da Análise Inicial

A análise inicial teve como principais objetivos:

* verificar a qualidade dos dados;
* identificar valores faltantes;
* detectar possíveis ruídos e outliers;
* analisar a relevância dos atributos;
* observar padrões iniciais entre as variáveis;
* levantar hipóteses sobre o comportamento do dataset.

Essa etapa foi importante para orientar as decisões de pré-processamento aplicadas posteriormente.

---

# Observações Iniciais

Durante a exploração do dataset no WEKA, foram identificadas características importantes relacionadas à distribuição e consistência dos dados.

## Valores Faltantes

Foram encontrados valores ausentes representados pelo símbolo:

```text
?
```

Os valores faltantes apareceram principalmente nos atributos:

* glicose
* imc

A presença desses valores indica possíveis falhas no preenchimento de informações clínicas ou perda de dados durante a geração do dataset sintético.

Esses casos exigiram tratamento posterior para evitar impactos negativos nos algoritmos de aprendizado de máquina.

---

# Identificação de Possíveis Ruídos

A análise visual e estatística permitiu identificar registros considerados discrepantes em relação ao comportamento predominante do dataset.

## Exemplos identificados

| Atributo                  | Valor |
| ------------------------- | ----- |
| frequencia_cardiaca_fetal | 189   |
| pressao_arterial          | 248   |
| consultas_pre_natal       | 0     |

Esses valores foram considerados possíveis ruídos ou inconsistências, pois apresentaram comportamento distante da maioria das instâncias observadas.

A presença de ruídos no dataset foi proposital, permitindo avaliar como diferentes algoritmos lidam com dados imperfeitos.

---

# Identificação de Outliers

Também foram identificados possíveis outliers em atributos clínicos importantes.

Os principais casos observados foram:

* pressão arterial extremamente elevada;
* glicose acima dos padrões predominantes;
* frequência cardíaca fetal muito alta.

Esses registros foram analisados cuidadosamente, pois podem representar:

* erros;
* inconsistências;
* ou casos reais de gravidez de alto risco.

A equipe optou por manter parte desses registros para avaliar a robustez dos algoritmos frente a situações extremas.

---

# Análise dos Atributos

## Atributos Relevantes

Os atributos clínicos apresentaram forte relação com o problema estudado, especialmente:

* pressao_arterial;
* glicose;
* imc;
* diabetes;
* frequencia_cardiaca_fetal;
* nivel_estresse.

Esses atributos possuem relevância médica conhecida na identificação de complicações gestacionais.

---

## Atributo Irrelevante

O atributo:

```text
cor_favorita
```

foi considerado irrelevante para o problema de gravidez de risco, pois não possui relação clínica com condições gestacionais.

Sua inclusão no dataset foi intencional, permitindo avaliar o impacto de atributos irrelevantes no desempenho dos algoritmos de classificação.

---

# Distribuição dos Dados

A análise das distribuições mostrou que:

* a maior parte das pacientes apresenta níveis moderados de pressão arterial e glicose;
* poucos registros possuem valores extremamente elevados;
* existe concentração maior de pacientes classificadas como baixo e médio risco.

Esse comportamento indica possível desbalanceamento entre classes, situação comum em problemas da área da saúde.

---

# Relações Entre Variáveis

Durante a análise visual no WEKA, foram observadas relações importantes entre alguns atributos.

## Pressão arterial e risco gestacional

Pacientes com pressão arterial elevada apresentaram maior concentração na classe de alto risco.

---

## Glicose e diabetes

Foi observada relação entre níveis elevados de glicose e presença de diabetes gestacional.

---

## IMC e risco

Gestantes com IMC elevado apresentaram tendência a maior risco gestacional.

Essas relações indicam que os atributos clínicos possuem potencial preditivo relevante para os algoritmos de aprendizado de máquina.

---

# Hipóteses Levantadas

Com base na análise inicial, foram levantadas as seguintes hipóteses:

* atributos clínicos como pressão arterial, glicose e IMC possuem forte influência na classificação do risco gestacional;
* ruídos e outliers podem impactar negativamente alguns algoritmos;
* algoritmos robustos, como Random Forest, podem apresentar melhor desempenho em dados ruidosos;
* a normalização dos atributos pode beneficiar algoritmos baseados em distância;
* atributos irrelevantes podem reduzir a qualidade da classificação.

---

# Considerações Sobre Pré-processamento

A partir da análise inicial, foram definidas algumas necessidades para o pré-processamento:

* tratamento de valores faltantes;
* remoção de atributos irrelevantes;
* normalização dos atributos numéricos;
* análise dos outliers;
* identificação de padrões inconsistentes.

Essas etapas foram consideradas fundamentais para melhorar a qualidade dos dados e o desempenho dos modelos de aprendizado de máquina.

---

# Conclusão

A análise exploratória inicial permitiu compreender a estrutura do dataset e identificar problemas importantes presentes nos dados.

Foram identificados:

* valores faltantes;
* possíveis ruídos;
* outliers;
* atributo irrelevante;
* diferenças de escala entre atributos.

Além disso, foram observadas relações relevantes entre variáveis clínicas e o risco gestacional, indicando potencial para aplicação de técnicas de clustering e classificação.

As informações obtidas nessa etapa serviram como base para as decisões de pré-processamento e escolha dos algoritmos utilizados no restante do trabalho.
