Installation guide by patel-nikhil: https://github.com/patel-nikhil

#### Unofficial Crusader Patch Latest Version: UCP 2.13

[changelog](https://github.com/Sh0wdown/UnofficialCrusaderPatch/releases/tag/v2.13) [download](https://github.com/Sh0wdown/UnofficialCrusaderPatch/releases/download/v2.13/UnofficialCrusaderPatch_v2.13.exe)

* * *    
### Installation

##### Download the Unofficial Crusader Patch (UCP)

[Latest Stable Release](https://github.com/Sh0wdown/UnofficialCrusaderPatch/releases/download/v2.13/UnofficialCrusaderPatch_v2.13.exe)  
[View source on GitHub](https://github.com/Sh0wdown/UnofficialCrusaderPatch/tree/master)

##### Copy UCP to installation directory and extract

Copying the UCP to the installation directory is necessary as the patcher needs to know where Stronghold Crusader is installed. If the location is under C:\\Program Files you may need to complete the remaining instructions by running as administrator. Common default installation paths are:

*   C:\Program Files (x86)\Firefly Studios\Stronghold Crusader
*   C:\Program Files (x86)\Steam\steamapps\common\Stronghold Crusader Extreme

##### Copy ucp.cfg (configuration file) to folder

If you plan to play multiplayer or wish to use someone else's configuration then sharing the ucp.cfg file is the best way to do this.  
For multiplayer, the UCP settings must be identical or else desync is almost certain to happen.

##### Interactive installation steps

*   Open extracted folder and double-click UnofficialCrusaderPatchGUI.exe
*   Browse and locate path to Stronghold Crusader if not already shown on the interface
*   Click continue to choose your options [(see overview of options)](features.html)
*   When you are ready click install

##### Silent installation steps

*   Open extracted folder and double-click to run UnofficialCrusaderPatchCLI.exe

_You may need to run this as administrator if your install is located within a system-protected folder/_  
_A black (console) window will temporarily open while the patcher is installing. This is normal behaviour._

##### Advanced (custom) installation steps

The UnofficialCrusaderPatchCLI.exe executable accepts a number of command-line arguments that allow you to customize the installation.  
Command-line arguments are as follows:

*   `--aic[-overwrite]=<relative path to source aiv folder>`
*   `--aiv[-overwrite]=<relative path to source aiv folder>`
*   `--maps[-overwrite]=<relative path to source maps folder>`
*   `--mapsExtreme[-overwrite]=<relative path to source mapsExtreme folder>`
*   `--no-output`

_Enclosure in square brackets indicate optional presence. Source folder refers to the folder where you have kept your aiv/aic/maps files._  
Default mode is copy. Behaviour is described as follows. aiv files will be used as an example.  
Program Output:

*   When the CLI tool is passed an argument it will by default display where files, if any, are saved to. It will also display what files (ie. aic) are copied, and to where (see below for details). This feature can be disabled by running the CLI tool with the argument `--no-output`

With argument `--aiv=<aiv path>` the following happens:

*   Files in "aic" folder of installation are copied to folder bak-YYYY-MM-DDTHHMMSS
*   Files from `<aic path>` folder are copied to aic folder of installation
*   Installation proceeds. For aic files, the copied files from can be used in the silent install if they are specified in the ucp.cfg

With argument `--aiv-overwrite=<aiv path>` the following happens:

*   Suppose file with filename 1.aiv exists in "aiv" folder of installation..
*   File 1.aiv is deleted from installation folder
*   The new 1.aiv is copied from `<aic path>` to "aiv" folder of installation
*   Installation proceeds. For aic files, the copied files from can be used in the silent install if they are specified in the ucp.cfg

### Visual Overview of Features

#### Step 1: Language Selection

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/language-select.png)

#### Step 2: Installation Path Selection

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/window.png)

#### Step 3: Select Your Features


#### Bugfixes

##### _These include fixes to various gameplay bugs. Most users will want to select all options._

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/bugfixes.png)

#### AIV

##### _Selecting a castle set here will change the way the AI characters build their castles in-game._

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/aiv.png)

#### AIC

##### _Selecting an file here will change the in-game behaviour of an AI. The boxes that are coloured beige indicate user-provided aic files._  
vanilla.aic is the AI behaviour as it is defined in Stronghold Crusader (without UCP).  
You may hold Ctrl and click to select/deselect multiple aic files. Note that if an AI Character is defined multiple times the one from the first file (alphabetically) will be used

##### _See [AIC Editing Tutorial](https://github.com/Sh0wdown/UnofficialCrusaderPatch/wiki/AIC-Editing-Tutorial) for more about editing AI behaviour_  

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/aic.png)

#### AI Lords

##### _These include changes to how the AI characters behave._

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/ai-lords.png)

#### Units

##### _These include changes to the characteristics of certain troops._

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/units.png)

#### Other

##### _These include various quality of life and convenience changes._

![](https://patel-nikhil.github.io/UnofficialCrusaderPatch/assets/img/other.png)