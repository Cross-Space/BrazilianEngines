# BrazilianEngines - Directory Structure Guide

## Repository Organization

This document outlines the organizational structure of the BrazilianEngines mod, following KSP modding best practices.

### Root Level
```
BrazilianEngines/
├── LICENSE                      # MIT License
├── README.md                    # Main documentation (English)
├── CHANGELOG.md                 # Version history and release notes
├── DIRECTORY_STRUCTURE.md       # This file
└── BrazilianEngines/            # Mod distribution folder
    └── GameData/                # KSP GameData root
        └── BrazilianEngines/    # Mod folder
```

### GameData Structure

```
GameData/BrazilianEngines/
│
├── 📁 Localization/             # Multi-language support
│   ├── en-us.cfg               # English (US) localization
│   └── pt-br.cfg               # Portuguese (Brazil) localization
│   └── LOCALIZATION_README.txt  # Localization guide
│
├── 📁 Parts/                    # Engine part definitions
│   ├── 📁 Engines/
│   │   ├── 📁 S-Series/         # Solid motors S-series (IAE)
│   │   │   ├── S10.cfg          # S10-1 and S10-2 motors
│   │   │   ├── S20.cfg          # S20 motor
│   │   │   ├── S23.cfg          # S23 motor
│   │   │   ├── S30.cfg          # S30 motor
│   │   │   ├── S31.cfg          # S31 motor
│   │   │   ├── S33.cfg          # S33 motor
│   │   │   ├── S40.cfg          # S40 motor (VLS-1 1st stage)
│   │   │   ├── S43.cfg          # S43 motor (VLS-1 1st/2nd stage)
│   │   │   ├── S44.cfg          # S44 motor (VLS-1 upper stage)
│   │   │   ├── S50.cfg          # S50 motor (future)
│   │   │   └── _S_Series_Shared.cfg  # Common S-series configs
│   │   │
│   │   ├── 📁 N-Series/         # Solid motors N-series (MLBR Program)
│   │   │   ├── N04.cfg          # N04 motor
│   │   │   ├── N09.cfg          # N09 motor
│   │   │   ├── N90.cfg          # N90 motor
│   │   │   └── _N_Series_Shared.cfg  # Common N-series configs
│   │   │
│   │   └── 📁 Liquid/           # Liquid engines
│   │       ├── Arion.cfg        # Arion engine variants
│   │       ├── L5.cfg           # L5 engine (planned)
│   │       ├── L15.cfg          # L15 engine (planned)
│   │       └── L75.cfg          # L75 engine (planned)
│   │
│   ├── 📁 Models/               # 3D models for engines
│   │   ├── 📁 S-Series/
│   │   │   ├── 📁 S10/
│   │   │   │   ├── S10.mu       # 3D model mesh
│   │   │   │   └── S10.dds      # Texture files
│   │   │   ├── 📁 S20/
│   │   │   ├── 📁 S23/
│   │   │   ├── 📁 S30/
│   │   │   ├── 📁 S31/
│   │   │   ├── 📁 S33/
│   │   │   ├── 📁 S40/
│   │   │   ├── 📁 S43/
│   │   │   ├── 📁 S44/
│   │   │   └── 📁 S50/
│   │   │
│   │   ├── 📁 N-Series/
│   │   │   ├── 📁 N04/
│   │   │   ├── 📁 N09/
│   │   │   └── 📁 N90/
│   │   │
│   │   └── 📁 Liquid/
│   │       └── 📁 Arion/
│   │
│   ├── 📁 FX/                   # Visual effects
│   │   ├── Waterfall_S-Series.cfg    # Waterfall plumes for solid motors
│   │   ├── Waterfall_Liquid.cfg      # Waterfall plumes for liquid engines
│   │   └── Waterfall_MLBR.cfg        # Waterfall plumes for MLBR motors
│   │
│   └── 📁 Flags/                # Mod-specific flags
│       └── BrazilianEngines/
│           └── BrazilianEngines.png  # Mod flag texture
│
├── 📁 Resources/                # Shared resources
│   └── Textures/                # Common texture assets
│
├── 📄 TechTree.cfg              # RP-1 tech tree integration
├── 📄 TestFlight.cfg            # TestFlight reliability data
├── 📄 ENTRYCOST.cfg             # Entry cost configurations
├── 📄 WaterfallFX.cfg           # Master Waterfall configuration
├── 📄 CommNet_Sites_RSS.cfg     # Real Solar System CommNet sites
├── 📄 Sites_RSS.cfg             # Launch sites for RSS
├── 📄 Config.cfg                # General mod configuration
└── 📄 .version                  # Version file (CKAN compatible)
```

