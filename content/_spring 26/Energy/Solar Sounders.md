meghna and i decided to add our own voices to the solar sounder body of work and exploration. 

solar sounders are sound generating devices that get their singing energy directly from the sun. i believe the first one was made in the 1960s by Alvin Lucier, but the most well known to me are the offerings from peter blasser and d fishkin.

[here](https://econtact.ca/18_3/blasser_solarsounder.html) you can read the website with solar sounder info
and [here's](https://www.rhizomedc.org/new-events/2016/9/3/solar-sounder-workshop-with-peter-b) another one detailing a solar sounder workshop given by mr blasser
[here's](https://isartum.net/leimma/63/refpitch/G3-27.06668) a reference for find interesting pitches for the sounder

blasser and fishkin's circuits were all built to emulate sounds created by other entities: birds, frogs, monks and trains. i was particularly enamored of the monk circuit because i had recently heard the gyuto monks on WFMU and been astounded.

the monks in question
https://www.youtube.com/watch?v=L42AnSAdzXw

solar panels
https://abra-electronics.com/solar-products/solar-cells-chargers-modules/2-4-watts/solar-200-9v-2w-solar-panel.html

https://www.adafruit.com/product/5856

i ended up ordering these ones:
https://www.harfington.com/products/p-1068694


step 3 [here](https://www.build-electronic-circuits.com/pnp-transistor/) shows how to do exactly what i want to do with a pnp for the nocturnal circuits

this is the circuit in question:
![[Screenshot 2026-04-17 at 6.28.32 PM.webp]]

![[Screenshot 2026-04-17 at 6.29.59 PM.webp]]


the above circuit didn't work very well with my 40107 cricket circuit so I tried a MOSFET based switch instead. the one i made fro, this unconventionally drawn schematic worked way better. [source](https://www.instructables.com/Make-Automatic-Night-Light-Switch-Circuit-Using-Mo/)

(the red line connecting the lightbulb and pin 2 of the mosfet should really be black)
![[Pasted image 20260428194401.webp]]

more easy to understand one from the [arduino forum](https://forum.arduino.cc/t/automatc-lights-on-using-ldr-and-mosfet-at-31-volt/688470)

![[Pasted image 20260428233109.webp]]


**Osc Voice circuit**

I'll use the CD40106 hex schmitt trigger ic set up like this:

![[schmitt trigger square.webp]]

a triangle wave would be ideal but i don't want to add more components (op-amp)

![[schmitt trigger triangle w buffer.webp]]


note frequency chart [source](https://www.phys.unsw.edu.au/jw/notes.html)
![[Screenshot 2026-04-18 at 5.16.25 PM.webp]]




**Gate controller Circuit**

I learned about the circuit in e4i, schematic from [here](https://www.electronics-tutorials.ws/waveforms/astable.html)

![[Screenshot 2026-04-18 at 3.40.18 PM.webp]]

astable mutlivibrator frequency table from the same website

![[Screenshot 2026-04-18 at 3.39.57 PM.webp]]



**Gate Circuit**

![[Screenshot 2026-04-18 at 5.13.31 PM.webp|683]]


#solar-final #synth #solar-sounder 


[[Screenshot 2026-04-22 at 11.42.35 PM.webp]]

I added some filters to the circuit, i used this handy calculator on [digikey](https://www.digikey.com/en/resources/conversion-calculators/conversion-calculator-low-pass-and-high-pass-filter) to figure out the right RC values

![[Screenshot 2026-04-22 at 11.44.24 PM.webp]]

amplifier circuit

![[Screenshot 2026-05-04 at 11.52.31 AM.webp]]
