# Op amps

## Intro to Operational Amplifiers

Operational Amplifiers, or op-amps for short, are linear ICs that are designed to amplify voltages and signals. Specifically, they amplify the *difference* between the voltages and signals that are applied to their two inputs. Op-amps are extremely versatile and can be used in many amazing ways. They're called operational amplifiers because they can perform mathematical operations such as addition, subtraction, multiplication, division, differentiation and integration.


The op-amp IC itself is made up of a bunch of transistors, several resistors, and a few capacitors. But instead of understanding the internal circuitry, it is much more important to understand the rules that are setup to work with the input and output leads.


## OP-AMP operation   

An op-amp has two inputs, one is inverting and one non-inverting. When a signal is fed through the inverting input, it will be reversed at the output. (Inverting input is -; non-inverting input is +.)


An op-amp is designed to identify the difference in voltages applied at its inverting and non-inverting inputs (usually pins 2 and 3 of the package). This difference is called the differential input voltage. The output of the op-amp is the differential input voltage multiplied by some value A - the open-loop gain.

---

A typical op-amp circuit uses it's two inverting and non-inverting signals, the positive and negative dc power supply leads, an output terminal and other leads that may be used in case of fine tuning. Often in a schematic, the power supply leads and the fine tuning leads are omitted.

When a voltage is applied to the inverting terminal (V-) is more positive than the voltage at the non-inverting terminal (V+), the output voltage will swing towards the negative supply voltage (-VS). If the voltage at the non-inverting terminal (V+) is more positive than the voltage applied to the inverting terminal (V-), the output will swing towards the positive supply voltage (+VS).

---
References:

https://learn.sparkfun.com/tutorials/introduction-to-operational-amplifiers-with-ltspice

https://www.falstad.com/circuit/circuitjs.html?startCircuit=lrc.txt

https://www.youtube.com/watch?v=kqCV-HGJc6A

https://www.youtube.com/watch?v=TQB1VlLBgJE