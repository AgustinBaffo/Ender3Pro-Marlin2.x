# Ender 3 Pro "V1.5"

This is a surprise upgrade to the Ender 3 Pro that some customers began to receive around mid-July of 2020. No documentation or support page exists for this variant. It appears to be an Ender 3 Pro with the 32-bit Ender 3 V2 board and the stock Ender 3 Pro display. To see which version you have, examine the control board. The newer board is Creality v4.2.2.

This configuration is very similar to the Ender 3 V2 config except that the CR-10 stock display is enabled.

## Flashing Firmware

The bootloader which handles flashing new firmware on this board remembers the last filename you used.

Therefore, to flash the compiled firmware binary onto the board you must give the "`firmware.bin`" file on the SD card a unique name, different from the name of the previous firmware file, or you will be greeted with a blank screen on the next boot.

## Marlin 2.1.2

I am currently using Marlin 2.1.2 firmware. Marlin versions and their default configurations files can be downloaded [here](https://marlinfw.org/meta/download/).

## BLTouch

This configuration adds the necessary setup for the printer to work integrating a BLTouch probe. I used this [site](https://3dprintscape.com/marlin-firmware-on-creality-board-complete-guide/) to configure most of the settings.

## Quick build
1. Install VSCode and PlatformIO and Auto Build Marlin extensions (see [this reference](https://automatedhome.party/2020/05/08/compiling-marlin-firmware-is-easy-dont-be-afraid-to-do-it/))
2. Download from [bugfix-2.0.x.zip](https://marlinfw.org/meta/download/) (see [this referece](https://3dprintscape.com/marlin-firmware-on-creality-board-complete-guide/)).
3. Clone this repository: `git clone git@github.com:AgustinBaffo/Ender3Pro-Marlin2.x.git`.
4. Replace the content of `Marlin` folder from `bugfix-2.0.x.zip` with this repository.
```
rm -rf Marlin-bugfix-2.0.x/Marlin
mv Ender3Pro-Marlin2.x Marlin-bugfix-2.0.x/Marlin
```
6. Replace `Marlin-bugfix-2.0.x/platformio.ini` with `Marlin-bugfix-2.0.x/Marlin/extra/platformio.ini`
```
cp Marlin-bugfix-2.0.x/Marlin/extra/platformio.ini Marlin-bugfix-2.0.x/platformio.ini
```
5. Open `Marlin-bugfix-2.0.x` folder from VSCode PlatformIO extension and build from VSCode.

For mor info see reference guides from point 1 and 2.
