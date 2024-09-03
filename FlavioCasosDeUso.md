# Fase de fortificação dos territórios no início de uma jogada
## ESCOPO
- Início da jogada de um jogador no war

## NÍVEL
- Fortificar o território do jogador que está com a vez

## ATOR
- Jogador

## INTERESSES E INTERESSADOS
- Jogador: Deseja fortificar seu território no início de sua jogada/vez
- Sistema: Controla o fluxo do jogo
- Verificador de Regra (VR): Verifica se o jogador que está com a vez tem algum continente conquistado e se ele pode trocar cartas

## PRÉ-CONDIÇÕES
- Precisa ser no início da jogada do jogador

## GARANTIA DE SUCESSO
- O jogador adiciona tropas nos territórios conquistados por ele

## CONDIÇÃO DE SUCESSO PRINCIPAL
1. Sistema inicia a vez de um jogador;
2. Sistema verifica se o jogador possui troca;
3. Sistema verifica se o jogador possui continentes conquistados;
4. Jogador adiciona tropas nos territórios dominados por ele;
5. Encerra a fase de fortificação.

## Extensões
- 2a: Se jogador possui troca
    1. Jogador realiza troca
    2. Aumenta o número de tropas do jogador
    3. Remove as cartas de troca usadas pelo jogador
    4. Aumenta o número de tropas a ser recebido na próxima troca
- 3a: Se jogador possui continentes conquistados
    1. Jogador coloca X (onde X é o número que cada continente possui caso um jogador domine ele) tropas nos territórios daquele continente
