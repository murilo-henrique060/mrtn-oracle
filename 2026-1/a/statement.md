Você foi contratado por uma empresa brasileira de HFT (*High Frequency
Trading*, ou negociação em alta frequência), que usa robôs para comprar
e vender ações na bolsa de valores em frações de segundo de forma
totalmente sistemática e automatizada. Sua primeira tarefa é implementar
um *sinal*: um número, calculado a partir do estado atual do mercado,
que orienta a decisão do robô entre comprar, vender ou não fazer nada. O
sinal que você vai calcular determina se naquele momento há mais demanda
de compra ou mais oferta de venda para uma ação.

Na bolsa, quem quer comprar ou vender ações registra um pedido no livro
de ofertas. O livro é formado por duas filas: pedidos de compra e
pedidos de venda. Os pedidos são agrupados em níveis de preço, ordenados
do melhor para o pior. Para cada nível $i$, são dados $c_i$ (total de
ações nos pedidos de compra) e $v_i$ (total de ações nos pedidos de
venda).

O sinal mede o desbalanceamento do livro para os primeiros $n$ níveis:
$$I_n = \frac{C_n - V_n}{C_n + V_n}, \qquad \text{onde } C_n = \sum_{i=1}^{n} c_i \text{ e } V_n = \sum_{i=1}^{n} v_i.$$

O valor de $I_n$ fica sempre entre $-1$ e $1$ e é interpretado da
seguinte forma:

- se $I_n > 0$, o sinal indica `COMPRA`;

- se $I_n < 0$, o sinal indica `VENDA`;

- se $I_n = 0$, o sinal indica `NEUTRO`.

Dado o livro de ofertas e uma série de consultas, em que a $j$-ésima
consulta possui profundidade $n_j$, informe o sinal correspondente a
cada consulta.

## Entrada

A primeira linha contém um inteiro $N$ ($1 \leq N \leq 10^{5}$), o
número de níveis do livro de ofertas.

Cada uma das $N$ linhas seguintes contém dois inteiros $c_i$ e $v_i$
($0 \leq c_i, v_i \leq 10000$), respectivamente o total de ações nos
pedidos de compra e de venda no nível $i$. É garantido que
$c_1 + v_1 > 0$.

A linha seguinte contém um inteiro $Q$ ($1 \leq Q \leq 10^{5}$), o
número de consultas. Cada uma das $Q$ linhas seguintes contém um inteiro
$n_j$ ($1 \leq n_j \leq N$), a profundidade da $j$-ésima consulta.

## Saída

Seu programa deve produzir $Q$ linhas. A $j$-ésima linha deve conter uma
única palavra: `COMPRA` se $I_{n_j} > 0$, `VENDA` se $I_{n_j} < 0$, ou
`NEUTRO` se $I_{n_j} = 0$.
