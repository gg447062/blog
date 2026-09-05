# Integrated Circuits

## Intro to ICs

Integrated circuits (ICs) are a miniature version of circuits that are made of resistors, capacitors, diodes, and transistors that are formed on a single chip of silicon. A single IC could be made of a few to tens of thousands of components, all fitting in a chip the size of a button.


## Types of ICs

Just as the large version of circuits, ICs can come in 3 different flavors:

***Analog (or linear) ICs*** can produce and respond to varying voltages in a circuit. These ICs include voltage regulators, operational amplifiers, comparators, timers, and oscillators.

***Digital (or logic) ICs*** can produce and respond to only high or low voltages (on or off). These ICs include logic gates (such as AND, OR, or NOR), microcontrollers, memories, binary counters, shift registers, multiplexers, encoders, and decoders.

***Analog / Digital ICs (MixSignal)*** has characteristics of both analog and digital ICs.



## Identifying ICs

There are many different shapes and sizes for ICs, this physical appearance is referred to as its ***package***. The package type factors in the number of pins coming out of the IC and the power dissipation. Lots of different components come in the same package type - for example, a voltage regulator IC could look just like transistor with three pins and a heatsink.

When it comes to DIL(dual in-Line) or DIP(dual in-line packages), the IC is enclosed in a black plastic holder with two rows of pins that are spaced on a standard grid of 0.1" (or 2.54mm), the same spacing used for breadboards and perfboards.

The same way as other components, ICs also come in SMD packages developed to be assembled by machines.

<p align="center">
<img src="https://cdn.sparkfun.com/assets/c/7/a/1/9/51e0633cce395f867b000000.jpg">    
</p>
<p align="center"><i>IC packages by Sparkfun</i></p>

<br>


## Sinking and sourcing current

*Sink* and *source* are terms used to describe the direction of current flow through the IC outputs (leads).  


**Sink**   
The IC is said to be sinking current when the direction of current is flowing into the chip. For example, an LED placed between the IC *output pin* and *+V (positive power supply)* will turn on when the pin is low (0V).

**Source**  
The IC is said to be sourcing current when the direction of current is flowing out from the chip. For example, an LED placed between the IC *output pin* and *0V (negative supply)* will turn on when the pin is high (+V).


## Safety and Precautions
Some ICs are sensitive to static electricity and can become damaged fairly easily. If you touch them and transfer the static charge from your clothes is sometimes enough to damage some ICs. When that is the case, the manufacturer and/or suppliers will send the ICs in antistatic packaging with a warning label - when you see this, be sure to store the chips inside the protective sleeve until you're ready to use them.

For some ultra sensitive ICs, you may be required to ground the circuit AND yourself when interacting with the chip.
