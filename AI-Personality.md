List of 169 parameters which set the AI characters' personality, f.e. what troops to recruit or how many iron mines to build.

| Name | Value Type | Description |
| :--- | :---: | :--- |
| Unknown000 | Int32 |  |
| Unknown001 | Int32 |  |
| Unknown002 | Int32 |  |
| Unknown003 | Int32 |  |
| Unknown004 | Int32 |  |
| Unknown005 | Int32 |  |
| CriticalPopularity | 0 to 10000 | 10000 equals 100 popularity. Below this value, the AI sells more stuff than usual to get money. |
| LowestPopularity | 0 to 10000 | Below this value the AI sets taxes zero until it reaches 'HighestPopularity' again. |
| HighestPopularity | 0 to 10000 | Above this value the AI sets taxes back up |
| TaxesMin | 0 to 12 | 0 being +7 popularity gifts and 11 (or 12) being -24 popularity taxes. | 
| TaxesMax | 0 to 12 | 0 being +7 popularity gifts and 11 (or 12) being -24 popularity taxes. |
| Unknown011 | Int32 |  |
| Farm1 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) | An array of farm slots, which the AI builds in the given sequence. |
| Farm2 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm3 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm4 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm5 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm6 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm7 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| Farm8 | [FarmBuilding](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Buildings) |  |
| PopulationPerFarm | Int32 | The AI builds one farm for each amount of this population value. (Also check MaxFarms) |
| PopulationPerWoodcutter | Int32 |  |
| PopulationPerQuarry | Int32 |  |
| PopulationPerIronmine | Int32 |  |
| PopulationPerPitchrig | Int32 |  |
| MaxQuarries | Int32 | Setting this to zero will not disable building! Set PopulationPerFarm to zero instead! |
| MaxIronmines | Int32 | Setting this to zero will not disable building! Set PopulationPerIronmine to zero instead! |
| MaxWoodcutters | Int32 | Setting this to zero will not disable building! Set PopulationPerWoodcutter to zero instead! |
| MaxPitchrigs | Int32 | Setting this to zero will not disable building! Set PopulationPerPitchrig to zero instead! |
| MaxFarms | Int32 | Setting this to zero will not disable building! Set PopulationPerFarm to zero instead! |
| BuildInterval | Int32 | This is only considered <= 5000 gold |
| ResourceRebuildDelay | Int32 | The delay before the AI rebuilds destroyed buildings. |
| MaxFood | Int32 | Includes wheat. Applies to each kind of food. |
| MinimumApples | Int32 | Reserves that are only consumed if current popularity < LowestPopularity. If the AI has less than this amount it will prioritize buying the missing food. |
| MinimumCheese | Int32 | Reserves that are only consumed if current popularity < LowestPopularity. If the AI has less than this amount it will prioritize buying the missing food. |
| MinimumBread | Int32 | Reserves that are only consumed if current popularity < LowestPopularity. If the AI has less than this amount it will prioritize buying the missing food. |
| MinimumWheat | Int32 | If the AI has less than this amount it will prioritize buying the missing wheat. |
| MinimumHop | Int32 | unclear |
| TradeAmountFood | Int32 |  |
| TradeAmountEquipment | Int32 |  |
| Unknown040 | Int32 |  |
| MinimumGoodsRequiredAfterTrade | Int32 | If the AI would have less than this amount of a good after sending them it won't send them to the requesting player. |
| DoubleRationsFoodThreshold | Int32 | Above this value of food the AI will give double rations out. |
| MaxWood | Int32 |  |
| MaxStone | Int32 |  |
| MaxResourceOther | Int32 |  |
| MaxEquipment | Int32 | Applies to each type of weapon or armour. |
| MaxBeer | Int32 |  |
| MaxResourceVariance | Int32 | added to all max resource values? |
| RecruitGoldThreshold | Int32 | A (gold) threshold which disables any recruitment of all units except for raiding and sortie until it is met. |
| BlacksmithSetting | [BlacksmithSetting](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Workshop-Settings) |  |
| FletcherSetting | [FletcherSetting](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Workshop-Settings) |  |
| PoleturnerSetting | [PoleturnerSetting](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Workshop-Settings) |  |
| SellResource01 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource02 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource03 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource04 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource05 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource06 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource07 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource08 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource09 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource10 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource11 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource12 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource13 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource14 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| SellResource15 | [Resource](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Resource) |  |
| DefWallPatrolRallyTime | Int32 | The amount of time for castle patrols set up in the AIV to move from one rally point to the next. (Remark: Only spearmen, horse archers and macemen currently do) |
| DefWallPatrolGroups | Int32 |  |
| DefSiegeEngineGoldThreshold | Int32 | This one makes no sense. In code: [if (Gold + Threshold > 30) then RecruitEngineer()], maybe it was supposed to be minus... Adding a "-" in front of the value will make it work. |
| DefSiegeEngineBuildDelay | Int32 | The delay before the AI builds its first defensive siege engine. |
| Unknown072 | Int32 |  |
| Unknown073 | Int32 |  |
| RecruitProbDefDefault | Int32 | The probability with which this AI reinforces missing defense troops. Note: These are ignored at the beginning of the game, as there are only sortie and defensive units being recruited. |
| RecruitProbDefWeak | Int32 |  |
| RecruitProbDefStrong | Int32 |  |
| RecruitProbRaidDefault | Int32 |  |
| RecruitProbRaidWeak | Int32 |  |
| RecruitProbRaidStrong | Int32 |  |
| RecruitProbAttackDefault | Int32 |  |
| RecruitProbAttackWeak | Int32 |  |
| RecruitProbAttackStrong | Int32 |  |
| SortieUnitRangedMin | Int32 | These units are only sent out if more than this amout of them has already been recruited. |
| SortieUnitRanged | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of ranged units that go to the last attacked farm or building, and guard it until another is attacked. |
| SortieUnitMeleeMin | Int32 | These units are only sent out if more than this amout of them has already been recruited. |
| SortieUnitMelee | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of melee units to attack enemy units shooting at the AI's buildings or workers. |
| DefDiggingUnitMax | Int32 | Amount of units that dig own moat. |
| DefDiggingUnit | [DiggingUnit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of unit to dig own moat. |
| RecruitInterval | Int32 |  |
| RecruitIntervalWeak | Int32 | The 'weak' state sets in if the AI is completely trashed. F.e. troops < 8, gold < 200, population < 15, ... |
| RecruitIntervalStrong | Int32 | The 'strong' state sets in if f.e. the AI has troops >= 40, gold >= 200, population >= 40, ... |
| DefTotal | Int32 | The total count of all defensive units (wall defense + patrols) |
| OuterPatrolGroupsCount | Int32 | The number of groups the patrols defending the outer economy split into. |
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
| HarassingSiegeEnginesMax | Int32 | The maximum of harassing siege engines an AI builds. |
| Unknown124 | Int32 |  |
| AttForceBase | Int32 | The base amount of troops with which this AI attacks |
| AttForceRandom | Int32 | The maximum random amount of additional troops in an attack (this is not the amount by which the troops increase per attack!) |
| AttForceSupportAllyThreshold | Int32 | If the AI has more than this amount of units in the attack force, it will help their allies or siege an enemy if commanded to do so. |
| AttForceRallyPercentage | Int32 | The %-amount of units of the attack force that the AI will rally before attacking. (0 - 100) |
| Unknown129 | Int32 |  |
| Unknown130 | Int32 |  |
| Unknown131 | Int32 |  |
| Unknown132 | Int32 |  |
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
| AttUnit2 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| AttUnit2Max | Int32 |  |
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
| AttUnitSiegeDef | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | These units patrol between siege enginees in order to protect them. |
| AttUnitSiegeDefMax | Int32 |  |
| Unknown161 | Int32 |  |
| AttUnitMain1 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | AttUntiMain1 to AttUnitMain4 is a list of the main strike force the AI recruits for sieges. Priotizes in order of the list, but only recruits untis for which they have enough gold. So try to place expensive units higher up. |
| AttUnitMain2 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| AttUnitMain3 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| AttUnitMain4 | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| AttMaxDefault | Int32 | This does nothing |
| AttMainGroupsCount | Int32 | "# of groups all the AttUnitMain split into. Maximum is 3" |
| TargetChoice | [TargetingType](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Targeting-Type) |  |