# WaterWork — Early Water Rework for Per Aspera

A YAML mod that reworks water management in the early game, adding an ice treatment building chain, updating colony needs, and making ice mining contribute to planetary water stock.

> **Requires the [WaterWorkFix](https://github.com/PerAsperaMods/WaterWorkFix) C# companion mod** — without it, vein consumption and water level mechanics will not work.

---

## Features

- **Ice Treatment Complex** — A new building with 3 tiers that mines and processes a water-ice vein to supply water to nearby colonies via pipes.
  - Tier 1: available from the start
  - Tier 2: unlocked via *Ice Refinery* (Biology lane — Basic Life Support)
  - Tier 3: unlocked via *Advanced Ice Refinery* (Biology lane — Intermediate Life Support + Water Distribution)

- **Food Factory T3** — A new superior food factory tier, unlocked in the Biology tree (Advanced Life Support).

- **Updated colony needs** — Colonies, food factories, and oxygen release plants now require water pipe access to operate.

- **Crater Lake** — A new building placed on crater veins that slowly raises atmospheric water vapor. Unlocked via the Crater Farm tech (Biology lane).

- **Ice mining raises water level** — Ice treatment plants and water mines gradually increase the planet's water stock when surface temperature exceeds 0 °C. *(WaterWorkFix companion required)*

---

## Installation

### Step 1 — BepInEx

Download and install [BepInEx 6.x IL2CPP](https://github.com/BepInEx/BepInEx/releases) into your Per Aspera folder:

```
D:\SteamLibrary\steamapps\common\Per Aspera\
```

Run the game once to let BepInEx generate its folder structure.

### Step 2 — Per Aspera SDK

Download `PerAspera-SDK-vX.X.zip` from the [SDK releases](https://github.com/PerAsperaMods/PerAspera-SDK/releases).

Extract the `plugins/SDK/` folder into `BepInEx/plugins/`:

```
BepInEx/plugins/SDK/
  PerAspera.Core.dll
  PerAspera.Core.IL2CppExtensions.dll
  PerAspera.GameAPI.dll
  PerAspera.GameAPI.Wrappers.dll
  ...
```

### Step 3 — WaterWorkFix companion

Download `WaterWorkFix.dll` from the [WaterWorkFix releases](https://github.com/PerAsperaMods/WaterWorkFix/releases) and drop it into `BepInEx/plugins/`:

```
BepInEx/plugins/
  WaterWorkFix.dll
```

### Step 4 — This mod (YAML)

Subscribe on [Steam Workshop (ID: 3359421244)](https://steamcommunity.com/sharedfiles/filedetails/?id=3359421244), or manually copy the mod folder into:

```
Per Aspera_Data/StreamingAssets/Mods/WaterWork/
```

---

## Final folder structure

```
Per Aspera/
├── BepInEx/
│   └── plugins/
│       ├── SDK/
│       │   ├── PerAspera.Core.dll
│       │   └── ...
│       └── WaterWorkFix.dll
└── Per Aspera_Data/
    └── StreamingAssets/
        └── Mods/
            └── WaterWork/       ← this mod
```

---

## Compatibility

- Per Aspera **1.8.x**
- Does **not** require BlueMars

---

## Related

- [WaterWorkFix](https://github.com/PerAsperaMods/WaterWorkFix) — C# companion (vein fix + ice melt mechanic)
- [Per Aspera SDK](https://github.com/PerAsperaMods/PerAspera-SDK) — Modding SDK used by the companion
