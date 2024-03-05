by @LordHansCapon

Hey guys,

I haven't found any tutorials regarding this repository, like how to set up the developer environment or how to write your changes into the patcher... so here we go, I will help you get started with it!

This tutorial will not be for programming newbies! So I will not be detailing how to exactly install your softwares, what is GIT, how to use it etc...

**Keep in mind that this tutorial is not Sh0wdown's tutorial, nor was it endorsed by him directly. So everything I write here is my own experience with the repository.**

### The Setup
First of all, we need an environment to setup in which we can compile/debug this repository. You can use JetBrains Rider, Visual Studio Code, Visual Studio... whatever fits you. I will be using JetBrains Rider as I already have it.

1. Download the repository by cloning, directly downloading or forking it.
2. Open the project, there are 4 projects in the solution, select the UnofficialCrusaderPatch one.
3. Setup your Run/Debug Configurations. In JetBrains, double tap Shift, then type in Edit Configurations. It will automatically create a Default .NET project run/debug configuration, you can press Apply & OK, the default should be fine. If it is not, then be sure the target framework is .NET v4.0.
4. To compile, you will need Evrey's AIV files, so head to this link: https://github.com/Evrey/SHC_AIV
5. Download Evrey's SHC_AIV project as a ZIP, extract **firefly_fixed**, **history**, **skirmish** into the UnofficialCrusaderPatch/SHC_AIV folder. Yes, you have to create the SHC_AIV folder first.

If everything done correctly, you can compile and run the software. Now this is where the fun begins.

### Getting to know the code
Due to the lack of documentation and the unconventional approach Sh0wdown has taken in this repository, it is hard to get started without a guide. But hey, this is what this article is about, right?

The patcher operates with CodeBlocks. Every CodeBlock is an array of byte which will be scanned in the exe. These CodeBlocks are use to identify (ident) the correct part of the exe.

To simplify it, you are not saying you want to override 4 bytes on address **6B90E8**, you say **search for these bytes** then we are saying **write some bytes** then **skip X bytes** then **write some bytes again**.

You can see every change applied in the patcher in the **changes** list in Version.cs. These changes will be rendered as Options in the patcher in their correspondig tab set by their ChangeType.

Let's look at one of the simplest changes in this patcher, search for 004CBCD5 in Version.cs. This is the **Disable sleeping mode for lack of resources** option under AI lords tab. Let's take a look at its structure.

We create a new Change instance, set its titleIdent to ai_nosleep, now this titleIdent will be the change's title, you can edit this in the Localization/English.txt or german/polish/russian etc. If you open the localization and search for **ai_nosleep**, you can find the title and its description which will be used when generating the option.

The second parameter of the Change constructor is the type of the change, this determines the tab this option gets on, then we have enabledDefault and exclusive.

Inside the Change, we have a DefaultHeader instantiated, which is used to create the header of the option. This also gets a descrIdent which will be our description when the option is expanded. If you want to create an option where it has suboptions such as the AI Attack target change one, you can take a look on how to do that at if you search for **ai_attacktarget** in Version.cs.

Any binary command you add under the header will be applied when the option is selected and the patcher starts installing.

### Adding code
We have discussed a lot of stuff but we haven't written a single line of code, nor did I explain how to edit any data really. So this section will be a quick look on how to add a simple change.