## File Organization Principles

### Part Definition Files (.cfg)

**Naming Convention:**
- Engine configurations: `<ENGINE_SERIES>.cfg` (e.g., `S20.cfg`, `Arion.cfg`)
- Shared configs: `_<SERIES>_Shared.cfg` (underscore prefix for ordering)
- Integration configs: `<SYSTEM>.cfg` (e.g., `TechTree.cfg`, `Waterfall.cfg`)

**File Grouping:**
- Engines of the same series grouped in single file or subfolder
- Visual effects (Waterfall) separated from engine definitions
- RP-1 integration in dedicated TechTree file
- Localization strings in Localization folder

### 3D Model Organization

**Structure:**
```
Models/
├── <SERIES>/            # One folder per series
│   ├── <ENGINE_ID>/     # One folder per engine variant
│   │   ├── model.mu     # Mesh file
│   │   └── texture.dds  # Texture file(s)
```

**Benefits:**
- Easy to locate specific engine models
- Simple texture management
- Clean scaling with new engines

### Configuration Files

**Position:** Root of `GameData/BrazilianEngines/`

**Why at root?**
- Easier to find and modify
- Standard KSP mod practice
- Better compatibility with CKAN patching
- Simpler for users to customize

**Files:**
- `TechTree.cfg` - RP-1 integration (stays here, critical)
- `Waterfall.cfg` - Visual effects (stays here)
- `TestFlight.cfg` - Reliability data (stays here)
- `ENTRYCOST.cfg` - Entry costs (stays here)

## Localization System

### Files
- `Localization/en-us.cfg` - English (US) strings
- `Localization/pt-br.cfg` - Portuguese (Brazil) strings

### Naming Convention
All strings use prefix: `#autoLOC_BEng_`

**Examples:**
```
#autoLOC_BEng_S10_1_Name = S10-1 Solid Motor
#autoLOC_BEng_S10_1_Desc = Description...
#autoLOC_BEng_Arion_Name = Arion Liquid Engine
```

## Future Expansions

### Planned Structure Changes
1. **Additional Languages** - es-es, de-de, fr-fr, ru-ru
2. **Documentation** - Move docs to dedicated folder
3. **Testing Assets** - Test scenarios and configurations
4. **Compatibility** - CrossFeed, Kerbalism, etc.

### New Engine Series
- **L-Series (Liquid)** - Will follow Liquid subfolder structure
- **Future MLBR variants** - Will follow N-Series structure

## Maintenance Guidelines

### Adding New Engines
1. Create engine definition file in appropriate series folder
2. Add 3D models to `Models/<SERIES>/<ENGINE_ID>/`
3. Add localization strings to both `en-us.cfg` and `pt-br.cfg`
4. Add Waterfall effects to `Waterfall_<SERIES>.cfg`
5. Add RP-1 tech tree entry to `TechTree.cfg`
6. Update CHANGELOG.md

### Updating Localization
1. Edit `Localization/en-us.cfg` for English
2. Edit `Localization/pt-br.cfg` for Portuguese
3. Use consistent prefixes: `#autoLOC_BEng_<ENGINE>_<TYPE>`
4. Keep descriptions between 50-150 characters for UI fit

### Version Management
- Update `.version` file with new version number
- Update `CHANGELOG.md` with release notes
- Tag commits with version in main branch

## Best Practices

✅ **DO:**
- Keep engine series together logically
- Use meaningful filenames
- Separate concerns (parts, FX, config)
- Add comments to complex configs
- Maintain localization consistency
- Test cross-platform (Windows/Mac/Linux)

❌ **DON'T:**
- Create deeply nested directories (>3 levels)
- Mix multiple engine types in one file
- Disable features with `.DISABLED` extension (delete or document)
- Commit untested configurations
- Forget to update localization

## Quick Reference

| Type | Location | Format |
|------|----------|--------|
| Engine parts | `Parts/Engines/<SERIES>/` | `.cfg` |
| 3D Models | `Parts/Models/<SERIES>/<ENGINE>/` | `.mu` + `.dds` |
| Textures | `Parts/Models/<SERIES>/<ENGINE>/` | `.dds` |
| Waterfall FX | Root or `Parts/FX/` | `.cfg` |
| Localization | `Localization/` | `.cfg` |
| Tech Tree | Root | `.cfg` |
| Version | Root | `.version` |
| License | Root | `.txt` |

---

**Last Updated:** 2026-09-07  
**Version:** 1.2.0 "Programa Sonda"  
**Maintainer:** Cross Space Team
