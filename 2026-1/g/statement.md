Uma sequência de DNA é representada por uma cadeia de caracteres $T$.
Também são conhecidos diversos genes, representados por cadeias de
caracteres e ordenados do mais relevante para o menos relevante. Os
genes são numerados sequencialmente, começando de 1.

São feitas $Q$ consultas. Cada uma delas delimita um trecho de $T$,
entre os índices $L_i$ e $R_i$, inclusive. Para cada consulta, o
objetivo é determinar o índice do gene mais relevante que ocorre
inteiramente como subcadeia desse trecho.

## Entrada

A primeira linha da entrada contém a cadeia $T$
($1 \leq |T| \leq 10^{5}$). A segunda linha contém o número $G$ de genes
($1 \leq G \leq 5 \times 10^{5}$). As próximas $G$ linhas contêm os
genes, do mais para o menos relevante, um por linha. Cada gene é uma
cadeia não vazia. É garantido que os genes são distintos e que a soma
$S$ dos seus comprimentos é de no máximo $5 \times 10^{5}$.

A linha seguinte contém o número de consultas $Q$
($1 \leq Q \leq 10^{5}$). Cada uma das próximas $Q$ linhas contém dois
inteiros $L_i$ e $R_i$ ($1 \leq L_i \leq R_i \leq |T|$), representando
os limites inclusivos da consulta.

Todas as cadeias contêm apenas as letras `A`, `C`, `G` e `T`.

## Saída

Para cada consulta, imprima o índice do gene mais relevante que ocorre
inteiramente no trecho correspondente do DNA. Se nenhum gene ocorrer
naquele trecho, imprima $-1$.
