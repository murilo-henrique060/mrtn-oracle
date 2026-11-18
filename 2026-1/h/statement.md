Uma rua possui $N$ semáforos, numerados de $1$ a $N$. Cada semáforo pode
estar em um de dois estados: fechado, representado por $1$, ou aberto,
representado por $0$.

Para preparar a rua para uma operação especial, foram instalados $M$
dispositivos de controle. Cada dispositivo atua sobre um trecho contínuo
da rua: ao ser ativado, ele alterna o estado de todos os semáforos
dentro de seu alcance. Assim, semáforos fechados são abertos, e
semáforos abertos são fechados.

O $i$-ésimo dispositivo afeta os semáforos cujos índices estão entre
$L_i$ e $R_i$, inclusive. Cada dispositivo pode ser ativado quantas
vezes forem necessárias.

É possível ativar os dispositivos de modo que todos os semáforos fiquem
abertos?

## Entrada

A primeira linha contém dois inteiros $N$ e $M$
($1 \leq N, M \leq 10^{5}$), representando, respectivamente, o número de
semáforos e o número de dispositivos de controle.

A segunda linha contém $N$ inteiros $v_1, v_2, \dots, v_N$
($v_i \in \{0, 1\}$), representando o estado inicial dos semáforos.

As próximas $M$ linhas descrevem os dispositivos. A $i$-ésima dessas
linhas contém dois inteiros $L_i$ e $R_i$
($1 \leq L_i \leq R_i \leq N$), indicando que o dispositivo $i$ afeta
todos os semáforos entre $L_i$ e $R_i$, inclusive.

## Saída

Imprima `YES` se for possível deixar todos os semáforos abertos, ou `NO`
caso contrário.
