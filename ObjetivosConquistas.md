# Objetivos de Conquistas de Territórios

## **Descrição**:
- Este caso de uso aborda todos os objetivos relacionados a conquistas de territórios, ou seja, conquista de continentes informados na própria 'carta', ou conquista de territórios não especificados. Esses objetivos são entregues no início da partida, e quando alguém completar seu objetivo, a partida é finalizada. 
- Os objetivos de conquistas de territórios são:
1. **Conquistar na totalidade os continentes**:
    - América do Norte e África
    - Ásia e África
    - América do Norte e Oceania
    - Europa, América do Sul, e mais outro continente da escolha do jogador
    - Ásia e América do Sul
    - Europa, Oceania, e mais outro continente da escolha do jogador
2. **Conquista de territórios (não precisa ser de um continente específico)**:
    - 24 territórios da escolha do jogador
    - 18 territórios da escolha do jogador com pelo menos 2 exércitos em cada território
## **Escopo**:
- Partida de WAR.
## **Nível**:
- Objetivo do Usuário
## **Ator Principal**:
- Jogador
## **Interessados e Interesses**
- **Sistema**: Vai controlar o fluxo da partida, entregando cartas e finalizando partida
- **Jogador**: Busca a conclusão do objetivo a ele designado
- **Verificador de Regras (VR)**: Verifica se algum jogador já alcançou seu objetivo
- **Notificador**: Entrega os objetivos para cada jogador no início da partida, informa quando algum objetivo foi concluído (e quem o concluiu), e notifica o jogador caso seu objetivo tenha sido alterado (fluxo alternativo do objetivo de eliminação de jogador)
## **Pré-Condições**:
- Partida ser iniciada
## **Garantia de Sucesso**:
- Todos os jogadores recebem seus devidos objetivos no início.
- A partida será encerrada assim que um jogador conclua seu objetivo.
## **Condição de Sucesso Principal**:
1. Sistema distribui 1 carta de objetivo para cada jogador no início da partida
2. Notificador mostra o objetivo de cada jogador separadamente
3. Jogador vai realizar suas jogadas
4. Verificador de Regras vai verificar se a condição do objetivo foi atingida após cada jogada dos jogadores
5. Jogador (1) vai concluir seu objetivo
6. Verificador de Regras vai confirmar a conclusão do objetivo
7. Sistema bloqueia jogadas futuras de outros jogadores, encerrando a partida
8. Notificador informa o ganhador, seu objetivo e o encerramento da partida
## **Extensões**:
a. Jogador alvo é eliminado antes que o jogador a quem foi designado tal objetivo, elimine-o
  1. Sistema vai destribuir o objetivo de 24 territórios para o jogador
  2. Notificador vai notificar ao jogador a falha no objetivo primário
  3. Notificador vai mostrar novo objetivo designado ao jogador
b. Jogador alvo é o próprio jogador que recebeu o objetivo
  1. Sistema vai destribuir o objetivo de 24 territórios para o jogador
  2. Notificador vai notificar ao jogador a falha no objetivo primário
  3. Notificador vai mostrar novo objetivo designado ao jogador
c. Nenhum jogador conclui o objetivo (partida é encerrada precocemente)
  1. Jogadores vão solicitar fim da partida
  2. Verificador de Regras vai verificar solicitações dos jogadores
  3. Sistema bloqueia jogadas futuras de outros jogadores, encerrando a partida
  4. Notificador informa o ganhador, seu objetivo e o encerramento da partida