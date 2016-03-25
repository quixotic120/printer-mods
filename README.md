**Detailed above:**

Bed clips - modified and cheap bed clip to maximize printable area

Fan shroud - fan shroud for dual e3d on the pegasus with one 40mm fan

SSR - using a solid state relay with the heated bed to enable PID temp control

endstops - basic structural mods to stiffen the end stops up and make them more consistent. 

Power supply - wiring a switch and fuse in as well as a case and mounts

**Other mods I've done that are either basic or covered better elsewhere:**

Auto bed level - I basically followed [Zennmasters guide](http://zennmaster.com/random-things/auto-bed-leveling-for-the-makerfarm-prusa-i3-part-1-assembly-and-basic-setup). His STLs won’t work; I dont have an STL for my servo mount; I used colin's STL for the laser cut wood bit under the extruder along with the servo mount from [here](http://www.thingiverse.com/thing:735410/) . I didn't edit them, I just lay them on top of each other in my slicer until it looked right. Not the most reliable method but it worked well and was easy! the z-arm from that will be way too short though - there's a longer one on thingiverse but I found it too long. it's a fairly simple mesh so I had no problem turning it into a solid with 123D and stretching it to my preference but I accidentally deleted the STL after I printed. sorry! My z-arm about 58mm long - I would say you need a minimum of 52mm for this machine and that would be cutting it very close.

Lighting - not worth posting; literally just wired a few white LEDs to a switch and tapped the power supply, added a small perf board for constant 12V connection which I use for the lighting and the extruder fans. 

RAMPS fan - [simple mount for 80mm fan](http://www.thingiverse.com/thing:806125). You need two of them; I just wired it directly to 12v so it’s always on.

octopi - got a raspberry Pi zero by total dumb luck at micro center. Octopi is fairly simple and there are plenty of guides out there so I won’t cover it. I will say the following though: you need a nightly build for the zero as wheezy will not boot, the edimax ew-7811Un wifi adapter works well and is 10 bucks shipped on amazon, and wireless networks that have emoji in the SSID will not work with the autoconfig. 

Also if you need to diagnose an issue and can’t get ssh you can easily wire composite video as described [here](http://raspberrypi.stackexchange.com/questions/38812/pi-zero-video-out-header). saves you like 10-20 bucks on a stupid weird HDMI cable you will probably never use again. My pi is wired to a usb voltage drop down converter I had for a car (12v-5v) so it can be connected directly to the 12v PSU; don’t want too much load on the RAMPS board.

filament filter - [this is neat](http://www.thingiverse.com/thing:492067) but I’m not convinced that it actually does anything. It’s simple to print and takes like 10 minutes so whatever, why not!

wire management - using a ton of the plastic bits that fill the open channels on the extrusions plus a bunch of zip ties and spiral wrap. It's ugly but functional. Would love suggestions on this front.

**future plans**

camera for octopi + mount: I ordered [this] (http://www.amazon.com/gp/product/B00V8A6CSU?psc=1&redirect=true&ref_=oh_aui_detailpage_o04_s01) camera:
it’s a piece of garbage but its really cheap. It didn’t work when it arrived but when I cracked it open I found the red cable had lifted from the pad at the usb plug. To further confuse things it did power on and they were not using the correct color code. oh well.

soldered it back and it works with an okay picture and very bright lighting. the cable was extremely long so I shortened it significantly, wired the dimmer (wheel pot) in-line, and removed the PCB for the dimmer connecting everything directly to the USB male end. The PCB was garbage; the red cable kept coming up because solder would release from the pad under the smallest bit of force and outside of the trimpot there were no components on it (even though it was like 3” long!). Worked without drivers or software on OS X so I’m hoping for similar results on the Pi. Just need to find time to set it up.

Z axis screws: threaded rods are kind of crappy. inconsistent, loud, dirty, and not very straight. In the meantime I’ve printed [this z bracket](http://www.thingiverse.com/thing:769057). It’s not amazing but I prefer it to the makerfarm mount where the nut kept working itself out and messing up the extruder offsets.
I’m researching acme/lead screws and trying to determine if the cheap Chinese sets are worth the 30-50 bucks.



