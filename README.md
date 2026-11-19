# Projeto Rank Lab

## Integrantes 
Leonardo Hiroshi Dondo de Freitas - RGM: 46610049

Rafael Marques de Oliveira - RGM: 47877081

## Descrição do Projeto
O RankLab é um programa em C que recebe 10 pontuações inteiras entre 0 e 100 e as ordena de três formas diferentes: Bubble Sort, Selection Sort e Insertion Sort. Além de ordenar, o programa conta quantas comparações cada método realizou, confere se os três chegaram ao mesmo resultado e mostra o menor valor, o maior valor e a mediana.

## Como o programa funciona
Exibe o cabeçalho do RankLab.

Lê as 10 pontuações. Se o valor estiver fora do intervalo de 0 a 100, ou não for um número, o programa avisa e pede novamente (sem avançar a posição).

Cria três cópias independentes do vetor original, antes de qualquer ordenação. Assim, cada algoritmo trabalha nos mesmos dados de partida.

Ordena cada cópia com um método e guarda o número de comparações devolvido por cada função.

Mostra o vetor original e os três vetores ordenados.

Verifica, com a função vetoresIguais, se os três resultados são iguais ("Resultados equivalentes: SIM/NAO").

Calcula menor, maior e mediana a partir do vetor ordenado. Como são 10 valores, a mediana é a média das posições 4 e 5.

Exibe a comparação de quantidade de comparações entre os três métodos.

## Funções
exibirCabecalho - Mostra o título do programa

lerPontuacoes - Lê e valida as 10 pontuações

copiarVetor - Copia um vetor para outro

exibirVetor - Imprime os elementos de um vetor

bubbleSort - Ordena com Bubble Sort e retorna o número de comparações

selectionSort - Ordena com Selection Sort e retorna o número de comparações

insertionSort - Ordena com Insertion Sort e retorna o número de comparações

vetoresIguais - Confere se dois vetores são iguais posição a posição

## Análise dos Resultados
Bubble Sort e Selection Sort fizeram sempre 45 comparações (n(n−1)/2 com n = 10), em qualquer um dos testes. O número de comparações deles não depende da ordem inicial dos dados.

Insertion Sort variou: 29 no teste principal, 26 com valores repetidos e 45 na ordem inversa. A ordem inversa é o pior caso, pois cada novo elemento precisa ser comparado com todos os anteriores.

Para vetores já ordenados ou quase ordenados, o Insertion Sort tende a ser o mais vantajoso (no melhor caso, faria apenas 9 comparações para 10 elementos).

Para valores repetidos, os três algoritmos ordenaram corretamente e o resultado foi o mesmo.

Em termos de comparações, nenhum método foi pior que o Insertion Sort em qualquer teste, mas todos têm complexidade O(n²) no pior caso. Para vetores grandes, seriam necessários algoritmos mais eficientes.

## Conclusão 
O projeto permitiu comparar, na prática, três algoritmos de ordenação simples. Todos produzem o mesmo vetor ordenado, mas o custo em comparações é diferente: Bubble e Selection são previsíveis, enquanto o Insertion Sort se adapta à ordem inicial dos dados.
