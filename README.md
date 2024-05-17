# Contrato de operação: attackTerritory

## Operação: 
`attackTerritory(source: Territory, target: Territory)`
## Referências cruzadas
Caso de Uso: Atacar Território
## Pré condições:
- Existe uma instância warGame de WarGame(**Criação de instância**)
- Existe uma instância jogador1 de Player (**Criação de instância**)    
- Existe uma instância jogador2 de Player (**Criação de instância**)
- jogador1 está associado a warGame (**Relação estabelecida**)
- jogador2 está associado a warGame (**Relação estabelecida**)     
- Existe uma instância reg de Region (**Criação de instância**)
- Existe uma instância source de Territory (**Criação de instância**)
- source está associado a jogador1 (**Relação estabelecida**)
- Existe uma instância target de Territory (**Criação de instância**)
- target está associado a jogador2 (**Relação estabelecida**)
- source.armyQuantity é maior que 2 (**Modificação de atributo**)
## Pós condições:
- Foi criada uma instância attackPhase de TerritoryConfrontPhase (**Criação de instância**)
- attackPhase foi associada a warGame (**Relação Estabelecida**)
- attackPhase foi associada a player1 (**Relação Estabelecida**)
- attackPhase foi associada a player2 (**Relação Estabelecida**)
- attackPhase.sourceArmyNumber tornou-se maxArmyNumber a partir do valor de source.armyQuantity (**Modificação de atributo**)
- attackPhase.targetArmyNumber tornou-se maxArmyNumber a partir do valor target.armyQuantity (**Modificação de atributo**)
- Foi criada uma instância diceCon de DiceConfront (**Criação de instância**)
- diceCon foi associado a attackPhase(**Relação Estabelecida**)
- Foi criada uma instância dice de Dice(**Criação de instância**)
- diceCon.wins teve seu valor alterado a partir de dice.faceNumber (**Modificação de atributo**)
- diceCon.losses teve seu valor alterado a partir de dice.faceNumber 
- target.armyQuantity teve seu valor alterado a partir de diceCon.wins (**Modificação de atributo**)
- source.armyQuantity teve seu valor alterado a partir de diceCon.losses (**Modificação de atributo**)

