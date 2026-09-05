## Digital Logic / Boolean Logic
Modern computers are built upon the fundamental concept of digital, or boolean, logic. Based on this system of rules, engineers have been able to create immensely complex systems based on simple true/false questions.

1 and 0 are used in boolean logic to represent true and false. This can become confusing since 1 and 0 are also used to represent high and low voltages in electronic circuits. It can be hard to determine the type of logic convention: positive true or negative true logic.

Voltage states actually vary depending on the specific logic of the IC. In general, +5 V is considered high, while 0 V (ground) is considered low. But in some cases, a voltage anywhere from +2.4 to +5 can be considered high while a voltage from +0.8 to 0 V can be considered as low. Every IC can operate with an entirely unique set of ranges for their logic.

## Logic gates
Logic gates are the physical circuits that perform boolean logic and they are the building blocks of digital electronics. There are 6 types of logic gates that each performs a different logical operation: INVERT (NOT), AND, NAND, OR, NOR, exclusive OR (XOR), and exclusive NOR (XNOR) gates. 

The inverter logic gate, or the NOT gate, are not true gates. They don't actually make any decisions. Very simply, their output is inverted from the input; the output is 1 if the input is 0, and vise versa.

The 6 digital logic gates are represented by these symbols below with inputs on the left and outputs on the right. These gates can be combined in many ways to create complex logic systems. The inputs of gates can be connected together while outputs should not. Outputs should only be connected to other inputs, they can also be connected to multiple inputs.

---
References:

https://learn.sparkfun.com/tutorials/digital-logic?_ga=2.85763097.1208191500.1566415199-1684579667.1531009928   
https://hackaday.com/2024/07/18/secrets-of-the-old-digital-design-titans/