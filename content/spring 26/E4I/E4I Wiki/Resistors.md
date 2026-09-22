# Resistors

## Intro to Resistors:

The job of a resistor in a circuit is to limit (or resist!) the flow of electric current.
They come in many shapes and sizes, but the most common ones are made from a mixture of carbon-based (conductive) materials with wires that come out from both ends; the more carbon, the less resistance.

The resistor can be connected in either direction (it does not have a power or ground). A current can flow through it in either direction. They are usually used within a circuit to limit current, divide voltages, and pull-up I/O lines.

The most common use of resistor is to limit the current in a part of a circuit; using a resistor with an LED to avoid burning out the LED. They can also be used to reduce the voltage being supplied to a part of a circuit by making a voltage divider. You can also combine a resistor with a capacitor to create timing circuits.


## Resistor Units
Every resistor has a specific resistance, which is measured in ohms Ω (omega).


## Identifying Resistors

#### Symbols
In a circuit schematic, resistors are labeled as R1, R2, etc. and is shown as these symbols:
<img src="https://cdn.sparkfun.com/r/600-600/assets/f/c/c/c/b/515dbf24ce395f2359000000.png" alt="Resistor">


#### Types
Resistors come in many packages and sizes depending on their power rating. The most common ones that we use here are in a through-hole 1/2W package.

- through hole
- SMD
- variable resistors
- photo resistors
- thermistors


#### Codes
Through-hole resistors use a color-coded system for noting their values. The most common resistor has 4 color bands.
- The first band = first digit
- The second band = second digit
- The third band = the multiplier (amt of zeros)
- The fourth band = the tolerance (or precision - this can mostly be ignored)

If a resistor has bands of red (2), violet (7), yellow (4 zeros) and gold bands so its value is 270000ohm = 270kΩ

There are many online and app-based resistor calculators you can reference.


#### Values
There isn't a readily available resistor for every possible value. While it might make sense to create resistors in increments of 10Ω in small values, once you get into 10,000Ω, a 10Ω difference would not make a significant difference, especially when you factor in the tolerance.

I.E. A 4700ohm resistor with a tolerance of ±10% will have a value within 10% of 4700ohm, between 4700 - 470 = 4230ohm and 4700 + 470 = 5170ohm (470 is 10% of 4700)

The E12 series - The most common resistor values comes in a series with 12 values (10, 12, 15, 18, 22, 27, 33, 39, 47, 56, 68, 82) and a tolerance of 10%. These values are then multiplied by powers of 10 to get 100, 120, 150 etc.


#### Power Ratings
Power is the rate at which energy is converted into something else. In the case of a resistor, when current flows through it, the energy is converted into heat. It is measured in Watts.

Every resistor has a maximum power rating and for most circuits, the heat is not noticeable and a standard power ratings of 0.25W or 0.5W are sufficient. In certain high-power circuits, you may need a higher power rating to be able to handle the heat.

The power, P, developed in a resistor can be worked out using these equations:
> P = V² / R  or  P = I² × R


## Resistors in Series and Parallel

#### Resistors in Series 
When resistors are connected in series, electric current needs to flow all of them, one after the next. This means it's getting limited/restricted more with each resistor. The total resistance in this case is calculated by adding all the resistor values together.

> R(total) = R1 + R2 + R3 ....

#### Resistors in Parallel 
Current flowing through resistors connected in parallel is a different story since it can flow through all the resistors at the same time. The calculation for the total resistance of N number of resistors is the inverse of the sum of all inverse resistances.

> 1/R(total) = 1/R1 + 1/R2 + 1/R3... 


## Substituting resistors

#### Substituting   

When you are building a circuit, your calculations may state that you need a 6700Ω resistor, but that value doesn't exist. As a rule, it is almost always okay to use any value that's is within 10-20% of the required value. If a more accurate is critical for an application, it will tell you. Another option is to connect two or more resistors in series or in parallel to create custom resistance values.


#### Precautions  

When working with a power hungry circuit, the current flowing through a resistor can cause it to get very hot! Make sure to always use resistors with the proper power rating. If the power rating is not specified for resistors in a circuit, the standard 1/4 or 1/2 watt resistors are usually okay to use.


#### Safety
If a resistor is overloaded with current, it will become very hot and darken in color. It could even melt or catch fire. Incredibly, the resistor may still be functioning once it gets to this point, although it may just be operating at a lower resistance.


## Resistor circuits (examples)

- Current limiting resistor
- Voltage Divider
- Variable resistor
- Resistor ladder


---
References:

https://electronicsclub.info/resistors.htm   
https://electronicsclub.info/vdivider.htm   
https://learn.sparkfun.com/tutorials/resistors   



