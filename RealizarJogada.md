# Realizar de uma Jogada

## **Descrição**:
- Este caso de uso descreve o processo pelo qual um jogador realiza uma jogada no jogo WAR. A jogada envolve as seguintes fases: Primeiramente a fortificação, que utiliza as tropas recebidas da rodada + carta que o jogador pode ou não ter para trocar por tropas, Fase de ataque, na qual o jogador pode escolher em atacar ou não e Realocação das tropas, que o jogador também escolhe se ele quer realocar ou não. Um detalhe importante é que a primeira jogada de cada jogador contém apenas a fortificação inicial, não contém a sessão de ataque e nem de realocação. Dito isso, o jogador inicialmente é obrigado a fortificar os territorios selecionados caso ele tenha pelo menos um território sob seu controle, depois disso ele pode atacar terrítorios adversários para expandir seu domínio e, finalizando a jogada, ele pode mover exércitos entre territórios. No término da jogada, caso o jogador consiga conquistar pelo menos um único território na sessão de ataque, ele vai ganhar uma única carta. Isso seria o resumo de como vai ser feito cada jogada. Para esclarecer as dúvidas, irei exemplificar com um mini resumo a seguir:
- Primeira jogada de cada jogador: é dada apenas pela fortificação inicial.
- As jogadas restantes: Fortificação, ataque(opcional {jogador pode ou não atacar}) e realocação(opcional{jogador pode ou não realocar}).
- No término de cada jogada, com execeção da primeira jogada de cada jogador, é verificado se o jogador conquistou pelo menos um território para receber a carta, se sim, ele recebe a carta.

## **Escopo**: 
- Todas as ações de controle de territórios e movimentações de exércitos que um jogador pode ou não realizar em seu turno.

## **Nível**: 
- Nível de objetivo do usuário

## **Ator Principal**: 
- Jogador

## **Interessados e Interesses**: 
- **Sistema:**  Deve garantir que a primeira jogada de cada jogador contém apenas a fortificação inicial, as jogadas posteriores a essa devem ser conectadas a partir de 3 sessões, que são, respectivamente: fortificação, ataque e realocação.
- **Jogador:** Deseja expandir seu domínio, conquistando territórios inimigos e fortalecendo suas defesas, com o propósito de alcançar o objetivo dado.
- **Verificador de Regra (VR):** Verifica se o jogador conquistou pelo menos um terrítorio, caso sim, recebe uma carta no final de sua jogada.

## Pré-condições
- O jogo deve estar em andamento e todos os jogadores devem ter sido inicializados com seus respectivos territórios e exércitos.
- O jogador deve ter pelo menos um território sob seu controle para que possa iniciar uma jogada.
- O jogador deve possuir exércitos disponíveis para alocação no início da jogada, sendo este número calculado com base em fatores como a quantidade de territórios e continentes controlados, e quaisquer bônus de cartas acumuladas.
- O jogador não pode ter alcançado o objetivo dado no inicio do jogo, caso ele tenha atingido o objetivo, o jogo é encerrado e a vitória é dada para o esse jogador.
- A fase anterior (fortificação inicial ou a jogada de um outro jogador) deve estar completamente encerrada e o sistema deve estar pronto para iniciar a nova jogada.

## **Garantia de Sucesso (Pós condições)**: 
- O sistema garantiu que a primeira jogada de cada jogador consistiu apenas na fase de fortificação inicial, sem permitir ações de ataque ou realocação.
- O sistema garantiu que todas as jogadas subsequentes foram corretamente divididas e executadas nas três fases obrigatórias: fortificação, ataque e realocação. Cada fase foi conduzida em sua ordem correta, sem omissões ou desvio das regras do jogo.
- O sistema assegurou que o jogador conseguiu alocar exércitos conforme desejado, fortalecendo suas defesas em territórios estratégicos.
- Se o jogador realizou ataques durante sua jogada e teve sucesso, o sistema garantiu que os territórios inimigos foram corretamente conquistados e que os exércitos necessários foram movidos para esses novos territórios, expandindo o domínio do jogador de acordo com suas escolhas.
- Se o jogador realocou, o sistema garantiu que a realocação foi feita de acordo com as regras de realocação.
- O jogador que conquistou pelo menos um território ganha uma carta no final da jogada e isso foi atualizado dentro do controle de cartas do jogador.
## **Condição de Sucesso Principal**:

## **Extensões**: 
