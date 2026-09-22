For our energy class Meghna and I, with Nava's help on the generator, decided to build an FM transmitter to transmit sounds from a custom built oscillator as well as mp3s from any aux cable source. We based our design and broadcasting ethos on the work of [[Tetsuo Kogawa|Tetsuo Kogawa 1]]. 

**The Schematic**

Here's a few circuit schematics and tutorials that I have found while researching transmitters

- Testuo Kogawa's transmitter [design](https://translocal.jp/radio/micro/howtosimplestTX.html) - this is **the** source of information that got everything started
- another version of it [here](https://electronics-diy.com/building-simplest-fm-transmitter.php) with interesting links to other projects
- here's a Make: [article](https://makezine.com/projects/super-simple-fm-transmitter/) on tetsuo's radio, glad to see them carrying on the the good work

![[tetsuo-schematic.webp]]

**process**

i whipped up a little 555 oscillator that outputs both square and triangle waves in order to have something to transmit. as an aside, my first idea for this project was an oscillator whose pitch was controlled by the amount of voltage that the player can generate with the hand cranked motor.

first meghna and i got all the parts for the circuit - except for a variable capacitor which we had to order from digikey - and sat with david rios to discuss it. he also hooked us up with some wire for the coil as well as a couple transistors and capacitors. we put it together on the breadboard but weren't able to test it until saturday because we didn't have a receiver. meghna bought a radio and we plugged in the oscillator and the transmitter and slowly tuned the radio until we heard the the humming of the oscillator. it was a beautiful moment because neither of us had any idea if it was going to work or not. we spent the rest of the day messing around with it trying to pick up a song from an aux cable, which was harder to hear than the oscillator.

**the all important coil, as demonstrated by tetsuo**

![[tetsuo-winding-the-coil.webp]]

the next week, we borrowed a variable capacitor from shloka to test out tuning the circuit. we were able to get a better signal, and for a good period of time when i was unfortunately not present meghna got a very clear signal out of it.  sadly in its unsoldered and capricious state we couldn't get a good signal out of it again that day. that evening meghna soldered the majority of the parts together onto a protoboard, save for the variable cap which was the wrong value, and the coil of which we had various versions whose number of turns was to be selected depending on the cap.

on friday the caps arrived in the mail so we replaced the borrowed one and soldered it into place. we were still struggling to get a good signal even though we had the right value of capacitor, so we decided to just solder on the coil with which we had the best success and try it with an antenna. i soldered the coil on that night and then went home. saturday night i did some research on how to read the radio's frequency since adjusting the cap without any idea of what effect it was having was like scrabbling for the frequency in the dark. i learned that you can find the frequency by placing a long wire in the lead of an oscilloscope and holding it near, but not touching, the radio transmitter's coil. through this research i also better understood how the circuit worked at all which gave me some confidence. it hadn't occurred to me that the coil together with the adjustable capacitor work together to from a circuit called an LC tank which is a kind of oscillator! some of the configurations of this are also called a colpitt's oscillator which emits a nice sine wave.

the next day, armed with my newfound knowledge, i went to school and used the oscilloscope technique to find and then set the frequency of the transmitter's oscillator. i then added a long wire to the circuit to act as an antenna, tuned the radio to approximately the frequency shown on the scope, and to my great pleasure i was able to pick up a remarkably good signal. i then made a slightly longer antenna based on the measurements i found somewhere about picking the correct antenna length based on the wavelength of the transmitter's frequency. i don't remember the formula but it said that my ideal antenna length was 2 foot something, or 66 cm. the formula was for a 1/4 wavelength so i figured that cutting the antenna in half would probably result in something like 1/8 the wavelength, which is at least an even ratio. so i made a 33 cm antena and soldered it on, which made the signal even better.

**wire placement for testing LC tank's frequency**

![[wire-placement.webp]]

**the frequency measured**

![[oscilloscope.webp]]

once i was satisfied with the transmitter side of things, i decided to work on the power. i had realized earlier that although i was learning a lot about the radio transmitter, i hadn't been able to get practical experience with the actual topic of the assignment, which was to generate electrical energy with kinetic energy. so during the whole time i had been working on the transmitter i had been 3D printing parts for some motor cranks. shloka lent me a small stepper so i grabbed a couple full bridge rectifiers and some big capacitors. i was able to generate a pretty smooth 15-20 volts while spinning the motor, which was pretty much double what we needed for this project. I tried using a voltage divider to scale down the voltage, but some was always leaking out through the resistor connected to ground so it was hard to keep it really stable.

sofi came to my rescue with a variable voltage regulator which could be adjusted via a little trim pot. it also had a small LED screen to show the voltage coming and in or going out, switched with a button, which was helpful while adjusting the output. however, i quickly realized that for some reason it drained the voltage out of the capacitors even when the LEDs were off, so i had to add a diode between its output and the power rail so it wouldn't do that. with that in place i was able to generate a steady 9 volts as long as i kept the motor generating at least 12-15 volts. i plugged connected the generator to the transmitter and was able to hear a very clear version of "do you believe in life after love" through the radio. i was immensely pleased with the effect, since it both achieved the power requirements of the assignment as well as the quality of radio transmission that we wanted to be able to send.

**the whole circuit in all its glory**

<iframe width="560" height="315" src="https://www.youtube.com/embed/79Qlv8-9b0k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Once I had it working I decided to make an enclosure. Instead of laser cutting or 3D printing, I decided to use a Tupperware I got at Dollar Tree as the project box. I soldered together the circuit, using a small little circuit board that joy gave me. Then I got some standoffs from the shop and used a hand drill to make four holes in the bottom of the Tupperware. I attached the variable voltage regulator to the standoffs and hung the rest of the circuit underneath it using solid core wire. Not the most sturdy construction but it worked for a while. It was cool that you could see the voltage regulator's screen through the tupperware so you could see how much voltage was being generated by the motor as it turned.

![[IMG_3061.webp]]

![[IMG_3062.webp]]
*the power circuit enclosed in it's tupperware with the enclosed radio behind it*

Unfortunately in my excitement and exhaustion (it was late at night when I finished) I didn't document the functioning circuit in it's enclosure. As can be expected, when it came time to present the project in class the next day, something went wrong with the power circuit and we couldn't get enough voltage to the radio. Nava had also made her wild motor and gear contraption to power the radio, but that also had its own issues and so the class never got to see the radio in all its glory.