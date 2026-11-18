Uma grande montadora localizada no Polo Industrial de Manaus (PIM)
gerencia um vasto armazém com $N$ tipos diferentes de componentes
eletrônicos. O sistema primário de separação de peças é eficiente, com
robôs autônomos que buscam os componentes necessários no armazém, com
base em sensores ópticos que identificam o tipo de peça, e os levam para
a esteira de triagem principal, onde são separados e enviados para a
linha de montagem.

Infelizmente, falhas nos sensores podem ocorrer. Nessas situações, a
fábrica conta com um protocolo de contingência: robôs de emergência
retiram componentes do armazém, um por vez, mas de forma completamente
"cega", sem identificar qual tipo de componente estão pegando até que
ele chegue à esteira de triagem principal. Com isso, em algumas
situações, os robôs podem retirar mais unidades de alguns componentes do
que o necessário.

A fábrica possui metas de produção que exigem $K_i$ unidades do
componente do tipo $i$. Atualmente, o estoque disponível no armazém
possui $C_i$ unidades do componente $i$.

O gerente de logística precisa saber: no pior cenário possível, qual o
número mínimo de componentes que os robôs devem retirar do armazém para
garantir que todas as exigências da linha de montagem sejam plenamente
atendidas? Se o estoque for insuficiente para garantir o cumprimento de
todas as metas, o sistema deve sinalizar a impossibilidade da operação
imprimindo $-1$.

## Entrada

A primeira linha contém um inteiro $N$
($1 \leq N \leq 2 \times 10^{5}$), o número de tipos de componentes.

A segunda linha contém $N$ inteiros $C_1, C_2, \dots, C_N$
($1 \leq C_i \leq 10^{4}$), representando a quantidade de estoque
disponível de cada componente.

A terceira linha contém $N$ inteiros $K_1, K_2, \dots, K_N$
($1 \leq K_i \leq 10^{4}$), representando a meta exigida para cada
componente.

## Saída

Imprima uma única linha contendo o número mínimo de retiradas
necessárias no pior caso para garantir todas as metas, ou $-1$ se for
impossível garantir o cumprimento das metas com o estoque atual.
