# Alfawise_U30_Pro_Screen_FW

This repository contains the screen UI of Alfawise U30_Pro and its development software. The UI was written by LONGER.

It also hosts the compiled motherboard firmware. Firmware sources are available [there](https://github.com/LONGER3D/Marlin1.1.9_LGT0.3.x_Alfawise_Ux0Pro).

## Screen_software_guide

This folder includes screen development software and development documentation.

You can use screen development software to add features to your printer. But you must first read the development documentation carefully.

## Alfawise_U30_Pro_Screen_Project

This folder includes U30_Pro Screen UI source code. 

## U30_Pro_UI_FW

This folder includes :

- UI_FW_U30_PPO_AFW_V0.3.0.zip : screen UI firmware
- U30_Pro_LGT0.3.1.hex : motherboard firmware.

If you want to reset your machine to factory settings, you can use them.

For how to download the UI to the screen, you can carefully read the SD Interface on the tenth page of the development document.

## Notes for correct deploy on screen
DGUS Tool will generate `14变量配置文件.bin` and `13触控配置文件.bin` that **must be renamed** to something like `14_var.bin` and `13_touch.bin` otherwise the LCD will not load the new firmware correctly (seems loads only BMPs files)

BMPs files by default are generated in portrait in the DWIN_SET folder, this mean that before loading it to the U30/LK4 Pro LCD you must be sure that all images are rotated by 90°, you can use windows folders picture tools to do that in batch or the "SaveAs" function of DGUS Tool, look at U30_Pro_UI_FW folder of this repo for an example
