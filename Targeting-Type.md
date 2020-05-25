| targeting types | Description |
| :---: | :--- |
| Gold | Always attacks the enemy who has the largest amount of gold. |
| Balanced | Attacks the enemy based on who is close and weak according to the formula below. |
| Closest | Always attacks the closest enemy |
| Any | Attacks the next enemy in the player list |
| Player | Always attacks the next enemy player in the list, otherwise the closest enemy AI. |

An AI with the "Balanced" targeting type will attack the enemy with the lowest calculated weighting value according to the following formula:   
`weight = (target's gold) / 100 + (power of target's army) + (target's available peasants) + 2 * (distance to target)`  

The army power of a player is the sum of all of their units' [power values](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Unit-Power-Table).