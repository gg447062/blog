# Digital Electronics

Digital electronics, like our computers and microprocessors, have only two voltage states; on or off / high or low. When we apply that to familiar circuits like an Arduino, those translate to 5V or 0V. The high or low voltage in a circuit can communicate many things like; state of switch, trigger of an event, a bit of a number, etc. Because of this binary nature, it can be represented as true or false statements, creating the basis of Boolean Logic.


## Digital circuits

There are two subcategories of digital logic circuits; combinational and sequential. Combinational logic changes the output of the signal instantly as a response to the present input change, while sequential logic is tied to a clock signal and propagates change based on present and past inputs. Sequential circuits are usually built up of a series of combinational circuits.


### Combinational
Combinational logic provides an almost immediate response to the incoming data of 0's and 1's (low or high). The response is only to the present input and has no regard for any past inputs. Combination circuits can be very simple or extremely complicated and almost any combinational circuit can be implemented with only "NAND" or "NOR" gates.


### Sequential
In a sequential logic circuit, data moves through the circuit step-by-step and the output state of each step is determined by the previous state and the input signal. Because of this, sequential logic circuits are able to store a state and therefore has memory.  A clock is responsible for driving data to the next step by providing a steady stream of pulses. The building block of sequential logic is the flip-flop.

