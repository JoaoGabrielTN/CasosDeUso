# Realizar de uma Jogada

## **Descrição**:
- Este caso de uso descreve o processo pelo qual um jogador realiza uma jogada no jogo WAR. A jogada envolve as seguintes fases: Primeiramente a fortificação, que utiliza as tropas recebidas da rodada + carta que o jogador pode ou não ter para trocar por tropas, Fase de ataque, na qual o jogador pode escolher em atacar ou não e Realocação das tropas, que o jogador também escolhe se ele quer realocar ou não. Um detalhe importante é que a primeira rodada contém apenas a fortificação inicial, não contém a sessão de ataque e nem de realocação. Depois dessa rodada, todas as outras vão conter as três sessões, respectivamente: Fortificação, ataque e realocação. No término da jogada, caso o jogador consiga conquistar pelo menos um único território na sessão de ataque, ele vai ganhar uma única carta. Para esclarecer as dúvidas, irei exemplificar com um mini resumo a seguir:
- **Primeira rodada** é dada apenas pela fortificação inicial.
- **As rodadas restantes:** Fortificação, ataque(opcional {jogador pode ou não atacar}) e realocação(opcional{jogador pode ou não realocar}).
- No término de cada jogada, com execeção da primeira rodada, é verificado se o jogador conquistou pelo menos um território para receber a carta, se sim, ele recebe a carta.

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
- O sistema garantiu que a primeira rodada consistiu apenas na fase de fortificação inicial, sem permitir ações de ataque ou realocação.
- O sistema garantiu que todas as rodadas subsequentes foram corretamente divididas e executadas nas três fases obrigatórias: fortificação, ataque e realocação. Cada fase foi conduzida em sua ordem correta, sem omissões ou desvio das regras do jogo.
- O sistema assegurou que o jogador conseguiu alocar exércitos conforme desejado, fortalecendo suas defesas em territórios estratégicos.
- Se o jogador realizou ataques durante sua jogada e teve sucesso, o sistema garantiu que os territórios inimigos foram corretamente conquistados e que os exércitos necessários foram movidos para esses novos territórios, expandindo o domínio do jogador de acordo com suas escolhas.
- Se o jogador realocou, o sistema garantiu que a realocação foi feita de acordo com as regras de realocação.
- O jogador que conquistou pelo menos um território ganha uma carta no final da jogada e isso foi atualizado dentro do controle de cartas do jogador.
## **Condição de Sucesso Principal (Fluxo Básico)**:
1. Sistema identifica que é a vez do jogador e inicia a sua jogada
2. Sistema calcula e atribui exécitos ao jogador com base no número de territórios controlados e bônus de continente
3. Jogador deve distribuir os exércitos recebidos entre seus territórios conforme sua estratégia
4. Sistema identifica que o jogador distribuiu todas as tropas e passa para a sessão de ataque
5. Jogador seleciona um terrítorio sob seu controle e escolhe um território inimigo adjacente para atacar
6. Sistema processa o ataque, utilizando a rolagem de dados para determinar o resultado
7. Sistema atualiza o controle do território atacado e move os exércitos do jogador para o território conquistado
8. Jogador escolhe passar para a fase de realocação
9. Sistema identifica e passa para a sessão de realocação
10. Jogador realoca as tropas
11. Jogador finaliza a sua jogada
12. Sistema finaliza a jogada
13. VR checa se o jogador conquistou um terrítorio para entregar a carta
14. Sistema passa a vez para o outro jogador
## **Extensões**: 
- 1a. A jogada atual é a primeira rodada.
    1. Sistema entrega apenas a fase de fortificação.
    2. Jogador distribui exércitos nos territórios controlados.
    3. Sistema encerra a jogada, sem fases de ataque ou realocação.
- 2a. O jogador possui um conjunto de cartas que deseja trocar por tropas.
    1. Jogador seleciona a opção de troca de cartas.
    2. Sistema valida o conjunto de cartas.
    3. Sistema entrega as tropas correspondentes e o jogador as aloca.
- 5a. O jogador opta por não iniciar nenhum ataque durante a fase de ataque.
    1. Jogador escolhe a opção de pular a fase de ataque.
    2. Sistema passa diretamente para a fase de realocação.
- 5b. O jogador tenta atacar com menos tropas do que o necessário.
    1. Sistema detecta a falta de tropas suficientes para o ataque.
    2. Sistema notifica o jogador e não permite o ataque.
    3. Jogador pode escolher outro ataque ou prosseguir para a realocação.
- 6a. O jogador realiza um ataque, mas não consegue conquistar o território.
    1. Sistema determina o resultado do ataque como mal sucedido.
    2. Jogador pode optar por realizar outro ataque ou prosseguir para a realocação.
- 10a. O jogador não tem tropas suficientes para realocar e tenta realocar.
    1. Sistema bloqueia essa ação.
- 10b. O jogador escolhe não realocar.
    1. Jogador escolhe a opção de pular a fase de realocação.
    2. Sistema encerra a jogada e passa o controle para o próximo jogador.
- 13a. O jogador conquistou pelo menos um território durante a jogada.
    1. Sistema determina que o jogador é elegível para receber uma carta. 
    2. Sistema faz o jogador receber uma carta.
- 13b. Sistema identifica que o jogador não conquistou pelo menos um terrítorio.
    2. Sistema determina que o jogador não é elegível para receber uma carta.
    3. Sistema encerra a jogada sem entregar nenhuma carta.
