A empresa Charliebot negocia várias estratégias de investimento de alta
frequência na SBC (Sociedade de Bolsas Computadorizadas). A empresa se
preocupa muito com a latência de rede, pois quanto menor ela for, maior
será o retorno esperado das estratégias.

A rede de fibra óptica utilizada atualmente foi mapeada em $N$ pontos de
presença e $M$ links bidirecionais. Os sinais de compra e venda da
Charliebot se originam em seu data center (o ponto 1) e precisam chegar
à instalação de co-location da SBC (o ponto $N$). Para cada par $(i,j)$
de pontos de presença conectados diretamente, foi medida a latência
$f_{ij}$ em microssegundos.

O provedor de rede instalou recentemente uma rede de micro-ondas
bidirecional entre alguns pontos de presença e mediu sua latência em
$w_{ij}$ microssegundos. Com isso, surgiu uma nova opção para reduzir a
latência. Entretanto, essa rede é mais cara e o orçamento da Charliebot
permite contratar no máximo $K$ links de micro-ondas.

Como um link de micro-ondas pode ter que contornar o terreno em que foi
instalado, não há nenhuma garantia de que $w_{ij} < f_{ij}$. Além disso,
o provedor de rede garante que sempre será possível encontrar um caminho
na rede mesmo quando o orçamento para micro-ondas for 0.

Qual é a menor latência possível, em microssegundos, de fim a fim?

## Entrada

A primeira linha contém três inteiros $N$, $M$ e $K$
($2 \leq N \leq 10^{5}$, $1 \leq M \leq 2 \times 10^{5}$,
$0 \leq K \leq 10$).

Cada uma das $M$ linhas seguintes contém quatro inteiros $i$, $j$,
$f_{ij}$ e $w_{ij}$ ($1 \leq i, j \leq N$, $i \neq j$,
$1 \leq f_{ij} \leq 10^{9}$, $w_{ij} = -1$ ou
$1 \leq w_{ij} \leq 10^{9}$), descrevendo uma conexão direta entre os
pontos de presença $i$ e $j$ com latência $f_{ij}$ na fibra e $w_{ij}$
no canal de micro-ondas. Se $w_{ij} = -1$, não há canal de micro-ondas
naquela conexão. Cada par de pontos aparece em no máximo uma linha.

## Saída

Imprima uma única linha contendo um inteiro correspondente à latência
mínima, em microssegundos, entre o data center da Charliebot e a SBC,
usando no máximo $K$ links de micro-ondas.
