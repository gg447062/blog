# Logic Levels

It is important to distinguish between **Voltage Source** and **Logic Levels** (Signal Voltage levels).

An Arduino Uno can be powered using a 9v battery and you can say that your project expects a **Voltage Source** of 9v. However the sensor that is connected to the microcontroller IC in the Arduino Uno (the Atmega 328) operates on a **Logic Level** of 5v.

While this might seems like a random choice, this actually determines the states of your circuit.

A logic level is a state or a specific voltage that a digital signal can inhabit. All digital circuits operate in a binary state: ON or OFF, logic 1 or logic 0. This binary logic is used to store, process, and transmit data or information. A binary 1 is also referred to as a HIGH signal and a binary 0 is referred to as a LOW signal - This is the logic that is seen in the Arduino.

Logic 0 and Logic 1 can vary from system to system and is usually defined in the datasheets from the chip manufacturers. While the majority of systems use either 3.3V or 5V for HIGH or logic 1, some systems might represent logic 1 as +3.5 V and +6.5 V.


---

- TTL Logic Levels  (5v)
- CMOS Logic Levels (3.3v)
- Arduino Logic Levels

---
References:

https://electronicsclub.info/acdc.htm#props

https://learn.sparkfun.com/tutorials/logic-levels

https://jeelabs.org/2010/12/16/voltage-3-3-vs-5/

https://cdn.sparkfun.com/assets/home_page_posts/2/7/7/5/Concept_Poster_Analog_vs_Digital_WEB.pdf

https://learn.sparkfun.com/tutorials/digital-logic

https://learn.sparkfun.com/tutorials/binary

https://electronicsclub.info/gates.htm

https://e2e.ti.com/support/logic-group/logic/f/logic-forum/862744/faq-what-s-the-difference-between-ttl-and-5v-cmos-logic
