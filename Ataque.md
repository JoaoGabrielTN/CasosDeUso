# Fase de Ataque de territórios

## **Escopo**: 
- partida de war
## **Nível**: 
- Ataque dos territorios
## **Ator Principal**: 
- Jogador
## **Interesses e Interessados**
- **Jogador**: 
- Deseja escolher com qual territorio ele irá atacar.
- Deseja atacar territorio inimigo.
- Deseja que ao conquistar territorio inimigo o mesmo troque a cor para cor do atacante.
- Deseja que ao conquistar territorio inimigo consiga definir quantas tropas vão ser alocadas.
- **Verificador de Regra (VR)**: 
- Verifica se tem exercitos disponiveis para atacar.
- Verifica se o territorio que o atacante deseja atacar esta conectado ao atacante.
- Verifica caso de empate defesa ganha.
- Verifica caso vitoria a cor do país atacado seja a mesma do país atacante. 
- Verifica o numéro maximo e minimo de tropas que podem ser deixadas ao conquistar o territorio.
- **Sistema**: 
- Após dominio do territorio sistema pinta a cor do territorio. 

## **Pré-condições**:
- Conter no minimo 1 territorio dominado.
- Todas as tropas foram alocadas.
- Conter mais de uma tropa no país do atacante.

## **Garantia de Sucesso**:
- Conquista do território com atualização visual da cor e redistribuição das tropas conforme desejado pelo jogador.
## **Cenário de Sucesso Principal**:
1. Jogador escolhe com qual dos seus territorios deseja atacar.
2. Verificador de regra verifica se ele possui o territorio.
3. Verificador de regra verifica se ele pode atacar com esse territorio.
4. Jogador escolhe qual territorio irá atacar. 
5. Verificador de regra verifica se territorio inimigo esta ligado ao territorio escolhido.
6. Jogador domina territorio. 
7. Sistema pinta territorio dominado.
8. Verificador de regra verifica se o territorio dominado esta na cor correta.
9. Jogador escolhe quantas tropas vão ser alocadas ao territorio dominado.
10. Verificador de regra verifica o numéro maximo e minimo de tropas que podem ser alocadas
11. Jogador encerra ataque.
## **Extensões**:
- 2a: Jogador não possui o territorio 
    1. Sistema notifica que o jogador não possui o território selecionado
    2. Jogador escolhe outro territorio em sua posse.
- 3a: Jogador não pode atacar com esse territorio
    1. Sistema notifica que jogador não pode atacar com esse territorio
    2. Jogador escolhe outro territorio em sua posse.
- 5a: Territorio inimigo não esta ligado ao territorio do jogador
    1. Sistema notifica que jogador não pode atacar esse territorio
    2. Jogador escolhe outro territorio para atacar.
- 6a: Jogador não domina territorio
    1. Sistema notifica que jogador perdeu na disputa.
    2. Sistema faz a verificação de quantas tropas foram usadas.
    3. Sistema retira o numero de tropas usadas no ataque.
    4. Jogador decide se ataca novamente ou encerra ataque.
- 10a: Numero incorreto de tropas alocadas 
    1. Sistema notifica que jogador não pode colocar aquele numero de tropas.
    2. Jogador escolhe outro número de tropas.
## **Requisitos Especiais**:
## **Lista de variantes tecnlógicas e de dados**:
## **Frequência de ocorrência**:
## **Diversos**: