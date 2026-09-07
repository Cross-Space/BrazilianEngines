# Changelog

All notable changes to BrazilianEngines will be documented in this file.

## v1.2.0 - "Programa Sonda" - 2026-09-07

### ✨ Features
- New solid motors S10-1 and S10-2
- Custom 3D models for S-series engines (S20, S23, S30, S31, S33, S40, S43, S44)
- Enhanced CommNet RSS support with Sites_RSS.cfg file
- Improved file structure organization for better compatibility
- CommNet sites integration for Real Solar System

### 🔧 Improvements
- Renamed Sites.cfg to Sites_RSS.cfg for clarity and better RSS compatibility
- Added CommNet_Sites_RSS.cfg for seamless Real Solar System integration
- Removed duplicate structures and unused configurations
- Repository cleanup (removed North_Iran_Engines directory)
- Consolidated engine configurations for better maintainability

### 📋 Commits Included
- dd433d6 Add CommNet_Sites_RSS.cfg file (Cross Aerospace, 2026-09-07)
- 13820ac Rename Sites.cfg to Sites_RSS.cfg (Cross Aerospace, 2026-09-07)
- 225a3c7 Add engines and 3D models for S-series engines (Cross Aerospace, 2026-09-07)
- 756ec7c Delete GameData for great update (Cross Aerospace, 2026-09-07)
- cc6001f Delete GameData/North_Iran_Engines directory (Cross Aerospace, 2026-09-02)

### 📦 Assets
- brazilianengines-v1.2.0.zip

### 📥 Installation
1. Download the latest asset from this release.
2. Extract the folder into your KSP `GameData` folder.
3. Ensure all dependencies are installed:
   - ROEngines
   - Realism Overhaul
   - Real Solar System
4. Launch KSP and enjoy the new engines!

### ⚠️ Important Notes
- Test in a separate KSP profile before using on main saves
- Custom 3D models may still be undergoing fine-tuning
- Future releases will bring liquid engines (L5, L15, L75) and MLBR program engines

### 🔮 Roadmap
- Integration of Brazilian liquid rocket engines (L5, L15, L75)
- MLBR Program solid motors (N04, N09, N90)
- Arion liquid engine configuration
- Complete RP-1 tech tree integration
- Enhanced engine descriptions with historical context

---

## v1.0.0-unified - 2025-11-30

This release consolidates TechTree and Waterfall templates and removes per-engine fragments.

### 📋 Commits Included
- ec8e530 Docs: document unified configs and mark as definitive (add README note and headers) (Cross Aerospace, 2025-11-30)
- cb09ab0 Finalize unified configs: fix TechTree syntax and mark unified TechTree/Waterfall as definitive (Cross Aerospace, 2025-11-30)
- 38da747 Merge pull request #4 from Cross-Space/fix/move-unified-files (Cross Aerospace, 2025-11-30)
- 6aa8fcb Remove duplicate WaterfallUnified.cfg in Engines/ (keep single copy under GameData/BrazilianEngines) (Cross Aerospace, 2025-11-30)
- c81938b Move unified TechTree to GameData/BrazilianEngines and remove duplicate Waterfall copy (Cross Aerospace, 2025-11-30)

### 📦 Assets
- brazilianengines.zip (SHA256: 4a9308b512fd545eef66e01739dfe26bb13696f2ba4e8250c99df8f839860fcb)

### 📥 Installation
1. Download the asset from the release.
2. Extract the folder into your `GameData` folder.
3. Ensure dependencies are installed:
   - ROEngines
   - Realism Overhaul
   - Real Solar System

### ⚠️ Notes
- Test in a separate KSP profile before using on main saves

---

## v1.1.0 - "Sonda" - 2025-10-21

[View full changelog](https://github.com/Cross-Space/BrazilianEngines/compare/v1.0.0...v1.1.0)

---

## v1.0.0 - "21 Heroes of Alcântara" - 2025-08-26

Initial release presenting a collection of Brazilian rocket engines for KSP RP-1.

**Dedicated to the 21 heroes of Alcântara** 🇧🇷

This release introduces:
- Real and fictional Brazilian rocket engines
- Integration with Realism Overhaul and Real Solar System
- Tribute to Brazil's space program heritage

[View full release](https://github.com/Cross-Space/BrazilianEngines/releases/tag/v1.0.0)