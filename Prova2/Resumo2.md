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

## Valores de um vetor

Podemos acessar o valor de um vetor passando o nome do vetor e o índice do valor entre colchetes. Exemplo:

```
int vet[5] = {1,2,3,4,5};

printf("%d %d %d %d %d\n", vet[0], vet[1], vet[2], vet[3], vet[4])
// Imprime na saída padrão os valores guardados no vetor 'vet', ou seja, 1 2 3 4 5
// Lembrando que a primeira posição de um vetor tem índice 0
```

Um método mais eficiente para acessar os valores de um vetor é por meio das estruturas de repetição. Exemplo:

```
int vet[5] = {1, 2, 3, 4, 5}, j = 0;

for (int i = 0; i < 5; i++)
{
	printf("%d ", vet[i]);
}

printf("\n");

while (j < 5)
{
	printf("%d ", vet[i]);
	j++;
}

printf("\n");

// O while e o for neste código são equivalentes, ambos imprimirão na saída padrão:
// 1 2 3 4 5
```

Para armazernar valores vindos do usuário no vetor ainda usamos o scanf(), passando junto com o & o nome do vetor e o índice entre colchetes. Pode-se utilizar estruturas de repetição para obter vários valores também. Exemplo:

```
int vet[10];

for (int i = 0; i < 10; i++)
{
	scanf("%d", &vet[i]);
}

for (int i = 0; i < 10; i++)
{
	printf("%d ", vet[i]);
}

printf("\n");

// Obtem valores para cada posição do vetor e depois imprime esses valores
```

