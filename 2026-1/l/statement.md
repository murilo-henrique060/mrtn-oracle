Yan está abrindo uma empresa de jogos! Sua primeira criação é um jogo de
quebra-cabeça em um labirinto, onde o jogador precisa alcançar a célula
objetivo no menor número de passos possível. O labirinto é representado
por uma grade $N \times M$ e possui diversos tipos de células:

- Células livres (`.`): por onde se pode caminhar livremente.

- Paredes (`#`): células bloqueadas pelas quais não se pode caminhar.

- Posição inicial (`*`): onde o jogador começa.

- Posição final (`F`): o objetivo a ser atingido.

- Paredes diagonais (`\` ou `/`): células com uma parede conectando dois
  cantos opostos. É sempre possível entrar em uma célula desse tipo, mas
  não se pode atravessar a parede diagonal, havendo restrição sobre para
  quais células vizinhas se pode caminhar a seguir.

  Mais especificamente, ao entrar em uma célula com parede diagonal, os
  movimentos possíveis dependem da orientação da parede:

  - Em uma célula `\`, é possível transitar entre cima e direita (`U`
    $\leftrightarrow$ `R`) ou entre baixo e esquerda (`D`
    $\leftrightarrow$ `L`).

  - Em uma célula `/`, é possível transitar entre cima e esquerda (`U`
    $\leftrightarrow$ `L`) ou entre baixo e direita (`D`
    $\leftrightarrow$ `R`).

- Interruptores (`X`): para cada parede diagonal, existe exatamente um
  interruptor correspondente que, quando acionado, inverte a orientação
  dessa parede (`\` torna-se `/` e vice-versa). Só é possível acionar um
  interruptor se você estiver sobre a célula dele.

O $k$-ésimo interruptor `X` (em ordem de leitura, linha por linha da
esquerda para a direita) está associado à $k$-ésima parede diagonal
(também em ordem de leitura).

É permitido andar nas quatro direções cardeais (`U`, `D`, `L`, `R`) ou
acionar o interruptor na célula atual (`X`). Cada uma dessas ações conta
como um movimento.

Yan quer que a fase final seja extremamente desafiadora! Ajude-o criando
um labirinto solúvel de dimensões $N \times M$ ($1 \leq N, M \leq 100$)
contendo no máximo $10$ paredes diagonais, de tal forma que o menor
número de movimentos necessário para resolvê-lo seja de pelo menos
$10^{5}$ passos.

## Entrada

Este problema não contém entrada.

## Saída

Imprima na primeira linha dois inteiros $N$ e $M$
($1 \leq N, M \leq 100$).

Nas próximas $N$ linhas, imprima uma cadeia de $M$ caracteres
representando cada linha do labirinto.

O labirinto deve conter exatamente uma célula `*` e exatamente uma
célula `F`. A quantidade de interruptores deve ser igual à quantidade de
paredes diagonais, e essa quantidade não pode exceder $10$.

O labirinto deve ser solúvel, e o menor número de movimentos necessário
para alcançar a posição final deve ser de pelo menos $10^{5}$.

Qualquer labirinto que satisfaça todas as condições será aceito.
