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
| Unknown009 | Int32 |  |
| Unknown010 | Int32 |  |
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
| MaxQuarries | Int32 |  |
| MaxIronmines | Int32 |  |
| MaxWoodcutters | Int32 |  |
| MaxPitchrigs | Int32 |  |
| MaxFarms | Int32 | The maximum amount of farms the AI builds. HopFarms are excluded from this! (Also check PopulationPerFarm) |
| BuildInterval | Int32 | This is only considered <= 5000 gold |
| ResourceRebuildDelay | Int32 | The delay before the AI rebuilds destroyed buildings. |
| MaxFood | Int32 | includes flour? |
| MinimumApples | Int32 |  |
| MinimumCheese | Int32 |  |
| MinimumBread | Int32 |  |
| MinimumWheat | Int32 |  |
| MinimumHop | Int32 | unclear |
| TradeAmountFood | Int32 |  |
| TradeAmountEquipment | Int32 |  |
| Unknown040 | Int32 |  |
| Unknown041 | Int32 |  |
| Unknown042 | Int32 |  |
| MaxWood | Int32 |  |
| MaxStone | Int32 |  |
| MaxResourceOther | Int32 |  |
| MaxEquipment | Int32 |  |
| MaxBeer | Int32 |  |
| MaxResourceVariance | Int32 | added to all max resource values? |
| RecruitGoldThreshold | Int32 | A (gold) threshold which disables any recruitment of all units except for raiding and sortie until it is met |
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
| Unknown068 | Int32 |  |
| Unknown069 | Int32 |  |
| DefSiegeEngineGoldThreshold | Int32 | This one makes no sense. In code: [if (Gold + Threshold > 30) then RecruitEngineer()], maybe it was supposed to be minus... |
| DefSiegeEngineBuildDelay | Int32 | The delay before the AI builds its first defensive siege engine. |
| Unknown072 | Int32 |  |
| Unknown073 | Int32 |  |
| RecruitProbDefDefault | Int32 | The probability with which this AI reinforces missing defense troops. |
| RecruitProbDefWeak | Int32 |  |
| RecruitProbDefStrong | Int32 |  |
| RecruitProbRaidDefault | Int32 |  |
| RecruitProbRaidWeak | Int32 |  |
| RecruitProbRaidStrong | Int32 |  |
| RecruitProbAttackDefault | Int32 |  |
| RecruitProbAttackWeak | Int32 |  |
| RecruitProbAttackStrong | Int32 |  |
| SortieUnitRangedMax | Int32 |  |
| SortieUnitRanged | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of ranged units that go to the last attacked farm or building, and guard it until another is attacked. |
| SortieUnitMeleeMax | Int32 |  |
| SortieUnitMelee | [Unit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of melee units to attack enemy units shooting at the AI's buildings or workers. |
| DefDiggingUnitMax | Int32 | Amount of units that dig own moat. |
| DefDiggingUnit | [DiggingUnit](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) | Type of unit to dig own moat. |
| RecruitInterval | Int32 |  |
| RecruitIntervalWeak | Int32 | The 'weak' state sets in if the AI is completely trashed. F.e. troops < 8, gold < 200, population < 15, ... |
| RecruitIntervalStrong | Int32 | The 'strong' state sets in if f.e. the AI has troops >= 40, gold >= 200, population >= 40, ... |
| DefTotal | Int32 | The total count of all defensive units (wall defense + patrols) |
| OuterPatrolGroupsCount | Int32 | The number of groups the patrols defending the outer economy split into. |
| OuterPatrolGroupsMove | Bool | Whether the patrols stay at one place (quarry) or move around. |
| Unknown095 | Int32 |  |
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
| AttForceRallyDistanceRandom | Int32 | The distance variance an AI will add to the default rally distance for sieges. |
| AttForceRallyPercentage | Int32 | The %-amount of units of the attack force that the AI will rally before attacking. (0 - 100) |
| Unknown129 | Int32 |  |
| AttForceCasualtiesPercentageBeforeAssault | Int32 | The %-amount of (siege engines? engineers? laddermen? tunnelers? siege def?) that need to be destroyed / killed before the main units attack. |
| AttForceSuccessRallyPercentage | Int32 | The %-amount of units of the attack force that will rally (at the bested enemy's keep location) before retreating or attacking again. |
| Unknown132 | Int32 |  |
| SiegeEngine1 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine2 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine3 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine4 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine5 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine6 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine7 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| SiegeEngine8 | [SiegeEngine](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/Units) |  |
| Unknown141 | Int32 |  |
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