# Windows 11 Changelog
## Windows 11 v2.0.0
After some hours of planning and some coding, just decided to do a quick backup of the bare bones of the project.

Originally called v2.0.0.0, replaced because it was too much zeroes...

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

## Windows 11 v2.1.0
Added a few improvements. Changed version system from vX.X.X.X to vX.X.X (4>3 digits).

Organized code positioning. Moved changelog from the README to its own file, CHANGELOG.md.

## Build
The HTML Build (made with TurboWarp Packager), now includes a Page Icon and a Loading Screen Background.

## Code
* BIOS
  * Removed the black background (but moved to Windows 11).
  * Added Project Stopping Detection.
  * Added the `bios.shutdown()` function, to shutdown the project properly and save data.
  * Added the `bios.os.shutdown(osname)` function, for the os to shutdown its own way.
  * Added the `bios.forceshutdown()` function to completely stop the project instantly.
  * Made the bios start with the `bios.start()` function, which runs when the green flag is pressed (Done so the project can be restarted).
* Windows 11
  * Added the black background, replacing the main script to avoid it disappearing when the shutdown is forced.
  * The main script with the logo was moved to a clone.
  * The logo is able to properly disappear if the project is stopped too quickly.
  * Added the `windows11.clone?` variable to let know if the current script is a clone (for broadcasts).

## Windows 11 v2.1.1 (Future Release)
The objective of this future release will be on adding a background to the Scratch project and for when the project is stopped, just like with our previous project [Scratch Windows 11 Online Simulator](https://scratch.mit.edu/projects/1027133381/).