#### Part 1
Create a new .block file in CodeBlocks, name it o_mychange1.block (o_ prefix means **other**, and I added **1** because later you wouldn't see the difference between localization string and the block string.). Add your byte array which you want to edit. Let's say I want to change my Marketplace Weapon item order, so I add:

`13 00 00 00 11 00 00 00 15 00 00 00 12 00 00 00 14 00 00 00 16 00 00 00 17 00 00 00 18 00 00 00`

This will 100% match the address I am searching for. This is at address 6B90E8. This is important, so keep that in mind.

#### Part 2
Open up Localization/English.txt, add this template:

```
o_mychange
{
	"My change name"
}

o_mychange_descr
{
	"My change long description which elaborates on how much it changes!"
}
```

Change the name and description obviously...

#### Part 3
Now open Version.cs and add to the changes list, create a new change and set it up as a single option change for now.

```
// Marketplace weapon order change
new Change("o_mychange", ChangeType.Other)
{
    new DefaultHeader("o_mychange")
    {
    }
},
```
Here we used our localization via accessing **o_mychange** and set our change into the Other tab. Now we can add some basic changes. Currently we want to change the whole array of bytes to a new one, so let's go ahead and create a BinaryEdit and tell it to identify the code part we store in our **o_mychange1.block**:

```
// Marketplace weapon order change
new Change("o_mychange", ChangeType.Other)
{
    new DefaultHeader("o_mychange")
    {
        new BinaryEdit("o_mychange1") // 6B90E8
        {
        },
    }
},
```
If we know what to replace the array of byte with, we can go ahead and create a new BinBytes instance which will store the data which will be written on our current position:

```
// Marketplace weapon order change
new Change("o_mychange", ChangeType.Other)
{
    new DefaultHeader("o_mychange")
    {

        new BinaryEdit("o_mychange1") // 6B90E8
        {
            // Marketplace item order
            new BinBytes(0x11, 0x00, 0x00, 0x00, 0x13, 0x00, 0x00, 0x00, 0x15, 0x00, 0x00, 0x00, 0x17, 0x00, 0x00, 0x00, 0x12, 0x00, 0x00, 0x00, 0x14, 0x00, 0x00, 0x00, 0x18, 0x00, 0x00, 0x00, 0x16, 0x00, 0x00, 0x00)
        },

    }
},
```
Great, now we overriden the whole array of bytes. You can now compile it and run it. But what if we need to override X bytes every Y bytes? To do that, you can use BinSkip which will skip X amount of bytes. Like so:

```
new BinaryEdit("o_mychange1") // 6B90E8
{
    new BinBytes(0x11, 0x00, 0x00, 0x00, 0x13, 0x00, 0x00, 0x00), // Write 8 bytes
    new BinSkip(4), // Skip 4 bytes
    new BinBytes(0x11, 0x00, 0x00, 0x00) // Write 4 more bytes
},
```
What if I want to jump between addresses? Well, you can create multiple BinaryEdit instances inside the DefaultHeader, so that's it. Create a new .block file to set the **base** address, then just write your bytes there!

Example from my armory/marketplace weapon order fix:
```
new BinaryEdit("o_armory_marketplace_weapon_order_fix1") // 217F50
{
    // Armory item ID order
    new BinBytes(0x11, 0x00, 0x00, 0x00, 0x13, 0x00, 0x00, 0x00, 0x15, 0x00, 0x00, 0x00, 0x17, 0x00, 0x00, 0x00, 0x12, 0x00, 0x00, 0x00, 0x14, 0x00, 0x00, 0x00, 0x18, 0x00, 0x00, 0x00, 0x16, 0x00, 0x00, 0x00),
    // Armory item image ID
    new BinBytes(0x4C, 0x00, 0x00, 0x00, 0x50, 0x00, 0x00, 0x00, 0x54, 0x00, 0x00, 0x00, 0x58, 0x00, 0x00, 0x00, 0x4E, 0x00, 0x00, 0x00, 0x52, 0x00, 0x00, 0x00, 0x5A, 0x00, 0x00, 0x00, 0x56, 0x00, 0x00, 0x00),
    // Armory item image offset
    new BinBytes(0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0xFE, 0xFF, 0xFF, 0xFF, 0x00, 0x00, 0x00, 0x00, 0x04, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0xFC, 0xFF, 0xFF, 0xFF, 0x04, 0x00, 0x00, 0x00, 0xFE, 0xFF, 0xFF, 0xFF, 0x00, 0x00, 0x00, 0x00, 0xFC, 0xFF, 0xFF, 0xFF, 0x00, 0x00, 0x00, 0x00, 0xFE, 0xFF, 0xFF, 0xFF, 0x00, 0x00, 0x00, 0x00)
},
new BinaryEdit("o_armory_marketplace_weapon_order_fix2") // 6B90E8
{
    // Marketplace item order
    new BinBytes(0x11, 0x00, 0x00, 0x00, 0x13, 0x00, 0x00, 0x00, 0x15, 0x00, 0x00, 0x00, 0x17, 0x00, 0x00, 0x00, 0x12, 0x00, 0x00, 0x00, 0x14, 0x00, 0x00, 0x00, 0x18, 0x00, 0x00, 0x00, 0x16, 0x00, 0x00, 0x00)
},
```


You can create custom assembly codes and inject them aswell, just take a look at the Healer change (o_healer), it allocates new data, uses labels, references, variables etc. Once you master the tools provided by Sh0wdown in this repo, you can translate any change and write it into an option.

This tutorial was not meant to teach you everything there is to know about this repository and how to contribute to it, it is more a getting started, first steps guide.

Thank you for reading, I am hoping to have a full, official guide for this repository because it deserves it!