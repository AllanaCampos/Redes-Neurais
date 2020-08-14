# Redes-Neurais
Este repositório contém os códigos implementados a partir de pseudocódigos encontrados no livro TAL, tais códigos foram implementados com intuito didático para introdução as redes neurais, onde foi feito uma comparação entre as redes neurais Adaline e Perceptron.
# Códigos
Os códigos para implementação encontram-se nas pastas com os nomes das redes neurais, onde está separado a implementação para treinamento da rede e para classificação das amostras.
# Treinamento
Para o treinamento das redes neurais, foram utilizados os arquivos na pasta ``` Dados-treinamento ```, cada treinamento utiliza apenas um arquivo de entrada e apresenta 6 arquivos de saída. Para que não haja erros no treinamento deve-se alterar o seguinte trecho de código de acordo com o arquivo de entrada:
```
if(split(split(lines[i],",")[4], 't').length == 2) resultado[i] = 1;
  else resultado[i] = -1;
```
Para arquivos de entrada que possuam ```setvers``` ou ```setvirg``` nos nomes deve-se utilizar a letra ```t``` no código anterior e para arquivos de entrada que possuam ```virgvers``` em seu nome deve-se utilziar a letra ```g```. 
Os resultados dos treinamentos encontram-se nas pastas ```Redes-neurais/Adaline/Adalinet/Resultados``` e ```Redes-neurais/Perceptron/Perceptront/Resultados``` os arquivos em tais pastas apresentam o peso das entradas das redes neurais, assim como o valor do bias, a seguir apresentam a validation accuracy, a trainning accuracy, fold accuracy e validation error; além de tais informações apresentadas, em resultados apresentam ainda duas pastas com o trainning accuracy e o trainning error.
# Classificação
Para a classificação das redes neurais foram utilizados os arquivos resultantes do treinamento e os arquivos da pasta ```Dados-classificação```. Para cada classificação foram utilizados 3 arquivos de entrada, dois dos arquivos encontrados no resultado do treinamento e um dos arquivos na pasta dos dados de classificação. Os arquivos devem representar o mesmo conjunto de dados, por exemplo para a classificação utilizando o arquivo ```cvirgvers15.txt``` deve-se utilizar os arquivos ```dados-plano-SL-SW-virgvers15.txt``` e ```dados-plano-PL-PW-virgvers15.txt```. Como saída são apresentados 8 arquivos que possuem os valores que foram determinados para cada classe.
Os resultados da classificação encontram-se nas pastas ```Redes-neurais/Adaline/Adalinec/Resultados``` e ```Redes-neurais/Perceptron/Perceptronc/Resultados```.
# Gráficos
Os gráficos na pasta ```Gráficos/Planos``` apresentam os resultados da classificação das redes neurais em um plano, considerando os valores de cada linha dos arquivos como um ponto no plano (x,y). Para a criação da reta no gráfico deve-se utilizar os resultados do treinamento das redes neurais, onde se consideram os pesos das redes e o valor do bias de forma que a reta fique igual a:
```
P1*x+P2*y+BIAS=0
```
Onde ```P1``` e ```P2``` são os pesos apresentados no resultado do treinamento.
O gráfico na pasta ```Gráficos/Gráfico4X4``` apresenta os valores das amostras utilizadas para treinamento e classificação no plano, onde cada característica é combinada com as outras em cada linha para uma visualização no plano dos dados.
