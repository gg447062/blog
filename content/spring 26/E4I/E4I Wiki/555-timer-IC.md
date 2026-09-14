# 555 timer IC

## Intro to 555

The 555 timer is an integrated circuit (IC) that can be used as an oscillator, a timer, and many types of circuits with the addition of a few exterior components. Due to its versatility, stability and low cost, the 8-pin 555 timer may be the most popular IC ever produced to this day.  



## 555 Astable mode
The astable mode of a 555 timer circuit is designed to perform as an oscillator. In this mode, the 555 is combined with two external RC (resistor-capacitor) charge/discharge circuits to output a rectangular wave. The waveform being generated can be adjusted (duration, frequency, etc.) by changing the RC values.

This mode is referred to as astable because the digital waveform that is output oscillates sharply between low (0V) and high (+Vs), with neither state being stable.



**Lab:**      555 LED Flasher / 555 LED Breather




## 555 Monostable
The monostable mode of the 555 acts as a simple timer. In this mode, the 555 used in combination with an external RC circuit will output a pulse when the capacitor reaches a trigger voltage (2/3 of the supply voltage). When the trigger voltage is reached, the chip's output will switch from low to high for a duration, which can be changed by adjusting the R and C.

This mode is referred to as monostable because the circuit will produce a single pulse when triggered. It is only stable in the output low state while the triggered output high state is only temporary.


**Lab:**      555 bounce-free switch (one shot)  




## 555 Bistable
The bistable mode of a 555 timer circuit is designed to perform as a flip-flop, a circuit that switches between two stable states which results in an output of current from the output pin.

Unlike the astable and monostable modes, this circuit does not require a RC circuit to set the timing. It very simply relies on a trigger pin and reset pin to switch between the two states; it's acts like a simple memory circuit.


**Lab:**      555 toggle switch 
