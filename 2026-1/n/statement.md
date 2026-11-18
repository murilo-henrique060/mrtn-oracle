A Nlogônia está implementando um novo sistema de transmissão de dados
entre suas $N$ estações de pesquisa, numeradas de $1$ a $N$. A
infraestrutura da rede é econômica: existem exatamente $N-1$ cabos
bidirecionais interligando as estações, de modo que sempre existe um
único caminho simples entre qualquer par de estações.

Para garantir que as mensagens cheguem apenas a quem realmente faz parte
do trajeto, os engenheiros criaram um mecanismo baseado em chaves de
acesso:

1.  Cada estação de pesquisa receberá uma lista de chaves de acesso.

2.  Quando uma estação $u$ envia uma mensagem para outra estação $w$, a
    mensagem é assinada com todas as chaves que $u$ e $w$ possuem em
    comum.

3.  Uma estação $v$ só consegue ler e autorizar a passagem da mensagem
    se possuir todas as chaves usadas nessa assinatura. Caso duas
    estações não compartilhem nenhuma chave, qualquer estação da rede
    conseguirá ler a mensagem.

O comitê de segurança estabeleceu as seguintes regras para a
distribuição das chaves:

- *Autorização no caminho:* Toda estação $v$ que estiver no trajeto
  entre $u$ e $w$ (incluindo as próprias estações $u$ e $w$) deve
  possuir todas as chaves compartilhadas por $u$ e $w$.

- *Bloqueio fora do caminho:* Se uma estação $v$ não pertence ao trajeto
  entre $u$ e $w$, deve haver pelo menos uma chave compartilhada por $u$
  e $w$ que a estação $v$ não possua (impedindo que ela leia a
  mensagem).

- *Economia:* O catálogo global pode conter no máximo $2N$ tipos
  distintos de chaves em toda a rede.

Sua tarefa é ajudar a equipe de engenharia a definir quais chaves cada
estação deve receber para cumprir todas as exigências.

## Entrada

A primeira linha da entrada contém um único inteiro $N$
($2 \leq N \leq 1000$), representando o número de estações de pesquisa.

As $N-1$ linhas seguintes descrevem as conexões da rede. Cada linha
contém dois inteiros $u$ e $v$ ($1 \leq u, v \leq N$, $u \neq v$),
indicando que existe um cabo ligando diretamente as estações $u$ e $v$.
É garantido que a rede forma uma árvore.

## Saída

Na primeira linha, imprima um único inteiro $K$ ($0 \leq K \leq 2N$),
indicando o total de chaves distintas criadas. As chaves devem ser
identificadas por inteiros de $1$ a $K$.

Nas próximas $N$ linhas, descreva a lista de chaves de cada estação de
$1$ até $N$. A $i$-ésima dessas linhas deve começar com um inteiro $Q_i$
($0 \leq Q_i \leq K$) indicando a quantidade de chaves da estação $i$,
seguido por $Q_i$ inteiros distintos representando as chaves entregues à
estação $i$.

É garantido que existe pelo menos uma atribuição válida de chaves. Se
houver mais de uma, qualquer uma será aceita.
