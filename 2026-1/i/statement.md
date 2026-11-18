Jaime é um porquinho-da-índia que está comemorando uma ocasião especial
e convidou muitas pessoas para a sua festa. Jaime tem $F$ amigos,
numerados de $1$ a $F$, e enviou convites para $N$ deles. Cada convite
pode incluir uma ou mais pessoas, indicando se apenas o amigo foi
convidado ou se ele pode levar outras pessoas, como sua família, por
exemplo.

Cada amigo convidado enviou uma das seguintes respostas:

- $\texttt{A}~a_i~t_i$: O amigo aceitou o convite. Seu grupo chegará no
  minuto $a_i$ e permanecerá na festa por $t_i$ minutos, saindo no
  minuto $a_i + t_i$.

- $\texttt{D}$: O amigo recusou o convite.

- $\texttt{T}~x_i$: A resposta é condicional. O amigo comparecerá se e
  somente se o amigo $x_i$ comparecer. Nesse caso, os dois grupos
  chegarão e sairão nos mesmos instantes.

Se uma resposta condicional depender de um amigo que recusou o convite,
de um amigo que não foi convidado ou de uma cadeia circular de respostas
condicionais, esse amigo não comparecerá.

Jaime precisa alugar cadeiras para a festa. Quando um grupo vai embora,
suas cadeiras ficam imediatamente disponíveis para grupos que chegam
naquele mesmo minuto. Determine o número mínimo de cadeiras que Jaime
deve alugar para que todas as pessoas presentes possam se sentar.

## Entrada

A primeira linha contém dois inteiros $F$ e $N$ ($1 \leq F \leq 10^{9}$,
$1 \leq N \leq \min(10^{5}, F)$), o número total de amigos de Jaime e o
número de convites, respectivamente.

Cada uma das próximas $N$ linhas contém dois inteiros $k_i$ e $p_i$
($1 \leq k_i \leq F$, $1 \leq p_i \leq 10^{5}$). Esses valores indicam
que o $i$-ésimo convite foi enviado ao amigo $k_i$ e inclui $p_i$
pessoas. Todos os valores $k_i$ são distintos.

Cada uma das próximas $N$ linhas contém a resposta ao convite
correspondente, na mesma ordem dos convites. Uma resposta tem um dos
seguintes formatos:

- $\texttt{A}~a_i~t_i$ ($1 \leq a_i \leq 10^{9}$,
  $1 \leq t_i \leq 10^{9}$): o amigo $k_i$ aceitou, chegará no minuto
  $a_i$ e permanecerá por $t_i$ minutos.

- $\texttt{D}$: o amigo $k_i$ recusou o convite.

- $\texttt{T}~x_i$ ($1 \leq x_i \leq F$): o amigo $k_i$ comparecerá se e
  somente se o amigo $x_i$ comparecer.

## Saída

Imprima um inteiro correspondente ao número mínimo de cadeiras que Jaime
deve alugar, que é também o número máximo de pessoas presentes
simultaneamente na festa.
