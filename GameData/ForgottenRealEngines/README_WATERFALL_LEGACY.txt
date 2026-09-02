ForgottenRealEngines legacy plume note
======================================

Plume_Unified.cfg and Waterfall_Avio.cfg have been disabled in v0.9.

Reason:
- The active ForgottenRealEngines effects are now handled by WaterfallUnified_Vega.cfg using ROWaterfall-style templates.
- Plume_Unified.cfg used RealPlume/SmokeScreen PLUME blocks and :FOR[RealPlume], which could conflict with the Waterfall-only integration target.
- Waterfall_Avio.cfg used direct ModuleWaterfallFX / RSMP-style patches. It is preserved as .cfg.DISABLED for reference only.
