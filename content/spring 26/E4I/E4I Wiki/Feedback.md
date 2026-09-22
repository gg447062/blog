# Feedback

## Intro to Feedback
Feedback refers to the modification of a system by comparing the actual output of the system to the desired output, thereby creating a self-regulating, closed-loop system.  

> The “system” can be almost anything: for instance, the process of driving a car down the road, in which the output (the position and velocity of the car) is sensed by the driver, who compares it with expectations and makes corrections to the input (steering wheel, throttle, brake). ~ The art of Electronics

Feedback systems are very widely used in amplifier and oscillator circuits. In these systems, a portion of the output signal is routed back to the input signal. The feedback can be either positive or negative depending on whether the signal is in phase or out of phase with the input signal.


## Negative Feedback
In a negative feedback system, a portion of the output voltage is routed back, through a resistor or capacitor, to the inverting input terminal, introducing a signal that is out of phase with the original input signal. This combination reduces the signal, making the output smaller. The negative feedback method reduces the overall gain of the circuit and improves stability of the output signal by reducing noise and distortions.

>"In fact, there is really only one formula you need to know for negative-feedback circuits (you still have to use the rules, however). This formula looks a lot like our old friend Vout = Ao(V+ - V-). There is, however, the V- in the formula—this you must reconsider. V- in the formula changes because now the output voltage from the op amp is “giving” extra voltage (positive or negative) back to the inverting terminal. What this means is that you must replace V- with fVout, where f is a fraction of the voltage “sent” back from Vout. That’s the trick!" ~ The art of Electronics
