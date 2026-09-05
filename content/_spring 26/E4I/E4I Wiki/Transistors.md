# Transistors

## Intro to Transistors:   

Transistors are Semiconductors that can use a very small current or voltage on one lead to control a much larger current flowing through the other two leads. This means that they can act electrically as either a switch or to amplify a small current.

In the plumbing analogy, a transistor acts like a faucet. A small force is applied to open a gate, allowing the larger force of water to flow through the pipe.

Load current = input current x transistor gain (hFE)

Transistor circuits can sometimes be difficult for beginners. The main reason being that it's a three-terminal component that deals with two different sets of voltages and currents.


## Transistor Families
Transistors are categorized into two families: Bipolar Junction Transistors (BJTs) and Field-Effect Transistors (FETs). BJTs requires a biasing input or output current at their control leads while FETs only require a voltage on the control lead and no current.

### Bipolar Transistors

There are two types of standard (bipolar junction) transistors, **NPN** and **PNP**. The letters represent the three layers of semiconductor material that makes up the component. In both these types, the middle layer acts as a gate or faucet that controls the current that flows through the layers.

<IMAGE>

The three leads of a bipolar transistor are labeled base (B), collector (C) and emitter (E). A small current at the base (input) is used to control a much larger current flowing through collector-emitter.

**Rule 1:** In a NPN transistor, the voltage at the collector terminal must be greater than the voltage at the emitter terminal by a few tenths of a volt in order to allow current flow through the collector-emitter junction. This is true regardless of the applied voltage at the base. In PNP transistors, the voltage at the emitter must be greater than the collector.

**Rule 2:** In a NPN transistor, there's a 0.6V voltage drop from the base to the emitter - This means the base voltage (VB) must be at least 0.6V greater than the emitter voltage (EV) in order to allow current through the collector-to-emitter junction. In PNP transistors, there's a 0.6V rise from base to emitter - VB must be at least 0.6V less than VB.

### Field-Effect Transistors

There are two types of FETs, **N-channel** and **P-channel**, the letters stand for the type of material the channel is made of. FETs have three leads labeled gate (G), source (S) and drain (D). They essentially operate using an electric field effect - using a small voltage from the gate to increase the resistance of the channel that the drain-source current flows through.

Since FETs use an electrical field, they only require a small input voltage and practically no current.



## Bipolar Transistor Types

**Small Signal**
  - used to amplify small signals.

**Small Switching**
  - switching transistors operate at either ON or OFF

**High frequency**
  - These are used for high-frequency applications such as radio, TV, and microwave.

**Power Transistors**
  - These are used in high-power (current and voltage) circuits. They usually are larger in size and have a metal heatsink attached to dissipate heat.

**Darlington Pair**
  - In certain applications, the current that is available to switch on a transistor is very low. This single transistor may not be enough to pass the current that is required from the load on the circuit.
  - This is an arrangement of two standard NPN or PNP transistors where the emitter of one transistor is connected to the base of the second transistor. This configuration allows for the current amplified by the first transistor to be further amplified by the second transistor.  
  - The total current gain of a Darlington pair is the gain of Transistor 1 x Transistor 2. If you have two transistors with a gain of 100, the total gain of the Darlington Pair would equal 1000.

**Phototransistor**
  - Phototransistors uses light levels to control the current flow between the emitter and collector. 
  
**Transistor Array**
  - These have multiple transistors packaged together inside one IC. 


## Field- Effect Transistor Types
Field-effect transistors have become increasingly more important than bipolar transistors. They are easy to make and require less silicon raw material. There are two major types: Junction and Metal Oxide. In both types, the output current is controlled by a very small input voltage and basically no input current.

**Junction Field-Effect Transistors (JFETs) Types**
  - Small signal and switching 
  - High frequency
  
**Metal Oxide Semiconductor Field-Effect Transistors (MOSFETs) Types**
  - Power switching / amplification
  - Voltage controlled resistors 
  


---
References:   
https://electronicsclub.info/transistors.htm

Testing Transistors:   
https://electronicsclub.info/transistors.htm#testing

Transistor Circuits:   
https://electronicsclub.info/transistorcircuits.htm

https://www.electronics-tutorials.ws/transistor/tran_8.html


