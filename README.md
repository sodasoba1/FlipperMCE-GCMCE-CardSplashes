# FlipperMCE-GCMCE-CardSplashes

SD Card layout for FlipperMCE/GCMCE card splash `.bin` files (OLED images).

## Quick Start
This repository provides a pre-configured `.bin` and `.ini` file structure for a basic SD card setup. 

> [!IMPORTANT]
> I strongly recommend reading the official documentation at [flippermce.github.io](https://flippermce.github.io/) before starting.

## Regional Syncing & Automation
To provide maximum compatibility across libraries, this collection uses an automated "Master Template" system:
* **Primary Source:**  splashes are created for the **NTSC-U (USA)** region.
* **Cross-Region Compatibility:** Using Python automation, these USA assets are synced across **PAL (EUR/UKV)** and **NTSC-J (JPN)** folders.
* **Redundancy:** Each folder includes both the primary `.bin` and a `-1.bin` redundancy file to ensure the splash displays correctly regardless of your file naming convention.

## Image Sources & Processing
Original images (before conversion) are located in `/CardSplashes-prebin`. 
* **Enhancements:** Many images have been manually edited to improve contrast, crispness, and legibility on small OLED screens.
* **Conversion:** Files were generated using the [FlipperMCE Splash Generator](https://flippermce.github.io/splashgen/splashgen.html).

## ❤️ Special Thanks
A huge thanks to [bbsan2k](https://github.com/bbsan2k) and [ManCloud](https://github.com/ManCloud) for creating such a fantastic piece of hardware!