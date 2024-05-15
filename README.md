# Contrato de operação: attackTerritory

## Operação: 
`attackTerritory(source: Territory, target: Territory)`
## Referências cruzadas
Caso de Uso: Atacar Território
## Pré condições:
- Um jogo War está ocorrendo (instância)
- Existem pelo menos duas instâncias de Jogador (Instância)    
- Existe uma instância de região (Instância) 
- Jogadores estão associados a pelo menos 1 território (relação estabelecida)
- Territórios estão delimitados por fronteiras (relação estabelecida)
- Territórios estão povoados com pelo menos um exército (Relação estabelecida)
- Fronteiras fazem fronteiras com pelo menos um território (relação estabelecida)
- Jogador possui pelo menos 2 exércitos em seu território de ataque (Relação estabelecida)
- Jogador ataca em um combate por meio da máxima quantidade possivel de exércitos disponíveis (Relação estabelecida)
- Jogador alvo defende em um combate por meio da máxima quantidade possivel de exércitos disponiveis no território defendido (Relação estabelecida)

## Pós condições:
- Foi criada uma instância de Combate (Criação instância)
