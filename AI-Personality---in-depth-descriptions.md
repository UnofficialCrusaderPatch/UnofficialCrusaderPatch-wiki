There are some values in the aic variables that might be hard to understand without understanding how exactly the AI uses them and how the prioritizations are.
Thus a few things will be explained in more detail here.


## Unit recruitment

There are a number of different variables for units the AI can recruit. These can be grouped into four categories: Sortie, Defence, Raid, Offence.
There are also different parameters that determine in which speed and priority these units are recruited. These are the RecruitProb and the RecruitInterval.
Then there is also a threshold of gold (RecruitGoldThreshold) that determines if defensive or offensive units are recruited.

Now, even if the variables for prioritizations are set, units set in sortie will ALWAYS be recruited first. They always have highest priority.
SortieUnitRanged have priority over SortieUnitMelee.
The RecruitProbs should be set so that all corresponding "Default", "Weak" and "Strong" add up to 100 for easier comparison.
After the AI has finished its castle and recruited first defenders and the sortie units, it will look at the recruit probabilities.
It will try to recruit a unit by comparing the numbers of those probabilities and then calculating a chance out of that.

The RecruitInterval variable is easy to use and understand. The higher this value, the slower the AI will recruit. Values should stay between 1 and 16.

The RecruitGoldThreshold is harder to explain and understand. It is mainly used (in vanilla Crusader) as to ensure Crusader AI Lords always have 
200 Gold for their workshops.
It prevents the AI from recruiting units other than for sortie and raids (for some reason) if it has less than the amount of gold specified here. Can be 
quite helpful to set in some situations. E.g. if the AI uses monks as main melee unit and should always try to build the cathedral required to recruit them.


Then there are the lists of defensive, raid and offensive units. The AI will try to recruit units from top to bottom. If it can not afford a unit it will be skipped. 


## Resourcemanagement

There are also a lot of different variables that determine how the AI handles resources. There is a list of which resources the AI immediately sells, for 
how much to keep of a specific resource, one for resource variance and one for sending resources to allies.

If an AI has e.g. lumber on its list of resources to sell, it will always do so as soon as they are on stock and it is not selling or purchasing something else 
at the moment. This can lead to problems if you set the wrong resource here. If we take out example, the AI will never keep any wood in stock. And if it tries to 
build something that costs lumber it will buy the required wood if it has the gold for that and (by chance) immediately sell it again before that building can be placed. 
This might end up in a loop and the AI will just lose gold without accomplishing anything.

Setting the maximum amount to keep of a specific resource is also important. You need to know how many stockpiles the AI you are modifying typically builds and work from there.
How many different resources will it use? How much stone / wood will be required? Typically setting the stone to [highest stone building cost] + 10 is a good idea. For wood it should 
always be a minimum of 20, and a maximum of [# of workshops that use lumber] times 8. Iron should be set to 10 if the AI has engineers with oil.
Iron, Pitch, Flour, Hop is part of MaxResourceOther, so setting one of them is not possible. 
Food should be set to an amount that is less than the maximum the AI could possibly store in the granary so it can sell some if too much is coming in. 
MaxEquipment determines how many of each equipment type the AI stores in the armoury. If the AI has a single armoury and uses 4 types, setting it to 7 should be fine. In general you 
should set it to: [# of armouries] times 50 divided by [# of types] minus [MaxResourceVariance].

You can also determine how many (if any) resources the AI will send to allies by setting the "MinimumGoodsRequiredAfterTrade" variable. If the player asks the AI for goods the AI will 
take a look at that value and if it would still have more than this amount of the asked good after the trade it will send the goods. E.g.: Player asks an AI for 20 wood. MaxWood is set to 
25 and MinimumGoodsRequiredAfterTrade is set to 15. 
The AI will probably have around 25 wood    ==>    25 - 20 = 5    ==>    5 < 15    ==>    AI won't send the wood.



## ToDo Add more entries and images