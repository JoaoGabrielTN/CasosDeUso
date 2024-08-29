# Caso de uso CDU*: Alocação de territórios ao fim da jogada
## **Descrição**:
Após cada fase de ataque, os jogadores podem distribuir tropas de territórios que possuem mais de 2 ou mais tropas para territórios seus territórios adjacentes.
## **Escopo**: 
- partida de war
## **Nível**: 
- alocação de tropas
## **Ator Principal**: 
- Jogador
## **Interessados e Interesses**:
- **Jogador**: deseja alocar as tropas ao fim da jogada em territórios disponíveis.
- **Verificador de regras (VR)**: verifica e garante que cada jogada está cumprindo com as regras do jogo.
## **Pré-Condições**: 
- Ter realizado a etapa de ataque.
## **Garantia de Sucesso**: 
- Jogador realiza as distribuições, disponíveis, de seu interesse.
## **Condção de Sucesso Principal**:
1. Jogador escolhe qual território irá movimentar suas tropas. (verificar se o território está em posse do jogador?)
2. VR checa se o território possui tropas para movimentar.  
3. Jogador escolhe a quantidade de tropas que deseja movimentar.
4. VR checa se o jogador escolheu uma quantidade válida de tropas para movimentar.
5. Jogador escolhe qual território irá receber as tropas.
6. VR checa se o território destino é válido.
7. Atualizar o número de tropas no território de origem e no território destino.
8. Jogador encerra a fase de alocação de tropas.
## **Extensões**:

- 2a VR identifica que o território não possui tropas válidas:
    1. O jogador é notificado que não há tropas suficientes
    2. O jogador seleciona outro território em sua posse
- 4a VR identifica que a quantidade de tropas é inválida:
    1. O jogador é notificado que a quantidade de tropas é inválida
    2. O processo de realocação de tropas reinicia
- 6a O VR indentifica que o território destino é inválido:
    1. O jogador é notificado que o território não é válido
    2. O jogador escolhe novo território
- 8a O jogador decide realocar tropas novamente:
    1. Retorna à etapa 1 do fluxo principal
## **Lista de variantes tecnológicas e de dados**:
## **Frequencia de ocorrência**:
## **Diversos**:


