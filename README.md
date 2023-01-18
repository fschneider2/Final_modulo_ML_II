Projeto final do modulo Machine Learning 2

Curso DataScience - Growdev 

## Documentação

A ideia inicial do projeto é treinar um algoritmo classificatorio que consiga classificar palavras em formato de áudio.

Para isso foi gravado varios áudios de 4 palavras diferentes, testar, treinar, compilar e executar.

Na pasta audios_treinamento, temos 8 arquivos de cada classe, que servirão para terinar o algoritmo.

Na pasta audios_teste, temos 2 arquivos de cada classe, que servirão para testar a acuracia do algoritmo.

Nas pastas de gráficos, temos os gráficos para analise de cada classe. A analise visual foi útil para identificar o quão proximo cada arquivo era similar aos de sua mesma classe, afim de identificar problemas que poderiam prejudicar a acuracia do projeto.


## Funcionalidades

No arquivo trabalho final, você irá encontrar uma função cuja ação é:

- Montar o caminho com os arquivos de áudio.
- Criar uma lista com as classes, para posterior aplicação no DF.
- Uso da biblioteca pydub para abrir os arquivos. Ao abrir já realizo um tratamento, removendo os valores menos de 30 e maiores que -30, assim já removendo outliers de minha amostra.
- Sabendo da necessidade de que todos os arquivos tenham o mesmo tamanho, e com interesse de que os audios não perdessem informações, resolvi aplicar uma formula para pegar partes de cada arquivo.
    ###### Onde o tamanho do arquivo foi dividido por um valor, 4150**, e peguei partes desse audio, pulando pelo resultado da divisão. Por exemplo, um arquivo com 41500 informações, iria pegar so 4150 informações, pulando de 10 em 10.
 ** este valor de 4150 foi definido ao fazer um teste, que esta presente no arquivo Teste_melhor_value.ipynb.

- A função retorna um DF pandas.

- Após tratado os dados, chamo a função, crio o x e o y para treinamento e o x e y de teste.
- Utilizo a função scaler, para normalizar os dados entre -1 e 1, afim de aumentar a acuracia de meu algoritmo, isso é recomendado, pois minhas pesquisas mostram que o algoritmo KNN obtem melhores resultados com valores normalizados.


## Rodando os testes

- Testando com os arquivos de teste, o algoritmo conseguiu chegar em 50 % de acuracia. 
- Testando com os arquivos de treinamento, o algoritmo se mostrou funcional, com 100% de acerto.


## Aprendizados

O código se mostrou funcional, porém é necessario novos testes afim de melhorar a manipulação dos dados e obter melhor acuracia em arquivos que não passaram pelo treinamento. 

A utilização do algoritimo knn pode não ser a melhor opção, realizarei o mesmo projeto com rede neural artificial, estou estudando Keras afim de buscar melhores resultados.
