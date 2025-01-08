# Orcs Attack!

The orcs lived peacefully in the western forest for centuries. But now, humans have come, and they are cutting down the forest for farmland. The orcs don't mind sharing... But the Bishop's greedy taxes force the villagers to cut down more and more trees. With their homes threatened, the orcs attack to reclaim their land! But the Bishop has hired a deadly adventurer, who stands ready to expel the orcs by any means necessary.

This is a project in applying Goal Oriented Action Planning (GOAP) to simulate the autonomous behavior of several agents.

## Agents

![](https://github.com/jsfabiani/GOAP_Orcs_Attack-/blob/main/gifs/Villagers.gif)

**Villagers**: they are the village's citizens. They want to have enough food to survive and pay their taxes. Their actions are:
- Go To Village: if they're not doing anything else (or if they just came back from hiding in the castle), the villagers will roam around the village.
- Farm: the villagers farm the land to stock their houses or pay the bishop's taxes. The farms recharge automatically after being farmed.
- Return Food to House: when their houses are unstocked. They need to farm food first.
- Pay taxes: when the Bishop orders them. They need to farm food first.
- Cut Down Tree: if they need food and there isn't enough farmable land, the villagers will chop down trees to make arable soil.
- Plow Soil: once they have chopped down trees, the villagers may plow the soil to make new farms.
- Go To Castle and Hide in Castle: when the orcs attack, the villagers will take refuge in the castle.
  
![](https://github.com/jsfabiani/GOAP_Orcs_Attack-/blob/main/gifs/Orc.gif)

**Orcs**: they were here long ago. They will protect their forest. Their actions are:
- Wander Forest: they're happy to do this when not threatened.
- Attack Village: if the villagers cut down too many trees, the orcs will become enraged and attack until too many of their members have been killed.
- Burn Down Farm: when attacking the village, the orcs will burn down the farms made by cutting down trees and turn them back to soil.
- Plant Trees: when attacking the village, the orcs will plant new trees in the soil to replenish the forest.
- Fight Adventurers: if an orc is threatened by the adventurer, they will stand firm and fight... although they are no match for the adventurer's steel!
- Retreat to Forest: when the orcs are diminished after taking too many losses, they will retreat back to the forest, where they will wander and wait for reinforcements from nearby orc settlements.
  
![](https://github.com/jsfabiani/GOAP_Orcs_Attack-/blob/main/gifs/Bishop.gif)

**Bishop**: the ruler of the land, he wants to get money and influence in order to protect his subjects. His actions are:
- Enter Castle: when he has nothing better to do. He's too important to mingle with the peasants!
- Raise Taxes: the Bishop has too many expenses, so the treasurery depletes periodically. When it gets too low, he will raise his subject's taxes.
- Hire Adventurers: when the castle is flooded with refugees, he will hire an adventurer to deal with the problem.
- Pay Adventurers: the adventurer's services are expensive! And she's armed! You don't want to make armed people mad! Paying her after she completes her job is his top priority, but it will deplete the treasurery.
  
![](https://github.com/jsfabiani/GOAP_Orcs_Attack-/blob/main/gifs/Adventurer.gif)

**Adventurer**: a deadly mercenary from accross the sea, she wants to complete her contract and get paid by the bishop. Her actions are:
- Follow Orc: when she's been assigned a contract, she will go to the village and find an orc to fight.
- Kill Orc: after acquiring her target, the adventurer will ruthlessly dispatch it. She will, however, stop fighting when the orcs retreat.
- Demand payment: when she drives out the orcs, she will demand payment from the bishop, not fighting again until it is fulfilled.
- Go To Camp: when her job's done, the adventurer will go back to the camp and stand by for further orders.

## The main loop

The villagers are self-sustainable, farming enough to keep their houses stocked. When the Bishop raises taxes, they are forced to cut down trees to make new farms. This causes the orcs to be enraged, which promts them to attack the village. The villagers take refuge in the castle and the Bishop hires the Adventurer to protect the village. The Adventurer then kills two orcs, causing the remaining one to run away, and goes to the castle to demand payment. As the villagers return to their village and start to cultivate again, the Bishop pays the Adventurer, depleting the treasurery and making him raise taxes again. When the orcs are replenished, they will attack again, repeating the cycle.

![](https://github.com/jsfabiani/GOAP_Orcs_Attack-/blob/main/gifs/GameLoop.gif)

## Assets used
- Lowpoly Medieval Peasants - Free - MEDIEVAL FANTASY SERIES by Polytope Studio https://assetstore.unity.com/packages/p/lowpoly-medieval-peasants-free-medieval-fantasy-series-122225
- Lowpoly Medieval Priest - Free - MEDIEVAL FANTASY SERIES by Polytope Studio https://assetstore.unity.com/packages/3d/characters/humanoids/lowpoly-medieval-priest-free-medieval-fantasy-series-164796
- Lowpoly Modular Armors - Free - MEDIEVAL FANTASY SERIES by Polytope Studio https://assetstore.unity.com/packages/3d/characters/lowpoly-modular-armors-free-medieval-fantasy-series-199890
- Low Poly Barbarian - Fantasy Low Poly 3D by Shokubutsu https://assetstore.unity.com/packages/3d/characters/low-poly-barbarian-fantasy-low-poly-3d-by-shokubutsu-294938
- Fantasy Lowpoly Pack (Demo) by Black Rose Developers https://assetstore.unity.com/packages/3d/environments/fantasy/fantasy-lowpoly-pack-demo-301518
- Low Poly Farm Pack Lite by Just Create https://assetstore.unity.com/packages/3d/environments/industrial/low-poly-farm-pack-lite-188100
- Medieval Tent Big by kawetofe https://assetstore.unity.com/packages/3d/environments/historic/medieval-tent-big-19023
- All animations from Mixamo.
