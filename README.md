# Gobber Rare Ores Datapack

This datapack reduces the ore generation frequency for the Gobber mod ores to make them much rarer and more valuable to find.

## What it does

- **Overrides** the original Gobber ore generation with rare versions:
  - Overworld Gobber Ore: ~2 veins per chunk (very rare), Y 0-160
  - Nether Gobber Ore: ~1 vein per 2 chunks (50% chance), Y 0-256
  - End Gobber Ore: ~1 vein per 3 chunks (33% chance), Y 0-256

## Installation

### Option 1: Folder Installation (Recommended)
1. Download the `gobber-rare-ores-datapack` folder
2. Place the entire folder into your world's `datapacks` directory
3. Use `/reload` command or restart your world
4. The changes will apply to newly generated chunks

### Option 2: Zip Installation
1. Download `gobber-rare-ores-datapack-1.0.0.zip`
2. Place the zip file directly into your world's `datapacks` directory
3. Use `/reload` command or restart your world

## Testing

To verify it's working, go to unexplored areas and use:
```
/fill ~-4 0 ~-4 ~4 32 ~4 air replace gobber2:gobber2_ore
```

You should find significantly fewer ore blocks compared to before!

## How it Works

This datapack uses the **feature override method** - it directly replaces the original Gobber placed features with new versions that have much lower spawn rates. This is more reliable than biome modifiers and works consistently.

## Compatibility

- Designed for **NeoForge** modloader
- Compatible with Minecraft 1.20.1+ 
- Requires the Gobber mod to be installed

## Rarity Comparison

- **Before**: 8 veins per chunk (original Gobber settings)
- **After**: 2 veins per chunk in Overworld, 50% chance in Nether, 33% chance in End

---

## 🤖 Note for AI Development

**CRITICAL: Datapack Zip Structure for Minecraft**

When creating zip files for Minecraft datapacks, the structure MUST be:

```
datapack.zip
├── pack.mcmeta          ← Files at ROOT level
├── data/                ← No extra folder wrapper!
└── other files...
```

**PowerShell command to zip correctly:**
```powershell
# Navigate TO the datapack folder first, then:
Compress-Archive -Path 'pack.mcmeta', 'data', 'README.md' -DestinationPath '../datapack-name.zip' -Force
```

**WRONG (causes datapack to fail):**
```
datapack.zip
└── datapack-folder/     ← Extra folder = BROKEN!
    ├── pack.mcmeta
    └── data/
```

Always test: Open the zip file - you should immediately see `pack.mcmeta` and `data/` folder, not another folder first!