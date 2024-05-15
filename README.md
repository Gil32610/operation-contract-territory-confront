# Contrato de operação: attackTerritory

## Operação: 
`attackTerritory(source: Territory, target: Territory)`
## Referências cruzadas
Caso de Uso: Atacar Território
## Pré condições:
- Um jogo War está ocorrendo (**Criação de instância**)
- Existem pelo menos duas instâncias de Jogador (**Criação de instância**)    
- Existe uma instância de região (**Criação de instância**) 
- Jogadores estão associados a pelo menos 1 território (**Relação estabelecida**)
- Territórios estão delimitados por fronteiras (**Relação estabelecida**)
- Territórios estão povoados com pelo menos um exército (**Relação estabelecida**)
- Fronteiras fazem fronteiras com pelo menos um território (**Relação estabelecida**)
- Jogador possui pelo menos 2 exércitos em seu território de ataque (**Relação estabelecida**)
- Jogador ataca em um combate por meio da máxima quantidade possivel de exércitos disponíveis (**Relação estabelecida**)
- Jogador alvo defende em um combate por meio da máxima quantidade possivel de exércitos disponiveis no território defendido (**Relação estabelecida**)
- 
## Pós condições:
- Foi criada uma instância comb de Combate (**Criação de instância**)
- comb foi associada a instância Jogador atacante
- comb foi associada a instância de Jogador defensor
- foi criada uma instância diceCon de DiceConfront (**Criação de instância**)
- diceCon foi associada a comb (**Relação estabelecida**)
- foi criada uma instancia de AttackDice attDice a partir de comb.númeroDeExércitosAtacantes (**Criação de instância**)
- foi criada uma  instância de DefenseDice defDice a partir de comb.númeroDeExércitosDefensores (**Criação de instância**)
- attDice foi associado a defDice (**Relação estabelecida**)
- diceCon.wins tornou-se attDice.wins (**Modificação de atributo**)
- diceCon.loss tornou-se defDice.loss (**Modificação de atributo**)
- diceCon foi associado a target (**Relação estabelecida**)
- diceCon foi associado a source (**Relação estabelecida**)
- target.armyQuantity tornou-se target.armyQuantity - diceCon.wins (**Modificação de atributo**)
- source.armyQuantity tornou-se source.armyQuantity - diceCon.losses (**Modificação de atributo**)
- target teve associação com targetArmy excluída (**Relação excluída**)
- Foi criada a(s) instância(s) targetArmy a partir de diceCon.losses (**Criação de instância**)
- target foi associado a targetArmy (**Relação estabelecida**)
- source teve associação com sourceArmy excluída (**Relação excluída**)
- Foi cirada a(s) instância(s) sourceArmy a partir de diceCon.wins (**Criação de instância**)
- source foi associado a sourceArmy (**Relação estabelecida**)