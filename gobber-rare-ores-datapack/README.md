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
- **Overworld**: 2 veins per chunk, Y -40 to Y 30, 2 ores per vein
- **Nether**: 2 veins per chunk (50% spawn chance), Y 5 to Y 120, 2 ores per vein
- **End**: 1 vein per chunk (33% spawn chance), Y 20 to Y 120, 2 ores per vein

## 📦 Installation

**⚠️ IMPORTANT: Folder Installation Required**

1. Place this entire `gobber-rare-ores-datapack` folder into your world's `datapacks` directory
2. Use `/reload` command or restart your world
3. The changes will apply to newly generated chunks

**Note**: This datapack **must be installed as a folder**. Zip files appear "loaded" but don't actually apply the changes due to mod feature override compatibility issues.

## 🧪 Testing

To verify it's working, go to unexplored areas and use:
```
/fill ~-4 -40 ~-4 ~4 30 ~4 air replace gobber2:gobber2_ore
```

**Expected Results:**
- **Before datapack**: Would find ~15-20 ore blocks in this area
- **After datapack**: Should find ~3-4 ore blocks (or possibly none)

## ✅ Compatibility

- **Minecraft**: 1.20.1+
- **Modloader**: NeoForge
- **Required**: Gobber Mod
- **Installation**: Folder only (zip files don't work)

## 📊 Impact Summary

| Aspect | Original Gobber | With Datapack |
|--------|----------------|---------------|
| **Overworld ores/chunk** | 64 | 4 |
| **Nether ores/chunk** | 64 | 2 (average) |
| **End ores/chunk** | 64 | 0.67 (average) |
| **Mining difficulty** | Creative-like | Balanced progression |
| **Progression curve** | Flat | Overworld → Nether → End |

The original Gobber mod generated an overwhelming **64 ores per chunk** in every dimension. This datapack creates a proper difficulty curve while maintaining the mod's intended height ranges and ore distribution patterns.