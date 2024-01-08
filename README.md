# SeriesTemporais_BolsadeValores_Yahoo
Este notebook mostra o estudo de Séries Temporais, ensinado no Curso Engenheiro de IA da DSA Academy.  Foi mostrado os calculos como SMA(simple moving averadge), MSD(moving standard deviation),VWAP(volume weighted average price) e RSI(INDICE DE FORÇA RELATIVA) 

Foi utilizado Transformer com Redes Neurais Recorrentes(LSTM E GRU), fazendo o TEMPORAL FUSION TRANSFORMER.

As bibliotecas utilizadas foram tensorflow, keras, sklearn, yfinance(do yahoo), ta

Foi criada uma função para extrair os dados com yfinance(https://finance.yahoo.com/)

Foi criada a função para engenharia de atributos onde se cria novas features, inclusive a variavel_alvo. 

Dividiu o dataframe extraido(apenas com as features criadas) para treino, validação e teste, no qual separou 85% para treino, 10% para validação e 5% para teste. 

A padronização dos dados foi feita com sklearn e a função STANDARDSCALER().

Foi feito o ajuste dos dados para serem aplicados no modelo de redes neurais recorrentes. 

A ARQUITETURA TEMPORAL FUSION TRANSFORMER UNE UMA PARTE COM TRANSFORMER E OUTRA COM RNN(LSTM E GRU)

Foi criada a função transformer_encoder , que é a função transformer em si.

Foi criada a função cria modelo, para unir o modelo transformer com a aplicação do LSTM E GRU, com cabeças de atenção, camadas, neuronios, dropout,etc.

O modelo foi compilado com a Função de erro 'mean squared error' amplamente utilizado em problemas de regressão e o otimizador Adam. 

O modelo foi treinado com 20 épocas. 

Foi extraido a previsão e feito a avaliação do modelo com a predição e o dataset de teste. 
A metrica utilizada foi tirar a raiz quadrada do erro quadratico medio (RMSE).
A pontuação foi de:0.019


QUANTO MENOR O ERRO, MELHOR. 

Confira como extraimos os valores de previsão de compra e venda de ações no notebook deste repositório. 
