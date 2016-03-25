less documented fixes for issues I've encountered that were headaches:

no feed from extruder - check for blockage (manually feed filament with head at higher than typical temp), ensure nozzle and peek tube are attached correctly, ensure stepper voltage is correct (mine is around 0.48V), ensure the drive gear is attached sufficiently/not sliding around, etc

clicking from extruder - check stepper voltage, play with tension on extruder idler (less is more, playing with mod ideas for this next because it is a pain to set perfectly), check for partial blockage

inversion of axes during homing procedure - check that endstop logic is correct with M119 and invert in config.h if needed

abl ignores z-offset - ensure endstop logic is correct, ensure software endstops are off, check eeprom settings with M501 - if there is a z-offset in eeprom it supercedes firmware

adjusting stepper drivers - i have a small all metal eyeglass screwdriver that I alligator clip to my + MM probe, this way I can read the value as i adjust the voltage  
