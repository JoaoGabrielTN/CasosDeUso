# **Nome do Caso de Uso**: Inicialização do Jogo

## **Nível**: 
- Objetivo do Usuário

## **Ator Principal**: 
- Jogador

## **Interessadoes e Interesses**
- Jogador : Deseja iniciar o jogo com seus territórios bem definidos.
- Sistema : Deseja imposibilitar dp jogador  adicionar tropas em terirorios inimigos
- Jogador : Deseja receber um objetivo bem definido e unico.
- Jogador : Deseja que exista uma maneira de decidir a ordem de quem vai jogar.
- Jogador : Deseja que tenha uma cor definida para se identificar e diferenciar dos demais jogadores.
- Jogador : Deseja adicionar tropas em seus territórios apos jogo começar.
- Jogador : Deseja que, após a fase de inicialização acabar, possa progesuir com fluxo do jogo.

## **Pré-condições**:
- Todos os jogadores estão presentes e prontos para iniciar.

## **Garantia de Sucesso**:
Todos os jogadores têm seus territórios definidos.
Cada jogador recebeu um objetivo específico.
A ordem dos jogadores para a rodada foi estabelecida.
Cada jogador tem uma cor definida para facilitar a identificação e 
tropas iniciais alocadas garantindo que a inicialização foi concluida
e o jogo está pronto para proxima fase.

## **Cenário de Sucesso Principal**: 
 - 1: jogadores estão prontos para iniciar o jogo 
 - 2: sistema define uma cor para cada jogador
 - 3: sistema define umm objetivo unico para cada jogador
 - 4: sistema define uma ordem para os jogadores fazerem suas jogadas
 - 5: sitema devide os teritorios do mapa igualmente entre os jogadores 
 - 6: sistema inicia o jogo
 - 7: jogadores adicionam suas tropas nos seus respectivos territorios
 na sua vez de jogar
 - 8: sistema verifica se todos jogadores fizeram suas jogadas então encerra turno inicial
## **Extensões**: 
- A. Número de Jogadores Não Definido
- descrição:O sistema não consegue identificar o número de jogadores
- 1 O sistema solicita que todos os jogadores confirmem sua presença.
- 2 Se algum jogador não estiver presente, o jogo não pode começar e o sistema aguarda até que todos estejam prontos.
- 3 Se o número de jogadores estiver abaixo do mínimo necessário, o sistema informa e aguarda até que o número adequado de jogadores esteja presente.
- B.Conflito de Cores
- descrição:Dois ou mais jogadores recebem a mesma cor
- 1 O sistema detecta a duplicidade e atribui uma nova cor aos jogadores afetados.
- 2 O sistema notifica os jogadores sobre a mudança de cor.
- 3 Atribui novas cores até que todas sejam únicas.
- C.Falha na Distribuição de Territórios
- descrição: O sistema não consegue distribuir os territórios igualmente entre os jogadores.
- 1 O sistema revisa a distribuição.
- 2 O sistema corrige e redistribui os territórios de forma que todos os jogadores recebam a quantidade correta.
- D. Objetivo Não Definido
- descrição :Um jogador não recebe um objetivo específico.
- 1 O sistema verifica se todos os jogadores têm objetivos.
- 2 Se um objetivo não for definido, o sistema gera um novo objetivo para o jogador afetado.
- 3  jogador é notificado sobre seu objetivo.
- E. Problema na Alocação de Tropas Iniciais
- descrição: jogador pode alocar em territorios inimigos
- 1 checa se a alocação do jogador foi valida
- 2 alocação foi invalida então dá oportunidade dele jogar novamente
- 3 imposibilita de alocar no territorio de outro jogador
## **Lista de variantes tecnlógicas e de dados**:
 - Um computador com sistema operacional
## **Frequência de ocorrência**:
 - Uma unica vez na partida 
## **problemas em aberto**:
- como identificar numero de jogadores?
- como inicializar tudo antes do jogo começar?
- como mudar sistema de distribuição de tropa apos inizialição?
 
