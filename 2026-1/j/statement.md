Empresas de telefonia alteraram recentemente a forma como operam. Como
você e seus dois colegas de equipe precisam treinar juntos para
maratonas de programação online, você deseja calcular quanto gastará
para contatá-los por telefone.

Existem ao todo $N$ empresas de telefonia, numeradas de 1 a $N$. Cada
empresa $U$ pode possuir múltiplas linhas de comunicação
**direcionadas**. Cada uma dessas linhas parte da empresa $U$ e alcança
todas as empresas de um intervalo $[L, R]$. O custo da comunicação varia
da seguinte forma: o custo para conectar a empresa $U$ à empresa $L$ é
$X$, à empresa $L+1$ é $X + K$, à empresa $L+2$ é $X + 2 \times K$, e
assim por diante, até a empresa $R$, para a qual o custo é
$X + (R - L) \times K$. Mais formalmente, o custo para conectar a
empresa $U$ à empresa $i$ ($L \leq i \leq R$) é $X + (i - L) \times K$.

O custo de um caminho é a soma dos custos das conexões que o formam. O
custo de uma chamada telefônica de uma empresa $U$ a outra empresa $V$ é
o menor custo entre todos os caminhos da empresa $U$ até a empresa $V$.
Um caminho pode não utilizar nenhuma linha de comunicação; portanto, o
custo de uma chamada de uma empresa para ela mesma é $0$.

Você usa os serviços da empresa 1, enquanto seus dois colegas de equipe
usam os serviços das empresas $A$ e $B$. Você precisa calcular o custo
total mínimo para ligar para ambos os seus colegas, isto é, a soma dos
custos mínimos das chamadas da empresa 1 às empresas $A$ e $B$. Vocês só
conseguem treinar se for possível ligar para ambos os colegas.

## Entrada

A primeira linha contém quatro inteiros $N$, $M$, $A$ e $B$
($1 \leq N \leq 10^{5}$, $1 \leq M \leq 10^{5}$, $1 \leq A, B \leq N$),
representando, respectivamente, o número de empresas, o número de linhas
de comunicação e os números das empresas de seus dois colegas. As
empresas $A$ e $B$ podem ser iguais entre si e também podem ser iguais à
empresa 1.

Cada uma das $M$ linhas seguintes contém cinco inteiros $U$, $L$, $R$,
$X$ e $K$ ($1 \leq U \leq N$, $1 \leq L \leq R \leq N$,
$0 \leq X \leq 10^{13}$, $-10^{8} \leq K \leq 10^{8}$), descrevendo uma
linha de comunicação que parte da empresa $U$ e alcança as empresas do
intervalo $[L, R]$. É garantido que $X + (R - L) \times K \geq 0$.

É possível que $U$ pertença ao intervalo $[L, R]$.

## Saída

Imprima uma única linha contendo um número inteiro representando o custo
total mínimo para ligar para ambos os colegas. Se não for possível ligar
para pelo menos um deles, imprima $-1$.
