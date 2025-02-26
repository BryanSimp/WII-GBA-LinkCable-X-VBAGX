# GBA Link Cable Dumper
A Nintendo Gamecube (GC) and Wii Homebrew App to get Game Boy Advance (GBA) BIOS, ROMs and saves via the GC GBA Link Cable.
Credits goes to the orignal creator [https://github.com/DamianS-eng/wii-gba-link-cable-dumper](https://github.com/FIX94/gba-link-cable-dumper)

## Features
1. Lightweight app launched from a [Homebrew Launcher](https://www.gc-forever.com/wiki/index.php?title=Booting_homebrew#Active_Products), such as the Picoboot or SD Media Launcher on Gamecube, or the Homebrew Channel on Wii.
1. Read physical Game Boy Advance cartrige inserted into a Game Boy Advance (SP) console connected via the Gamecube Game Boy Advance Link Cable.
1. Dump the GBA ROM to the same storage device as the loaded app.
1. Backup save data from cartridge.
1. Restore save data backup to catridge.
1. Erase save data from cartridge.
1. Dump the GBA console BIOS.

# How to Use
1. Grab the release from the [releases](https://github.com/DamianS-eng/wii-gba-link-cable-dumper/releases) tab and extract the folder and the correct dol file for the GC/Wii to your Homebrew Loader.
   - Usually this is the `apps` folder on the SD card.
1. Before launching the app in your Homebrew Launcher, make sure to sync your Wii Remote, or plug in a GC Controller into Port 1 of your console, and the GBA Link Cable into Port 2.
1. Now Boot your GBA without a cart inserted, it should automatically boot into the dumper when connected. From there you can just follow the instructions on screen.  
  - If your GBA resets when you get to the step of inserting a cart, try to boot your GBA with the cart already inserted and holding down `Start + Select` when you see the Game Boy splash screen. This suspends the game launch and should allow the dumper to boot up from there.

# VBAGX
1. This version uses VBAGX to play the games and be able to send and recieve files to
1. Here is the download for VBAGX ([https://github.com/dborth/vbagx](https://github.com/dborth/vbagx))
1. It takes a while to get the ROMS uploaded so it is easier to put them on ahead of time however they have to follow this format
1. NAME(all caps) [GAME ID].gba EX. POKEMON RUBY [AXVE01].gba

## Dump Notes

- The `bin`, `gba` and `sav` files dumped will be placed in a folder called "dumps" or under "vbagx" on your main device (from where the loader launched).
- Please note that dumping GBA ROMs can take a long time because of the cable protocol limitations. An estimation will be displayed on screen before you dump it as a reference. File sizes vary by GBA rom.
  - 4mb takes about 6 minutes.
  - 16mb takes about 26 minutes.
  - 32mb takes about 48 minutes.
  - ROM sav and BIOS backups are very quick.

# Compile

1. Grab the latest .zip from the master branch using `git clone`.
1. Run the `build.bat` script.
- If there are compiler issues, ensure the latest dependencies are installed `pacman -syuu`, and make sure you clean between compiles (`make clean`, refer to [build.bat]([https://github.com/DamianS-eng/wii-gba-link-cable-dumper/blob/Readme-update/build.bat](https://github.com/DamianS-eng/wii-gba-link-cable-dumper/blob/master/build.bat) for specific commands).

If you are using version 3.0.3 of devkitPro you will not be able so compile unless you have the packages
ppc-bzip2 and ppc-zlib 
use pacman -S ppc-bzip2 and pacman -S ppc-zlib
to install if you want to compile a new version of the code

# Credits

Latest gba header changes by yuv422.

Save Support based on SendSave by Chishm. 

GBA BIOS Dumper by Dark Fader.

Wii Remote support added by DamianS-eng.

VBAGX support added by BryanSimp
