# Estimativa de Preços de Imóveis - Boston Housing Dataset

## Introdução

Este ebook aborda o processo de modelagem de regressão para estimar os preços de imóveis em Boston. Serão utilizadas técnicas de machine learning para treinar modelos preditivos e avaliar seu desempenho.

O objetivo é fornecer um material detalhado sobre as etapas envolvidas na construção, treinamento, avaliação e otimização de modelos de regressão.

---

## Conjunto de Dados

O conjunto de dados utilizado é o **Boston Housing Dataset**, disponível na biblioteca Scikit-Learn. Este dataset contém informações sobre diversas características de imóveis em Boston, bem como o preço mediano desses imóveis.

- **Amostras**: 506
- **Atributos**: 14 (13 atributos de entrada e 1 atributo target)

### Exemplos de Atributos de Entrada:
- Taxa de criminalidade per capita por cidade
- Número médio de cômodos por habitação
- Proporção de área construída antes de 1940

### Atributo Target:
- Valor mediano das casas ocupadas pelo proprietário (em milhares de dólares)

Este é um problema de **regressão**, pois o atributo target é um valor contínuo. O objetivo dos modelos será predizer este valor com base nos atributos de entrada.

---

## Seleção das Técnicas de Modelagem

As técnicas de modelagem selecionadas para treinar os modelos de regressão foram:
- **Regressão Linear**: Modelo linear simples do Scikit-Learn.
- **Support Vector Regression (SVR)**: Baseado em Support Vector Machines.
- **Decision Tree Regression**: Modelo de árvore de decisão para regressão (XGBoost).

### Pressupostos dos Modelos:
- Aceitam apenas variáveis numéricas como entrada.
- Não trabalham nativamente com dados categóricos.
- Podem ter problemas com outliers.

---

## Separação entre Conjuntos de Treino e Teste

Foi utilizada uma separação padrão entre os conjuntos de treino e teste:
- **20% dos dados** destinados ao conjunto de teste.

A separação foi realizada com a função `train_test_split` do Scikit-Learn, utilizando uma semente aleatória (`random_state`) para garantir reprodutibilidade. 

### Conjuntos Resultantes:
- **X_train, y_train**: Conjuntos de treino.
- **X_test, y_test**: Conjuntos de teste.

O modelo será treinado no conjunto de treino e avaliado no conjunto de teste, evitando **overfitting** e garantindo uma boa generalização.

---

## Treinamento do Modelo de Regressão Linear

O primeiro modelo treinado foi uma **Regressão Linear** simples, importada do módulo `linear_model` do Scikit-Learn.

### Passos:
1. Inicialização do modelo.
2. Treinamento com o método `.fit()` usando os dados de treino (`X_train`, `y_train`).
3. Não foram ajustados hiperparâmetros, sendo utilizados os valores padrão.

O resultado é um modelo de **Regressão Linear treinado** e pronto para fazer predições.

---

## Próximos Passos

Os próximos passos do projeto incluem:
- Treinar os modelos de **SVR** e **Decision Tree Regression**.
- Avaliar o desempenho de cada modelo no conjunto de teste utilizando métricas como **MSE**.
- Comparar visualmente os resultados e erros de cada modelo.
- Realizar **otimização de hiperparâmetros** para melhorar o desempenho.
- Selecionar o melhor modelo final.

O modelo final poderá ser utilizado para realizar predições de preços de novos imóveis com base nas características de entrada disponíveis.

---

## Conclusão

Neste ebook, abordamos as etapas iniciais de modelagem de regressão para estimar preços de imóveis utilizando o Boston Housing Dataset. 

- Discutimos as técnicas selecionadas, pressupostos, separação do dataset e o treinamento inicial de um modelo básico de **Regressão Linear**.
- Os próximos passos incluem o treinamento de outros modelos, otimização e avaliação para determinar o modelo com melhor desempenho.

Este processo é fundamental em projetos de ciência de dados, garantindo a construção, avaliação e implantação dos melhores modelos preditivos.
