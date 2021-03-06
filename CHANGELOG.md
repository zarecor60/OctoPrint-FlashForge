# OctoPrint-FlashForge Changelog

## 0.1.18 (2020-5-15)
### New Features
* Allow connection to FlashForge Guider IIs (Thanks @jayceekeys)
### Fixes
* Support Python 3
* Disable light controls when printing from SD

## 0.1.17 (2020-5-13)
### New Features
* Controls for the enclosure light added to the "Control" tab
### Fixes
* Now it should actually support .3drem files for Dremel printers...
* Support M146 command for controlling LED lights (see [Wiki](https://github.com/Mrnt/OctoPrint-FlashForge/wiki/G-Code-Dictionary#m146---control-enclosure-lights)) for docs)

## 0.1.16 (2020-5-8)
* Support .3drem files for Dremel printers
* Fix for hanging when DisplayLayerProgress plugin is in use (Thanks @jumpingmushroom)

## 0.1.15 (2020-5-4)
* Fixes for issues uploading to SD card on newer printers such as Finder v2 (Thanks @boozecouncil)

## 0.1.14 (2020-4-30)
* Fixes for USB connection issues on newer printers such as Finder v2 (Thanks @boozecouncil)

## 0.1.13 (2020-4-16)
* Added additional support for PowerSpec Ultra 3D (Thanks @kelkin)

## 0.1.12 (2020-4-16)
* Added support for FlashForge Finder v2 (Thanks @Spillmaker)

## 0.1.11 (2020-4-2)
* Added support for FlashForge Creator Max (Thanks @pfemiani)

## 0.1.10 (2020-2-9)
* Set USb buffer to a sensible size

## 0.1.9 (2020-1-15)
* Corrected version number in setup file

## 0.1.8 (2020-1-14)
* **Changes to default settings and initial connection handling -
check the configuration section and ensure the "Hello" command is set**: Go to Settings and under Serial Connection > Firmware & Protocol >Protocol fine tuning: open up the "Advanced" section and set the value for "Hello" command to `M601 S0`
* Made upload to SD card more robust
* Made pausing/resuming/canceling SD card printing more robust
* Tested on
  * FlashForge Finder Firmware: V1.5 20170419
  * FlashForge Dreamer Firmware: V2.6 20190320
  * PowerSpec Ultra 3D Firmware: V2.4 20160407

## 0.1.7 (2019-12-9)
* Added support for Dreamer NX (Thanks @mrspartak)
* Support VID 0x0315 as PowerSpec (Thanks @twistedcustomdevel)

## 0.1.6 (2019-12-9)
* Support FlashForge VID 0x0315 (Thanks @twistedcustomdevel)

## 0.1.5 (2019-10-10)
* Support FlashForge Inventor

## 0.1.4 (2019-09-08)
* Updates to README
* Set default values for settings we care about
* Fix bug causing timeout when reading from USB port

## 0.1.3 (2019-09-03)

* Support for OctoPi/Linux (where USB access requires OS permission)
* Automatically install `libusb1` if missing

## 0.1.2 (2019-09-03)

* Detect two versions of FlashForge Finder
* Pausing/Cancelling the print triggered by "Upload to SD Card" should now work
* **NB: Printing still only supported via "Upload to SD Card" button!**

## 0.1.1 (2019-08-01)

* Automatically detect printer (no hardcoding of USB ID's)
* Initial support for "Upload to SD" button: requires .gx file prepared using FlashPrint, print starts after upload **NB Pause, Cancel buttons do not work!**

## 0.1.0 (2019-06-01)

Initial commit:

* Connect to printer if USB ID matches hard coded ID
* Monitor & set temperatures
* Move extruder, bed
* Turn fan on/off
