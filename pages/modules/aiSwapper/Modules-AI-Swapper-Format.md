# AI-Swapper-Format

The new AI system uses a dedicated format to represent AIs without a direct connection to a specific AI slot. The format is based on a folder and configuration files.

### Resource Placement

For the GUI to pick-up the AI format, the AI-folder needs to be placed at a specific position inside a plugin. The general plugins folder is in:

`<game-folder>/ucp/plugins`

The AI folder now needs to be placed inside a plugin:

`<plugin-folder>/resources/ai/<ai-folder>`

A full path would then be:

`<game-folder>/ucp/plugins/<plugin-folder>/resources/ai/<ai-folder>`

The AI folder itself can have an arbitrary name. It will not define how the AI will show up in the game or in the GUI.  
**Note:** As of now, there seems to be an issue with non-ASCII characters in the AI folder name. So please use only ASCII characters for now.

## Folder Overview

The following contains an overview of complete AI folder that provides all parts.

```text
ai-folder
│
├── aiv
│   ├── ... <aiv-files>
│   └── mapping.json
│
├── binks
│   ├── ... <bik-files>
│   └── mapping.json
│
├── lang
│   └── ... <locale> (example: "en")
│           ├── binks 
│           │   └── ... (same content as default "binks", but for this language)
│           │
│           ├── speech 
│           │   └── ... (same content as default "speech", but for this language)
│           │
│           └── lines.json (same structure as default "lines.json", but for this language)
│
├── speech
│   ├── ... <wav-files>
│   └── mapping.json
│
├── character.json
├── lines.json
├── meta.json
├── portrait.png
└── portrait_small.png
```

## Parts

### meta.json

The core of the AI configuration is the meta.json file. It includes several properties that will be displayed in the AI-Swapper. But most importantly it describes which parts are even provided by the AI.

```json
{
  "name": "John Silver",                // name used in the AI-Swapper-GUI
  "description": "A small description", // short description of the AI; currently nowhere displayed
  "author": "Thomas",                   // author of the AI
  "link": "www.example.com",            // link to the AI source; currently nowhere displayed
  "version": "1.0.0",                   // version of the AI; for information purposes, not used for version resolving
  "defaultLang": "de",                  // default language of the AI; uses typical language codes; expects the data in the main folder
  "supportedLang": ["de", "en"],        // supported languages of the AI; uses typical language codes; expects the data in the properly named "lang"-folder (except for the defaultLang)
  "switched": {                         // defines which AI parts are provided by the AI; "true" means:
    "binks": true,                          // a "binks"-folder with "mapping.json" and bink-files is provided   
    "speech": true,                         // a "speech"-folder with "mapping.json" and wav-files is provided
    "aic": true,                            // a "character.json" with AIC part is provided
    "aiv": true,                            // an "aiv"-folder with "mapping.json" and aiv-files is provided
    "lord": true,                           // a "character.json" with lord part is provided
    "startTroops": true,                    // a "character.json" with start troops part is provided
    "lines": true,                          // a "lines.json" with the texts of the AI is provided
    "portrait": true                        // a "portrait.png" and a "portrait_small.png" with the portrait of the AI is provided
  }
}
```
*Important*:  
JSON does not support comments. These are only for documentation purposes and need to be removed should the example be used as reference.

### portrait.png and portrait_small.png

These files are transformed to the actual AI portraits in-game. Unlike before, where the portraits used Windows bitmap format, only the [PNG-format](https://de.wikipedia.org/wiki/Portable_Network_Graphics) is supported as of now.  
Additionally, the handling of transparency was changed. While transparency was indicated by a special magenta color before, the portraits of the AI format actually use the alpha channel to indicate transparency. It is important to understand that the game still only supports whether there should be a pixel or not and alpha values like 0.3 or 0.7 for example are rounded to 0 or 1. Being aware of this can help preventing edge artifacts.  
Both the normal and the small portrait need to be provided if the portrait support should be available.

_Format_:
- _portrait.png_: 72x72
- _portrait_small.png_: 36x36
