# **Nome do Caso de Uso**: Inicialização do Jogo

## **Nível**: 
- Objetivo do Usuário

## **Ator Principal**: 
- Jogador

## **Interessadoes e Interesses**
- Jogador : Deseja receber um objetivo bem definido e unico.
- Jogador : Deseja receber uma ordem de jogada para todos os demais jogadores.
- Jogador : Deseja receber uma cor para se identificar e diferenciar dos demais jogadores(branca,  vermelho, preto, azul, amarelo e verde).
- Jogador : Deseja receber territórios por sorteio de forma igulitaria .
- jogador : Deseja receber carta dos territorios atribuidos a ele.
- Jogador : deseja receber um soldado por territorio recebido na distribuição antes de iniciar jogo.
- Jogador : Deseja adicionar tropas em seus territórios apos jogo começar com base no seguinte calculo numero de territorios/2, com no minimo de 3 tropas.
- Jogador : Deseja que, após a fase de inicialização acabar, possa progesuir com fluxo do jogo.

## **Pré-condições**:
- Todos os jogadores estão presentes e prontos para iniciar.

## **Garantia de Sucesso**:
Todos os jogadores têm seus territórios definidos.
Cada jogador recebeu um objetivo específico.
cada jogador recebeu as cartas dos seus territorios
A ordem dos jogadores para a rodada foi pre-estabelecida.
Cada jogador tem uma cor definida para facilitar a identificação e 
tropas iniciais foram alocadas garantindo que a inicialização foi concluida
e o jogo está pronto para proxima fase.

## **Cenário de Sucesso Principal**: 
 - 1: jogadores estão prontos para iniciar o jogo 
 - 2: sistema define uma cor para cada jogador
 - 3: sistema define umm objetivo unico para cada jogador
 - 4: sistema define uma ordem para os jogadores fazerem suas jogadas
 - 5: sitema devide os teritorios do mapa igualmente entre os jogadores 
 - 6: sistema atribui cartas recefente aos territoririos recebidos por cada jogador
 - 7: sistema aloca uma tropa com a respectiva com de cada jogador em seu respectivo territorio 
 - 6: sistema inicializa o jogo
 - 7: jogadores adicionam suas tropas nos seus respectivos territorios
 na sua vez de jogar pre-estabelecida 
 - 8: sistema verifica se todos jogadores fizeram suas jogadas então encerra turno inicial
## **Extensões**: 
- 1 Número de Jogadores Não Definido
- descrição:O sistema não consegue identificar o número de jogadores
- a O sistema solicita que todos os jogadores confirmem sua presença.
- b Se algum jogador não estiver presente, o jogo não pode começar e o sistema aguarda até que todos estejam prontos.
- c Se o número de jogadores estiver abaixo do mínimo necessário, o sistema informa e aguarda até que o número adequado de jogadores esteja presente.
- 2 Conflito de Cores
- descrição:Dois ou mais jogadores recebem a mesma cor
- a O sistema detecta a duplicidade e atribui uma nova cor aos jogadores afetados.
- b O sistema notifica os jogadores sobre a mudança de cor.
- c Atribui novas cores até que todas sejam únicas.
- 4 Falha na Distribuição de Territórios
- descrição: O sistema não consegue distribuir os territórios igualmente entre os jogadores.
- a O sistema revisa a distribuição.
- b O sistema corrige e redistribui os territórios de forma que todos os jogadores recebam a quantidade correta.
- 5 Objetivo Não Definido
- descrição :Um jogador não recebe um objetivo específico.
- a O sistema verifica se todos os jogadores têm objetivos.
- b Se um objetivo não for definido, o sistema gera um novo objetivo para o jogador afetado.
- c  jogador é notificado sobre seu objetivo.
- 6 Problema na Alocação de Tropas Iniciais
- descrição: jogador pode alocar em territorios inimigos
- a checa se a alocação do jogador foi valida
- b alocação foi invalida então dá oportunidade dele jogar novamente
- c imposibilita de alocar no territorio de outro jogador
## **Lista de variantes tecnlógicas e de dados**:
 - Um computador com sistema operacional
## **Frequência de ocorrência**:
 - Uma unica vez na partida 
## **problemas em aberto**:
- como identificar numero de jogadores?
- como inicializar tudo antes do jogo começar?
- como mudar sistema de distribuição de tropa apos inizialição?
 
