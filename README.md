# Gobber Rare Ores Datapack

This datapack dramatically reduces the ore generation frequency for the Gobber mod ores to create balanced, progressive difficulty across dimensions.

## 🎯 What it does

### Ore Reduction Overview
```
┌─────────────┬─────────────┬─────────────┬─────────────┐
│ Dimension   │ Original    │ Datapack    │ Reduction   │
├─────────────┼─────────────┼─────────────┼─────────────┤
│ Overworld   │ ████████    │ █           │ -93.75%     │
│             │ 64/chunk    │ 4/chunk     │             │
├─────────────┼─────────────┼─────────────┼─────────────┤
│ Nether      │ ████████    │ ▌           │ -96.875%    │
│             │ 64/chunk    │ 2/chunk     │             │
├─────────────┼─────────────┼─────────────┼─────────────┤
│ End         │ ████████    │ ▌           │ -98.95%     │
│             │ 64/chunk    │ 0.67/chunk  │             │
└─────────────┴─────────────┴─────────────┴─────────────┘
```

### **Detailed Changes:**
- **Overworld**: 2 veins per chunk, Y -40 to Y 30, 2 ores per vein = **4 ores/chunk**
- **Nether**: 2 veins per chunk (50% spawn chance), Y 5 to Y 120, 2 ores per vein = **2 ores/chunk average**
- **End**: 1 vein per chunk (33% spawn chance), Y 20 to Y 120, 2 ores per vein = **0.67 ores/chunk average**

## Installation

### Folder Installation (REQUIRED - Zip Files Don't Work Properly)
1. Download the `gobber-rare-ores-datapack` folder
2. Place the entire folder into your world's `datapacks` directory
3. Use `/reload` command or restart your world
4. The changes will apply to newly generated chunks

**⚠️ Important**: This datapack has compatibility issues when used as a zip file. While Minecraft will show it as "loaded", the ore generation changes will NOT apply. This is a known issue with certain datapack configurations that override mod features. Always use the folder method for this datapack.

## Testing

To verify it's working, go to unexplored areas and use:
```
/fill ~-4 -40 ~-4 ~4 30 ~4 air replace gobber2:gobber2_ore
```

**Expected Results:**
- **Before datapack**: Would find ~15-20 ore blocks in this area
- **After datapack**: Should find ~3-4 ore blocks (or possibly none)

## How it Works

This datapack uses the **feature override method** - it directly replaces the original Gobber placed features with new versions that have much lower spawn rates. This is more reliable than biome modifiers and works consistently.

## Compatibility

- Designed for **NeoForge** modloader
- Compatible with Minecraft 1.20.1+ 
- Requires the Gobber mod to be installed

## 📊 Impact Summary

| Aspect | Original Gobber | With Datapack |
|--------|----------------|---------------|
| **Overworld ores/chunk** | 64 | 4 |
| **Nether ores/chunk** | 64 | 2 (average) |
| **End ores/chunk** | 64 | 0.67 (average) |
| **Mining difficulty** | Creative-like | Balanced progression |
| **Progression curve** | Flat | Overworld → Nether → End |

The original Gobber mod generated an overwhelming **64 ores per chunk** in every dimension. This datapack creates a proper difficulty curve while maintaining the mod's intended height ranges and ore distribution patterns.

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