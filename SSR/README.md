SSR + PID bed

Pros: 
more even heating of bed
less flex in bed
more precise temperature management
fairly simple

Cons:
Longer to heat up
a bit expensive

needs:
DC-DC solid state relay sufficient for your bed (10x10 makerfarm will need ~20 amps minimum)
heatsink for said relay and thermal paste
wire

connect d9 +/- to the SSR input
connect one lead of the bed directly to the power supply, note which polarity you use
connect the other polarity from the power supply to the positive on the SSR load end
connect the negative from the SSR load to the other bed lead. 
see wiring diagram.png

the bed is non-polar so it doesn’t matter which line from the power supply goes where. Just make sure that one polarity from the PSU goes directly to the bed and the opposite polarity goes to the SSR load and then the other bed lead.

some notes: [use cheap SSRs (Fotek, no name, counterfeit name brand, etc) from amazon and eBay at your own risk](http://canada.ul.com/safetyalerts/ul-warns-of-solid-state-relay-with-counterfeit-ul-recognition-mark-release-13pn-52/)

that being said, I’m using this [fotek SSR](http://www.amazon.com/gp/product/B019132BZS?psc=1&redirect=true&ref_=oh_aui_detailpage_o03_s01 obviously nowhere near its rated load (which I seriously doubt it could handle). it is working as expected and with a moderately sized heatsink maintains an acceptable temperature. YMMV depending on seller and batch though!
