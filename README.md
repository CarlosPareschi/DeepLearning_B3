# Modelo de Compra e Venda de Ações usando Deep Learning

Este projeto consiste em um modelo de aprendizado profundo (deep learning) desenvolvido para prever se é mais provável que as ações BBAS3, CSNA3, PETR4 e VALE3 devam ser compradas ou vendidas com base em dados de imagens de gráficos de ações. O modelo utiliza uma arquitetura de rede neural convolucional (CNN) com uma camada Inception para extrair características importantes das imagens e uma camada densa para a classificação binária.

![Exemplo de Gráfico de Ações](https://github.com/CarlosPareschi/DeepLearning_B3/blob/main/images/2019-12-09_1.png)

A partir de agora explico como foi aplicado as técnicas para BBSA3, mas a abordagem foi a mesma nas demais, como os notebooks mostram.

## Dados

Os dados consistem em imagens de gráficos de ações da empresa BBAS3. As imagens foram divididas em conjuntos de treinamento e teste, sendo que cada ação tem uma pasta específica contendo subpastas de "comprar" e "vender", tanto para treinamento quanto para teste. Aqui está a distribuição das imagens para BBAS3:

Conjunto de Treinamento:
- BBAS3: 2088 imagens de "comprar" e 2655 imagens de "vender".

Conjunto de Teste:
- BBAS3: 496 imagens de "comprar" e 689 imagens de "vender".

## Pré-processamento de Dados

As imagens foram normalizadas e redimensionadas para o tamanho adequado antes de alimentar o modelo.

## Arquitetura do Modelo

O modelo utiliza uma arquitetura de rede neural convolucional (CNN) com uma camada Inception. A camada Inception é responsável por extrair características complexas das imagens através da combinação de diferentes filtros de convolução. A arquitetura do modelo inclui as seguintes camadas:

- Camada de Entrada: Aceita as imagens como entrada.
- Camadas Inception: Extrai características das imagens.
- Camadas de Pooling: Reduzem o tamanho das representações de características.
- Camadas Densas: Realizam a classificação binária.
- Camada de Saída: Produz a probabilidade de comprar ou vender.

## Treinamento do Modelo

O modelo foi compilado com a função de perda de entropia cruzada binária e otimizador Adam. Ele foi treinado por 10 épocas com um tamanho de lote de 32. Durante o treinamento, uma porcentagem dos neurônios foi aleatoriamente desligada (dropout) para evitar o overfitting.

## Avaliação do Modelo

O modelo foi avaliado com os dados de teste e obteve os seguintes resultados para a ação BBAS3:

- Acurácia BBAS3: 88.27%
- Precisão BBAS3: 80.31%
- Recall BBAS3: 95.36%

## Resultados

Os resultados mostram que o modelo é capaz de prever com precisão se a ação BBAS3 deve ser comprada ou vendida com base nos dados de imagem dos gráficos de ações.
