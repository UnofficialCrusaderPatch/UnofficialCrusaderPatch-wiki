The personalities and quirks of the AI characters in Stronghold Crusader are hardcoded in its executable into 169 integer parameters. This information can be edited through the use of the AI Character (AIC) format, which contains exactly these 169 parameters of each AI in text form, available to be edited by everyone. The UCP is then able to read the aic-file and edit Crusader's executable appropriately.

## HOW TO EDIT YOUR OWN AIC-FILE

### Creating your own file

If you start the UCP and navigate to the **AIC section** you will get a list of UCP-intern .aic-files.
Expand the description of the "vanilla.aic" and click on the export button.  
![](https://i.imgur.com/6SyRpLg.png)

Check your selected Crusader folder. There should be a new folder called "aic". With the exported "vanilla.aic" file inside.  
![](https://i.imgur.com/sLNjH5y.png)

Rename the file to "myversion.aic" and click in the UCP on the reload button in the bottom right.  
![](https://i.imgur.com/SKoXPfP.png)

Your file should now appear in the list. If you check it and install the patch, your AIC changes will be patched into your Crusader executable.  
![](https://i.imgur.com/6HEUNKB.png)

### Editing AIC files

There are two ways to edit the .aic files:
1. Use the [AI Character Editor (AICE)](https://github.com/ByBurton/AI_Character_Editor/releases) by [ByBurton] (https://github.com/ByBurton) AKA Kimberly to have a graphical user interface for editing (no longer supports latest version)
2. Use a text editor

As the use of the **AICE** is straightforward, I will describe an example edit in text form instead. Open the "myversion.aic" file in a text editor of your choice. You will see an **AIFileHeader** section. This is supposed to include general information of the .aic-file like descriptions and their translations. You can also write a description with line breaks in the following way:  
![](https://i.imgur.com/VDXU5rq.png)

Now, let's say we want to replace Philipp's Spearmen with Pikemen. Therefore we need to find the AICharacter entry of Philipp first:  
![](https://i.imgur.com/SjhUm7d.png)

Now scroll down until you find the **PoleturnerSetting** and set it from Spears to **Pikes**  
![](https://i.imgur.com/UyL1dP4.png)

Directly below is the list of resources the AI always sells. There you have to change **SellResource11** from Pikes to Spears, so that the AI does not instantly sell their newly produced pikes, but spears instead.  
![](https://i.imgur.com/zFDvZUZ.png)

Next we need to change the units he wants to recruit, so we have to change all entries with **Spearman** to **Pikeman**.
This includes the following entries: 
- SortieUnitMelee
- DefDiggingUnit
- AttDiggingUnit
- AttUnitMain1
- AttUnitMain2  
![](https://i.imgur.com/MTQQ2ke.png)

Now save the file and click the reload button in the UCP.

### Applying your AIC-File
The myversion.aic file should now be listed with a different color in the AIC section of the UCP. Activate it and deactivate all other .aic-files in the list.  
![](https://i.imgur.com/isAwrEn.png)

Then click install as usual and your edits should be applied to your Crusader executable.
If you start up Crusader and play a match against Philipp, he should now produce pikes and recruit Pikeman.  
![](https://i.imgur.com/ezDLyi9.png)