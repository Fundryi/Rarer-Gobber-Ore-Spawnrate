# Gobber Rare Ores Datapack

This datapack reduces the ore generation frequency for the Gobber mod ores to make them much rarer and more valuable to find.

## What it does

- **Overrides** the original Gobber ore generation with rare versions:
  - Overworld Gobber Ore: ~2 veins per chunk (very rare), Y 0-160
  - Nether Gobber Ore: ~1 vein per 2 chunks (50% chance), Y 0-256
  - End Gobber Ore: ~1 vein per 3 chunks (33% chance), Y 0-256

## Installation

1. Place this entire folder into your world's `datapacks` directory
2. Use `/reload` command or restart your world
3. The changes will apply to newly generated chunks

## Testing

To verify it's working, go to unexplored areas and use:
```
/fill ~-4 0 ~-4 ~4 32 ~4 air replace gobber2:gobber2_ore
```

You should find significantly fewer ore blocks compared to before!

## Compatibility

- Designed for **NeoForge** modloader
- Compatible with Minecraft 1.20.1+ 
- Requires the Gobber mod to be installed

## Rarity Comparison

- **Before**: 8 veins per chunk (original Gobber settings)
- **After**: 2 veins per chunk in Overworld, 50% chance in Nether, 33% chance in End