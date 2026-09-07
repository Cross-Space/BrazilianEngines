# BrazilianEngines v1.2.0 "Programa Sonda" - Installation Guide

## Quick Start

### Requirements

**Minimum:**
- Kerbal Space Program 1.8.0+
- Realism Overhaul
- ROEngines
- Real Solar System (RSS)

**Recommended:**
- RP-1 (Career mode integration)
- Waterfall/ROWaterfall (Visual effects)
- Real Fuels (Propellant management)
- Module Manager (Configuration patching)

### Installation Steps

1. **Download the mod**
   - Visit [Releases page](https://github.com/Cross-Space/BrazilianEngines/releases)
   - Download `brazilianengines-v1.2.0.zip`

2. **Extract to GameData**
   - Extract the `.zip` file
   - Copy `BrazilianEngines` folder to `KSP/GameData/`
   - Result: `KSP/GameData/BrazilianEngines/`

3. **Verify Dependencies**
   - Ensure ROEngines is installed
   - Ensure Realism Overhaul is installed
   - Ensure Real Solar System is installed

4. **Launch KSP**
   - Start the game
   - Select your save (recommended: RSS+RP-1 mode)
   - Verify Brazilian engines appear in VAB/SPH

## Directory Verification

After installation, your structure should look like:

```
KSP/
└── GameData/
    ├── BrazilianEngines/
    │   ├── Localization/
    │   ├── Parts/
    │   ├── Flags/
    │   ├── TechTree.cfg
    │   ├── Waterfall.cfg
    │   └── ...
    ├── ROEngines/
    ├── RealismOverhaul/
    ├── RealSolarSystem/
    └── ...
```

## Configuration

### Language Selection

BrazilianEngines automatically detects your KSP language:

**English:** Strings from `Localization/en-us.cfg`
**Portuguese (Brazil):** Strings from `Localization/pt-br.cfg`

To change manually:
- Edit `KSP/settings.cfg`
- Find `LANGUAGE = English` section
- Change to preferred language

### RP-1 Integration

BrazilianEngines fully supports RP-1:

- Engines appear in correct tech tree nodes
- Entry costs and unlock requirements apply
- TestFlight reliability data included
- Historical availability dates respected

**Optional:** Customize entry costs by editing:
```
GameData/BrazilianEngines/ENTRYCOST.cfg
```

### Waterfall Effects

If Waterfall is installed, visual effects automatically apply.

**Disable Waterfall effects:**
- Rename `GameData/BrazilianEngines/WaterfallUnified.cfg` to `.DISABLED`
- Restart KSP

**Customize effects:**
- Edit `GameData/BrazilianEngines/WaterfallUnified.cfg`
- Modify scale, position, or template values
- Restart KSP to see changes

## Troubleshooting

### Engines Not Appearing

**Check:**
1. Folder structure is correct
2. All dependencies installed and up-to-date
3. No mod conflicts (check debug output)
4. Module Manager processed configs correctly

**Debug:**
```bash
# Check KSP logs
KSP/KSP_Data/output_log.txt
```
Look for errors related to BrazilianEngines

### Localization Issues

**Strings appear as #autoLOC_BEng_... ?**
- Module Manager may not have processed configs
- Try installing Module Manager
- Check that localization files exist in `Localization/` folder

**Portuguese not appearing?**
- Verify `pt-br.cfg` exists
- Check KSP language is set to Portuguese
- Verify no file naming errors

### Performance Issues

**If experiencing lag/stuttering:**
1. Disable Waterfall effects (see above)
2. Reduce texture quality (optional)
3. Check for mod conflicts
4. Update to latest KSP version

### Compatibility Issues

**With RP-1:**
- Ensure RP-1 is loaded AFTER BrazilianEngines
- Check tech tree patch loads correctly
- Verify no duplicate engine definitions

**With other mods:**
- Check for conflicting part names (BRA-*)
- Load order: BrazilianEngines → RO → RP-1
- See COMPATIBILITY.md for details

## Uninstallation

To remove the mod:

1. Delete `GameData/BrazilianEngines/` folder
2. Remove any related mod entries in save files (optional)
3. Restart KSP

## Advanced Configuration

### Custom Cost/Entry Costs

Edit `GameData/BrazilianEngines/ENTRYCOST.cfg`:

```cfg
@PART[BRA-S20]:FOR[xxxRP0]
{
    %cost = 45          // Part cost (fund)
    %entryCost = 2000   // Unlock cost (science)
}
```

### Tech Tree Customization

Edit `GameData/BrazilianEngines/TechTree.cfg` to move engines between tech nodes.

### TestFlight Customization

Edit `GameData/BrazilianEngines/TESTFLIGHT.cfg` to adjust reliability values.

## Support

**Issues or Questions?**
- Open an issue: [GitHub Issues](https://github.com/Cross-Space/BrazilianEngines/issues)
- Check existing issues first
- Include KSP version, mod list, and error logs

**Want to Contribute?**
- See [CONTRIBUTING.md](CONTRIBUTING.md)
- All contributions welcome!

## Version History

- **1.2.0** (2026-09-07) - "Programa Sonda" - Localization, restructuring
- **1.0.0-unified** (2025-11-30) - Unified configurations
- **1.1.0** (2025-10-21) - "Sonda" release
- **1.0.0** (2025-08-26) - Initial release

## License

MIT License - See [LICENSE](LICENSE) file

---

**Enjoy Brazilian rockets in KSP! 🇧🇷🚀**
