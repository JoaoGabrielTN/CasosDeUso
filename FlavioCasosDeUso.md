# Fase de fortificação dos territórios no início de uma jogada
## ESCOPO
- início da jogada de um jogador no war

## NÍVEL
- Fortificar o território do jogador que está com a vez

## ATOR
- Jogador

## INTERESSES E INTERESSADOS
- Jogador: deseja fortificar seu território no início de sua jogada/vez
- Sistema: Controla o fluxo do jogo
- Verificador de Regra (VR): Verifica se o jogador que está com a vez tem algum continente conquistado e se ele fez alguma troca

## PRÉ-CONDIÇÕES
- Precisa ser a vez do jogador

## GARANTIA DE SUCESSO
- O jogador adiciona tropas nos territórios conquistados por ele

### CONDIÇÃO DE SUCESSO PRINCIPAL
1. Sistema inicia a vez de um jogador;
2. Sistema verifica se o jogador possui troca;
3. Sistema verifica se o jogador possui continentes conquistados;
4. Jogador adiciona tropas nos territórios dominados por ele;
5. Encerra a fase de fortificação.

## Extensão
2. A - Se jogador possui troca, a troca será feita, adicionando o número de tropas que podem ser colocados
