very basic and ugly script to allow you to flash marlin from inside OctoPrint.

install avrdude (sudo apt-get install avrdude)
copy flash_marlin somewhere (I use ~/OctoPrint/scripts)
edit SOURCEDIR to reflect your username
edit MARLINHEX to reflect the name of your marlin hex file
make it executable (chmod +x)

edit config.yaml (sudo nano ~/.octoprint/config.yaml) and add the following to the system section:
  - action: flash
    command: ~/path/to/flash_marlin
    confirm: You are about to flash Marlin, ensure up-to-date hex is in SOURCEDIR
    name: Flash Marlin


restart octoprint or the computer

to use: scp marlin.hex into sourcedir, click system in octoprint, click flash, etc. Probably smart to run it from cli once to see output and make sure it’s working - I don’t know how to pass script messages to octoprint so if it fails it just does nothing (most situations it would just leave the octoprint service dead but I don’t know how well that works). If you get a port error you may need /ttyUSB0 instead of ACM0 - raspbian/octopi uses ACM0 but other releases use USB0. 

to make a hex file: 
on OS X preferences for arduino IDE 1.6.7 is /users/name/Library/Arduino15/preferences.txt
open and add line build.path=/Users/name/path/to/hex/output
save and restart IDE - compile/check and compilation will output to path established above. Use MFMarlin.ino.hex with above instructions assuming you’ve cloned my git. don’t use eep, elf, or with_bootloader.hex.

edit: added a line to flash eeprom_clear before flashing marlin. Was having issues with persistant EEPROM values between flashing. I generally hardcode all of my settings into firmware so this isnt a huge deal but if you don't you should comment out the line about eeprom_clear.hex. the eeprom_clear code is part of the arduino ide so you can grab it from the examples lib
