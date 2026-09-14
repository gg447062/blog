# AC / DC

AC and DC refer to the type of current flow through a circuit. AC stands for ***Alternating Current*** and DC stands for ***Direct Current***.


## Alternating Current (AC)

Alternating current describes a charge that flows in one direction, then periodically switches direction. The voltage also reverses along with the current and swings continually between positive (+) and negative (-). A 12V AC current alternates between +12V and -12V. When plotted on a graph, AC resembles a sine wave.

The rate of direction change is called the frequency, which is measured in hertz (Hz). One hertz is the number of positive/negative cycles per second. The mains electricity in the US is measured at 60Hz and 120V.



## Direct Current (DC)

Unlike Alternating Current, Direct current flows in only one direction, and likewise, a DC voltage is always positive (+) or always negative (-). The voltage and current may increase or decrease, but the direction stays the same.

All electronic circuits that we build require a ***steady DC*** at a consistent value in order to operate correctly. Batteries and regulated power bench supplies are the best choices for providing a steady DC supply for your circuits.



#### Power Supplies

Power supplies are able to convert the mains AC supply into a safer low voltage AC current. It does so through the use of a transformer. The lower voltage AC is then turned into DC through a bridge rectifier. The signal at this point looks like if you've flipped all the peaks of the AC sine curve to one direction. This state is called ***Varying DC*** and it's not yet suitable for use in electronic circuits.

Varying DC can be smoothed with the aid of a capacitor. ***Smooth AC*** is suitable for projects that have are not very sensitive to voltage variations such as lamps, heaters and motors.

- Steady DC
- Smooth DC
- Varying DC


----
References:

https://learn.sparkfun.com/tutorials/alternating-current-ac-vs-direct-current-dc/all

https://electronicsclub.info/acdc.htm#props

https://cdn.sparkfun.com/assets/home_page_posts/2/7/7/5/SFE_Poster_Series_-_AC_and_DC.pdf
