# Windows 11 v2 in Scratch
A program for Scratch resembling Windows 11, full of features and regular updates.

# IMPORTANT NOTICE
This repository is licensed under the MIT License. Third-party assets (including Scratch's sprites, sounds or any) remain subject to their original licenses and are property of their respectful owners.

# Other (non-Scratch) versions
Our idea is to bring additional features to Windows via Turbowarp extensions like gamepad support, resolution and fullscreen handlers, better internet connection and way more.

Also, thanks to the Turbowarp Packager, we will also be releasing HTML versions of the project for the TurboWarp and Scratch releases for it to be faster, better and easier to use.

# Project Timeline
* BIOS
  * BIOS OS Loading
  * BIOS Disk Loading
  * BIOS Gamepad Support (Turbowarp Release)
  * BIOS Configuration
* Windows 11
  * Installation Page
  * Wallpapers
  * Taskbar
    * Time / Date
    * Start Menu
    * Pinned Apps (Calculating taskbar space)
   
More stuff coming sonn once some objectives are completed!

# Changelog
## Windows 11 v2.0.0.0
After some hours of planning and some coding, just decided to do a quick backup of the bare bones of the project.

I just realized that it haves too much zeroes.

### New Features
* BIOS
  * Screen
    * Horizontal Resolution (By moving to the corner of the screen, with a fallback using the `Touching Edge` block when `Fencing` is disabled in TurboWarp / Forkphorus)
    * Vertical Resolution (Same as above)
  * Stats
    * Framerate (By counting for 1s, taking into account some delay because of how the program is designed)
    * Delta Timer (By comparing the BIOS's last update)
  * Time
    * Timezone detection (By comparing `Days since 2000` and your current hour, prepared for weird cases)
    * Global Time (`Days since 2000`)
    * Local Time (`Days since 2000`, but taking the timezone into account)
    * Last BIOS Update (The last time, using the global time, a frame was recorded)
  * Internal
    * Frame (Frames completed that second)
    * LastFrameUpdate (Last time framerate was updated)
  * Background
    * The BIOS includes a black background that resizes based on the screen resolution
    * Scaled to 1.1x to avoid errors found in TurboWarp
* MAINDISK
  * A plan for the future to make Disks to store data downloaded from a server
  * Logo based on MacOS's External Disk Icon
* Windows 11
  * The Windows Logo just appears
    * Size based on Real-Time Screen Size
    * Animation prepared for lag / different FPS (Like 60FPS mode in Turbowarp)
