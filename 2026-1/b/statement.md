São dados $N$ intervalos de inteiros $[L_i, R_i]$, em uma ordem fixa.
Para cada índice $i$, deve-se escolher exatamente um inteiro $x_i$
pertencente ao $i$-ésimo intervalo, isto é, $L_i \leq x_i \leq R_i$.

Uma escolha é válida se a sequência $x_1, x_2, \dots, x_N$ for
estritamente crescente, ou seja, se $x_1 < x_2 < \dots < x_N$. Duas
escolhas são consideradas distintas se diferirem em pelo menos um valor
$x_i$.

Calcule o número de escolhas válidas, módulo $10^9 + 7$.

## Entrada

A primeira linha contém um inteiro $N$ ($1 \leq N \leq 300$).

Cada uma das $N$ linhas seguintes contém dois inteiros $L_i$ e $R_i$
($1 \leq L_i \leq R_i \leq 10^{9}$), descrevendo o $i$-ésimo intervalo.

## Saída

Imprima um único inteiro: o número de escolhas válidas, módulo
$10^9 + 7$.
