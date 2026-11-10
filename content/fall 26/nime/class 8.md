
i tried to make a sequencer, it didn't work right. i struggled for days with a weird behavior from some diodes. they seemed to defy the main rule of the diode as a 'one way street for electricity'. the whole point of using them in the circuit was for current to only flow out of the step outputs of my cd4017 counter chip so as to not to damage the chip itself and to keep everything working as it should. however, i was seeing evidence of current flowing between the outputs despite the diodes. i also noticed that the cv steps weren't outputting the full 12 volts that they should have been putting out with their pots at full blast. i spent about 4 days pulling my hair out over it until i noticed that when i removed certain diodes from the circuit, things began to work normally. that's when i inspected my diodes closer and noticed that not all of them were the  1n4148 or 1n914 that were called for in the schematic. i looked up the numbers i realized that contrary to my previous belief, the shop did indeed have zener diodes. according to wikipedia:

'A Zener diode is a type of diode designed to exploit the [Zener effect](https://en.wikipedia.org/wiki/Zener_effect "Zener effect") to affect electric current to flow against the normal direction from anode to cathode, when the voltage across its terminals exceeds a certain characteristic threshold, the _Zener voltage_.'

this explained all of the weird behavior that had been driving me crazy. when i replaced the diodes with the correct ones, everything worked exactly as it should. the big lesson from this experience is to **always read the part number!!**

i also tried to make an envelope follower, it didn't work well, probably due to my voltages since the circuit i used was designed for a 9v battery and i'm now using a 12v bipolar supply. i'm gonna try this schematic instead: https://www.eddybergman.com/2020/02/synthesizer-build-part-20-arp2600.html#google_vignette

i also made myself a little power supply to provide the +12/-12 voltage levels needed by the circuits i was making. 

![[class 8-1794166323835.webp]]