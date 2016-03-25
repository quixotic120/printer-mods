these aren't mods but they were a total pain in the butt to find so I figured I'd throw them up here
42BHH48-151K-24B is my stepper for the extruders - 4.2V 1.8deg 1.5A stepper
35BHH37W-099A-21 is my stepper for everything else - 2.7V 1.8deg 1.0A stepper

vref- I aim for 70% max current to ensure heat is under control and have not had issues
polulu a4988 - vref = tripmax * 8 * (0.05) = max 0.4 vref for 1.0A motors, 0.6 vref for 1.5A motors
DRV8825 - vref = tripmax/2 = max 0.5v for 1.0A, max 0.75v for 1.5A 
stepsticks - vref = tripmax * 1.6 = 1.6v for 1A - maxed out. can change s1,s2 to 0.1ohm, r1 to 30k, and remove and short r4 (or 0k replacement). this will raise max to 1.5A



