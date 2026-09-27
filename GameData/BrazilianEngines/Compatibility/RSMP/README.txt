BrazilianEngines - RSMP Compatibility
========================================

Install this file at:

GameData/BrazilianEngines/Compatibility/RSMP/RSMP_Compatibility.cfg

Requirements:
- BrazilianEngines
- RSMP
- Waterfall

This compatibility patch is deliberately limited to BrazilianEngines' Brazilian SRB parts.
It reuses the templates already provided by RSMP:
- srb-waterfall
- lemon-SRB-core

It does not include or redistribute RSMP's assets, templates, sounds, or configs for other mods.

The patch removes the existing ModuleWaterfallFX from each targeted BrazilianEngines SRB
and creates a per-part ModuleWaterfallFX using the RSMP templates, preserving the
BrazilianEngines-specific transform positions and plume scales.

Liquid engines are intentionally not modified.


Load-order detail:
This patch uses :AFTER[ROWaterfall], so the native BrazilianEngines ROWaterfall configuration is processed first. The compatibility patch then removes the resulting ModuleWaterfallFX and installs the RSMP SRB template stack for BrazilianEngines SRBs only.
