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

TODO
