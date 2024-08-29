# Fase de fortificação dos territórios no início de uma jogada
## 1 - 
### ESCOPO
- início da jogada de um jogador no war
### NÍVEL
- Fortificar o território do jogador que está com a vez
### ATOR
- Jogador
### INTERESSES E INTERESSADOS
- Jogador: deseja fortificar seu território no início de sua jogada/vez
- Verificador de Regra (VR): Verifica se o jogador que está com a vez tem algum continente conquistado e se ele fez alguma troca
### PRÉ-CONDIÇÕES
- Precisa ser a vez do jogador
### GARANTIA DE SUCESSO
- O jogador adiciona tropas nos territórios conquistados por ele
### CONDIÇÃO DE SUCESSO PRINCIPAL
- VR escolhe um jogador para começar;
- VR verifica se o jogador possui trocas disponíveis;
- Caso tenha, aumenta o número de trocas que o jogador pode colocar no território e aumenta o número de tropas na próxima troca;
- VR verifica se o jogador possui continentes conquistados, caso haja, o jogador pode colocar mais x tropas apenas no território daquele continente
- Jogador adiciona tropas nos territórios dominados por ele
- Encerra a fase de fortificação
