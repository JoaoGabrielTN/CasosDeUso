# Povoar um Território Recentemente Conquistado

## **Descrição**:
- Este caso de uso descreve o processo em que o jogador vai povoar um terrítorio no momento em que ele conquista o território. O jogador é obrigado a povoar o território conquistado com no mínimo uma tropa e no máximo três tropas.

## **Escopo**: 
- A ação de povoar um terrítorio no momento em que ele for conquistado

## **Nível**: 
- Nível de Subfunção

## **Ator Principal**: 
- Jogador

## **Interessados e Interesses**: 
- **Jogador:** Deseja consolidar sua conquista alocando tropas adequadas ao território recém-conquistado para defender e manter a posição.
- **Sistema:**  Deve garantir que o jogador aloque corretamente o número de tropas, que seja no mínimo uma tropa e no máximo três.

## Pré-condições
- O jogador deve ter vencido o ataque e conquistado o território.
- O jogador deve ter tropas disponíveis para alocação.
- O sistema deve estar preparado para receber a entrada do jogador sobre a quantidade de tropas a serem alocadas.

## **Garantia de Sucesso (Pós condições)**: 
- O território conquistado está povoado com o número de tropas escolhido pelo jogador (mínimo de uma e máximo de três).
- O sistema atualiza o estado do jogo, refletindo a nova distribuição de tropas e o controle do território.
- O jogador continua o fluxo de jogo, avançando para as fases subsequentes ou encerrando sua jogada.

## **Condição de Sucesso Principal (Fluxo Básico)**:
1. Jogador conquista um território após vencer um ataque.
2. Sistema solicita ao jogador que aloque tropas no território recém-conquistado.
3. Jogador escolhe o número de tropas a alocar (entre uma e três).
4. Sistema atualiza o estado do jogo, povoando o território conquistado com as tropas escolhidas pelo jogador.
5. O fluxo de jogo retorna ao ponto em que o jogador pode realizar outras ações ou encerrar sua jogada.

## **Extensões**: 
- 1a. Jogador não conquistou o terrítorio
    1. Sistema verifica e não permite a alocação de tropas para o terrítorio atacado.
- 3a. O jogador possui apenas 2 tropas no território de ataque
    1. Sistema verifica e faz a alocação automatica, já que o jogador tem apenas uma tropa para ser alocada
- 3b. O jogador tenta alocar menos de uma ou mais de três tropas no território recém-conquistado.
    1. O sistema rejeita a entrada
