
***
List of 169 parameters which set the AI characters' personality, f.e. what troops to recruit or how many iron mines to build.

| Name | Value Type | Description |
| :--- | :---: | :--- |
| WallDecoration| Int32 | Wall decorations like flags, set up in the AIV file, can be defined with this value. 10 to 13 are flags, 8 is poured oil, 9 are burning flames, 14 are braziers, 15 are decorative skills, 22 are disease clouds. More is described in issue #616 |
| Unknown001 | Int32 |  |
| Unknown002 | Int32 |  |
| Unknown003 | Int32 |  |
| Unknown004 | Int32 |  |
| Unknown005 | Int32 |  |
| CriticalPopularity | 0 to 10000 | 10000 equals 100 popularity. Below this value, the AI sells more stuff than usual to get money. |
| LowestPopularity | 0 to 10000 | Below this value the AI sets taxes in steps to TaxesMin, and rations to 'extra rations' until it reaches 'HighestPopularity' again. |
| HighestPopularity | 0 to 10000 | Above this value the AI sets taxes back up until a stable 0 to -3 current popularity modifier is reached |
| TaxesMin | 0 to 12 | Minimum taxes allowed. 0 to 11 beeing the steps from +7 popularity to -24 popularity by taxes in the keep. | 
| TaxesMax | 0 to 12 | Maximum of Taxes allowed. 0 to 11 beeing the steps from +7 popularity to -24 popularity by taxes in the keep. |
| Unknown011 | Int32 |  |
| Farm1 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) | An array of farm slots, which the AI builds in the given sequence. |
| Farm2 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm3 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm4 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm5 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm6 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm7 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm8 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| PopulationPerFarm | Int32 | An array for values to setup buildings by current workers spawned. For each amount of available workers, one of the building type (variable name) is placed. Set this to 0 to get no buildings of that type. |
| PopulationPerWoodcutter | Int32 |  |
| PopulationPerQuarry | Int32 |  |
| PopulationPerIronmine | Int32 |  |
| PopulationPerPitchrig | Int32 |  |
| MaxQuarries | Int32 | An array of values for the maximum amount of buildings placed of the named type. Minimum is 1. For disabling a buildings type, set the PopulationPerBuilding for described type to 0 |
| MaxIronmines | Int32 |  |
| MaxWoodcutters | Int32 |  |
| MaxPitchrigs | Int32 |  |
| MaxFarms | Int32 |  |
| BuildInterval | Int32 | The gameticks between buildsteps. This is only considered <= 5000 gold |
| ResourceRebuildDelay | Int32 | The delay before the AI rebuilds destroyed resource buildings. |
| MaxFood | Int32 | Includes wheat. Applies to each kind of food seperatly. |
| MinimumApples | Int32 | Reserves that are only consumed if current popularity < LowestPopularity. If the AI has less than this amount it will prioritize buying the missing food. |
| MinimumCheese | Int32 |  |
| MinimumBread | Int32 |  |
| MinimumWheat | Int32 | If the AI has less than this amount, it will prioritize buying the missing wheat. |
| MinimumHop | Int32 | If the AI has less than this amount, it will prioritize buying the missing hops. |
| TradeAmountFood | Int32 | The amount of food, wheat or hops bought at once. Only one of these trades is made per gametick. |
| TradeAmountEquipment | Int32 | The amount of equipment for the armoury bought at once. Only one of these trades is made per gametick. |
| AIRequestDelay | Int32 | The time until an AI can request goods again after its request was accepted. |
| MinimumGoodsRequiredAfterTrade | Int32 | If the AI would have less than this amount of a good after sending them, it won't send them to the requesting player. |
| DoubleRationsFoodThreshold | Int32 | Above this value of food the AI will give double rations out. |
| MaxWood | Int32 |  |
| MaxStone | Int32 | maximum amount of stone to store in the stockpile + the amount of the biggest unbuild Stonebuilding that hasn't been reached in the buildorder of the AIV. |
| MaxResourceOther | Int32 | maximum amount of hops, iron, pitch and flour to store in the stockpile. |
| MaxEquipment | Int32 | Maximum amount of weapons or armour stored in the armoury. |
| MaxBeer | Int32 |  |
| MaxResourceVariance | Int32 | allowed tolerance for all goods before AI sells back to max allowed stock |
| RecruitGoldThreshold | Int32 | A (gold) threshold which disables any recruitment and buying of ressources for aiv buildings or economy below it. Sortie units, ressource buildings and defensive siegeengines are excluded. |
| BlacksmithSetting | [BlacksmithSetting](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Workshop-Settings) |  |
| FletcherSetting | [FletcherSetting](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Workshop-Settings) |  |
| PoleturnerSetting | [PoleturnerSetting](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Workshop-Settings) |  |
| SellResource01 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | Array of resources sold immediately back to 0 |
| SellResource02 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Hop |
| SellResource03 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Iron |
| SellResource04 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Pitch |
| SellResource05 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Wheat |
| SellResource06 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Beer |
| SellResource07 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Flour |
| SellResource08 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Bows |
| SellResource09 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Crossbows |
| SellResource10 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Spears |
| SellResource11 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Pikes |
| SellResource12 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Maces |
| SellResource13 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually Swords |
| SellResource14 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually LeatherArmors |
| SellResource15 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) | usually IronArmors |
| DefWallPatrolRallyTime | Int32 | The amount of time for castle patrols, set up in the AIV, to move from one rally point to the next. (Remark: Only spearmen, horse archers and macemen currently do) |
| DefWallPatrolGroups | Int32 | The amount of concurrent existing patrol groups of, in the AIV setup castle patrols per unit type |
| DefSiegeEngineGoldThreshold | Int32 | Positive values, will give the AI, if at > 0 gold, the possibility to setup defensive siegeengines for almost free (spending its entire remaining gold, cheating the missing gold if it doesnt have sufficient funds). Negative values will make the AI require to have at least the values amount of gold before spending gold on siegeengines setup in the AIV |
| DefSiegeEngineBuildDelay | Int32 | The delay before the AI builds/rebuilds in the AIV placed siegeengines, after their spots are free or supporting Towers are build. |
| Unknown072 | Int32 |  |
| Unknown073 | Int32 |  |
| RecruitProbDefDefault | Int32 | The probability with which this AI changes its recruited type into defensive troops on the recruitment state change. Note: Sortie units are always recruited first! The AI starts the game always with defensive recruitment state. Until the AIV is completely build, defensive recruitment state has a higher probability by a high offset if above 0. |
| RecruitProbDefWeak | Int32 |  |
| RecruitProbDefStrong | Int32 |  |
| RecruitProbRaidDefault | Int32 | defensive, raid and attack probabilities for one strength state (weak/default/strong) should sum up to 100, as they are set in percentiles. |
| RecruitProbRaidWeak | Int32 |  |
| RecruitProbRaidStrong | Int32 |  |
| RecruitProbAttackDefault | Int32 |  |
| RecruitProbAttackWeak | Int32 |  |
| RecruitProbAttackStrong | Int32 |  |
| SortieUnitRangedMin | Int32 | These units are only sent out if at least this amout of them has already been recruited. More than the set amount can be recruitet if the AI looses resource building workers frequently. |
| SortieUnitRanged | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of ranged units that go to the last attacked farm or building, and guard it until another is attacked. |
| SortieUnitMeleeMin | Int32 | These units are only sent out if this amout of them has already been recruited. |
| SortieUnitMelee | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of melee units to attack enemy units shooting at the AI's buildings or workers. |
| DefDiggingUnitMax | Int32 | Amount of units that dig own moat. |
| DefDiggingUnit | [DiggingUnit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of unit to dig own moat. |
| RecruitInterval | Int32 |  |
| RecruitIntervalWeak | Int32 | The 'weak' state sets in if the AI is completely trashed. F.e. troops < 8, gold < 200, population < 15, ... |
| RecruitIntervalStrong | Int32 | The 'strong' state sets in if f.e. the AI has troops >= 40, gold >= 200, population >= 40, ... |
| DefTotal | Int32 | The total count of all defensive units (wall defense + patrols). If the AI is in its 'strong' state, it can overproduce defensive units and put them into the patrols group, if any patrols group is set. |
| OuterPatrolGroupsCount | Int32 | The number of splits for outer defensive patrols. |
| OuterPatrolGroupsMove | Bool | Whether the patrols stay at one place (quarry) or move around. |
| OuterPatrolRallyDelay | Int32 | The delay after which the AI sends out patrols to defend the outer economy. 4 is approximately one month, 24 being half a year. |
| DefWalls | Int32 |  |
| DefUnit1 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| DefUnit2 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| DefUnit3 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| DefUnit4 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| DefUnit5 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| DefUnit6 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| DefUnit7 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| DefUnit8 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnitsBase | Int32 | Base amount of raid troops, Special case: [unknown trigger => end result multiplied by 1.25] |
| RaidUnitsRandom | Int32 | Maximum random addition to raid troops. Special cases: [gold > 5000 => multiplied by 2][gold < 1000 => set to 0][enemy gold < 500 => divided by -2] |
| RaidUnit1 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnit2 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnit3 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnit4 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnit5 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnit6 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnit7 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| RaidUnit8 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| HarassingSiegeEngine1 | HarassingSiegeEngine |  |
| HarassingSiegeEngine2 | HarassingSiegeEngine |  |
| HarassingSiegeEngine3 | HarassingSiegeEngine |  |
| HarassingSiegeEngine4 | HarassingSiegeEngine |  |
| HarassingSiegeEngine5 | HarassingSiegeEngine |  |
| HarassingSiegeEngine6 | HarassingSiegeEngine |  |
| HarassingSiegeEngine7 | HarassingSiegeEngine |  |
| HarassingSiegeEngine8 | HarassingSiegeEngine |  |
| HarassingSiegeEnginesMax | Int32 | The maximum of harassing siege engines an AI builds. Capped at 10. |
| RaidRetargetDelay | Int32 | Might bug out ranged units when too low, this is the time raid units take until they get new instructions |
| AttForceBase | Int32 | The base amount of troops with which this AI attacks |
| AttForceRandom | Int32 | The maximum random amount of additional troops in an attack (this is not the amount by which the troops increase per attack!) |
| AttForceSupportAllyThreshold | Int32 | If the AI has more than this amount of units in the attack force, it will help their allies or siege an enemy if commanded to do so. |
| AttForceRallyPercentage | Int32 | The %-amount of units of the attack force that the AI will rally before attacking. (0 - 100) |
| Unknown129 | Int32 |  |
| AttAssaultDelay | Int32 | A delay for the main army attack, while siege engines are active. |
| AttUnitPatrolRecommandDelay| Int32 | The amount of gameticks, until the Attackunit patrol get issued a new command for patroling around the enemy's keep/castle |
| Unknown132 | Int32 | The delay until the main army gets a new command, mainly visible when a lord got killed, the army might retreat faster from the conquered location. |
| SiegeEngine1 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine2 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine3 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine4 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine5 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine6 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine7 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine8 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| CowThrowInterval | Int32 | The amount of stones needed to be thrown until the AI throws a diseased cow instead (catapults & trebuchets). Value 0 disables cows and -1 makes the AI not throw any bolders, only cows. |
| Unknown142 | Int32 |  |
| AttMaxEngineers | Int32 |  |
| AttDiggingUnit | [DiggingUnit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | This unit is only recruited if the target enemy has moat and used preferably to dig enemy moat. |
| AttDiggingUnitMax | Int32 |  |
| AttUnitVanguard | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of unit, that engages the enemy walls and traps before the main army moves in |
| AttUnitVanguardMax | Int32 |  |
| AttMaxAssassins | Int32 |  |
| AttMaxLaddermen | Int32 |  |
| AttMaxTunnelers | Int32 |  |
| AttUnitPatrol | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Ranged attack unit that patrols around the enemy castle / keep. Preferably ranged units should be used here. |
| AttUnitPatrolMax | Int32 |  |
| AttUnitPatrolGroupsCount | Int32 | # of groups the AttUnitPatrol split into. BUGGY! More than 1 group results to only a single group attacking, the others standing idle. |
| AttUnitBackup | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Attacking unit that holds position and doesn't attack until the walls are breached. |
| AttUnitBackupMax | Int32 |  |
| RangedBackupGroupsCount | Int32 | # of groups the RangedBackupUnits split into. If shields are present in the army, one will be added to each group (if possible). |
| AttUnitEngage | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Units that engage enemy groups of units outside the castle. Prioritizes larger groups no matter where they are on the map. Otherwise destroys buildings outside the castle. |
| AttUnitEngageMax | Int32 |  |
| AttUnitSiegeDef | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | These units patrol between siege enginees in order to protect them. Get priority in attackunit recruitment process. |
| AttUnitSiegeDefMax | Int32 |  |
| AttUnitSiegeDefGroupsCount | Int32 | # of groups the AttUnitSiegeDef split into. |
| AttUnitMain1 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | AttUntiMain1 to AttUnitMain4 is a list of the main strike force the AI recruits for sieges. Priotizes in order of the list, but only recruits untis for which they have enough gold. So try to place expensive units higher up. |
| AttUnitMain2 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| AttUnitMain3 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| AttUnitMain4 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| AttMaxDefault | Int32 | The maximum amount of units produced of AttUnitMain, until all other troop type maximums have been filled out. Only after, or when unable to produce the other units, the AI will fill up the main army with more AttMainUnit# |
| AttMainGroupsCount | Int32 | # of groups all the AttUnitMain split into. Maximum is 3 |
| TargetChoice | [TargetingType](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Targeting-Type) | Options are: Gold - will target enemy with most gold. Balanced - will target weakest enemy. Closest - will target closest enemy. Player - will target player, or closest enemy if in players team or in multiplayer. |
***

***

***
