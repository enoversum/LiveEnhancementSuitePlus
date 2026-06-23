# LiveEnhancementSuite Plus
**Live Enhancement Suite (LES)** updated for Live 12.3+ with 3 new added keybinds, better timings and new functionality.

## Improvements: 
* Compatible with Live 12.3 and above via **improved right-click menu search routine** that works again with better timings.
* The optional **closing of the browser** after a search is now realised via the _Ctrl + Alt + B_ shortcut instead of previously via mouse click with coordinates (which tended to fail). The setting for this (resetbrowsertobookmark) is still respected, coordinates aren't.
* **Buplicate** has a new shortcut (Ctrl + Shift + B) to allow for Bouncing to new track via Ctrl + B.
* **Clear track** (remove all clips from currently hovered track) via Alt+X is now working in Live 12.3 again. Due to AHK not being able to determine the exact point release version, this will not work Live 12.x versions before 12.3. 

## New features:
* **Icons:** Add icons to the left-hand column for select (or all) menu items. 
    * If enabled, you can add tiny icons to the left of a menu item. The menu with icons takes slightly longer to load up if `dynamicreload` is active.
    * Place `.ico` or `.png` files inside an `icons` folder in your main LES directory. 
    * Files should be small (performance!) and best designed as squares (16x16px).
    * PNG is sometimes tricky regarding transparency. Best use `.ico` files for full transparency support.
    * Add an icon by referencing it in square brackets in front of a menu item name. Example: If the file is called `synth.png` or `synth.ico`, you would write your menu item's first line like this: `[synth] Serum 2`.
    * `settings.ini` needs a new setting `enableicons` set to `1` (see default `settings.ini`). If the option is set to `0` or doesn't exist, LES disables the feature.
* **Close and fold:** Closing the window after loading the device (VST2/VST3 only), and folding the mini window in the device chain at the bottom. Can be used together or individually. Just add ` -close` and/or ` -fold` (with a leading space) to the second line of your entries in `menuconfig.ini`. Both are optional.
    * `-close` can be overridden when loading a plugin by holding the Shift button while clicking the corresponding menu item. 

Example entry for a plugin:

    Arturia Pigments
    Pigments vst3 -close
  
_Pigments closes after loading_

    Arturia Pigments
    Pigments vst3 -fold
  
_Pigments' window in device view folds after loading_

    Arturia Pigments
    Pigments vst3 -close -fold
  
_Pigments closes and folds after loading_

Disclaimer: This is an update to make LES work great again *cough* on Live 12.3 and above. I'm not a hardcore AHK developer. But please let me know if you're facing any issues. 

Link to original: https://github.com/LiveEnhancementSuite/LESforWindows
