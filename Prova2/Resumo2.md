# Vetores

Estruturas de dados que permitem armazenar diversos valores em uma única variável.

## Declaração e inicialização de vetores

Para declarar um vetor basta especificar o tipo de variáveis que o vetor armazena (int, char, float, etc.), o nome do vetor (mesmas regras da declaração de variáveis simples) e quantos valores o vetor poderá armazenar. Exemplo:

```
int vet[5];
// Declara um vetor de inteiros com 5 posições
```

A quantidade de valores que um vetor armazena pode ser definida de forma estática, como no exemplo anterior, ou de forma dinâmica, declarando o vetor com uma variável entre colchetes '[ ]'. Exemplo:

```
int n;
scanf("%d", &n);

float vet[n];
// Declara um vetor de floats com n posições determinadas pelo usuário, dinamicamente
```

Vetores declarados de forma estática podem ser inicializadas com valores logo após sua inicialização colocando valores entre chaves '{ }', vetores declarados de forma dinâmica não podem ser inicializados desta forma. Exemplo:

```
int vet[5] = {1, 2, 3, 4, 5};
// Declara um vetor de inteiros com 5 posições, inicializando-o com os valores 1, 2, 3, 4 e 5
```
```
int n = 5;
int vet2[n] = {1, 2, 3, 4, 5};
// Declara um vetor de inteiros com n posições, levantará a exceção "variable-sized object may not be initialized" pois vetores declarados dinamicamente não podem ser inicializados, mesmo que a variável usada na declaração não seja dada por um usuário
```

Caso um vetor seja inicializado sem que todas as suas posições sejam preenchidas, como no exemplo anterior, as posições não declaradas serão preenchidas com o valor 0, isto vale para qualquer tipo de vetor, incluindo strings (o famoso \0 ou nulo na tabela ASCII). Exemplo:

```
int vet[5] = {};
// Declara um vetor de inteiros com 5 posições e o inicializa com todas as posições valendo 0

int vet[5] = {1, 2, 3};
// Declara um vetor de inteiros com 5 posições e o inicializa com os valores 1, 2, 3, 0, 0
```

