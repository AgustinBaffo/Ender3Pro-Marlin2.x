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

