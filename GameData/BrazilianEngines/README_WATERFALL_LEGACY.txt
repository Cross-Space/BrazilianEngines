Brazilian Engines legacy Waterfall note
======================================

Waterfall_New.cfg has been disabled in v0.9.

Reason:
- The active visual effects are now handled by WaterfallUnified.cfg using ROWaterfall-style template assignments.
- Waterfall_New.cfg used direct ModuleWaterfallFX patches and :FOR[RSMP], which could create duplicated effects or accidentally declare RSMP in ModuleManager.
- The file is preserved as .cfg.DISABLED for reference only and is not loaded by KSP/ModuleManager.
