Os tratadores de dragões de Dragolândia estão reorganizando um grande
terreno retangular, dividido em células quadradas de mesmo tamanho,
dispostas em $N$ linhas e $M$ colunas. Algumas células contêm
obstáculos, como montanhas e poços de lava, enquanto as demais células
são espaços livres, cada uma habitada por um dragão.

Para dar novos ares ao ambiente sem desorganizar a dinâmica do grupo, os
tratadores desenharam em um pergaminho mágico transparente a posição
atual de todos os dragões, de modo que cada célula livre do terreno
corresponda a uma marcação no pergaminho. Eles planejam realocar os
dragões usando esse mesmo pergaminho como molde. Para isso, os
tratadores podem manipular o pergaminho livremente sobre a mesa: podem
girá-lo em qualquer sentido ou até mesmo virá-lo ao contrário (olhando
pelo verso da folha transparente).

Uma nova disposição é considerada válida se o pergaminho se alinhar
perfeitamente aos limites originais do terreno e se todas as marcações
de dragões caírem exatamente sobre células livres. Obviamente, nenhum
dragão pode ser posicionado sobre um obstáculo.

Sua tarefa é calcular o número total de maneiras válidas de alinhar o
pergaminho ao terreno. Cada orientação física distinta do pergaminho é
contada como uma maneira diferente, mesmo que duas orientações façam as
marcações caírem exatamente sobre as mesmas células. A orientação
inicial, com o pergaminho sem ser girado ou virado, já conta como uma
maneira válida.

## Entrada

A primeira linha da entrada contém dois inteiros $N$ e $M$
($1 \leq N, M \leq 1000$), representando as dimensões do terreno.

As próximas $N$ linhas contêm $M$ caracteres cada, descrevendo o
terreno:

- O caractere '`.`' indica um terreno livre, onde um dragão habita.

- O caractere '`#`' indica um obstáculo.

## Saída

Imprima uma única linha contendo um número inteiro: a quantidade de
maneiras válidas de alinhar o pergaminho ao terreno.
