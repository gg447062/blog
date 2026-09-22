
### ["What the $#%$ is a Rungler?"](https://www.modwiggler.com/forum/viewtopic.php?p=1276372&sid=b7df58e12bd7db96d5b6b2627252485b#p1276372)

 by **[richard](https://www.modwiggler.com/forum/memberlist.php?mode=viewprofile&u=615&sid=b7df58e12bd7db96d5b6b2627252485b)** » Sun Sep 01, 2013 9:57 am

I thought people might be interested in this. I don't think its been posted before. It is extracted from a document written by Rob Hordijk, sent to me by Joker Nies. I hope and assume it is fine with Rob for it to be posted here:
"What the \$#%$ is a rungler?  
  
The purpose of the rungler is to create short stepped patterns of variable length and speed. One could categorize the circuit somewhere halfway between a plain S&H and a shiftregister-based pseudorandom generator. It needs two frequency sources to work and basically creates a complex interference pattern that can be fed back into the frequency parameters of the driving oscillators to create an unlimited amount of havoc.  
  
The rungler is basically a CMOS shift register clocked by one oscillator and receiving its data input from the other oscillator. The output bits of the shiftregister are used as a binary code 'to do something with'. E.g. in the Benjolin the last 3 stages of the shift register for a 3 bit code that is fed into a 3 bit DA converter. This DA eight level output voltage is fed back to the oscillator frequency control inputs. The output of the DA is the 'rungler CV signal'. To describe the rungler waveform in similar terms as like a sine wave or pulse wave I call it a 'stepped havoc wave'.  
  
When the rungler signal is fed back to the frequency parameters of the oscillators it will change the triangle waveforms and pulse widths of the oscillator outputs, making other types of havoc waves, like a 'pulsed havoc wave' and a 'sloped havoc wave'. Note that it is these properties of stepped, sloped and pulsed that are of interest in the waves.  
(The Dutch composer Jan Boerman formulated an idea in the 1960s about audio signals that are inbetween pitched and unpitched. Havoc waves are probably somewhere in that region, maybe a bit similar to granular synthesis stuff. I haven't really thought deeply about this myself, but Boerman has certainly always been an inspiration to me to try to go into that inbetween territory.)  
  
The rungler will try to find a balanced state. In this way it behaves according to principle from Chaos Theory. There seems to be an unlimited amount of possible balanced states and when a balanced state is just slightly disturbed it can be noted that it takes a little time to find the next balanced state, with noticeable bifurcations, etc. Note that a new balanced state is defined by the exact position of the control knobs plus the previous state it was in.  
  
The first rungler experiments I did were back in 1980 I think, and there are quite a lot of variations possible on the rungler idea. In the Benjolin design the data input for the shiftregister is not just the pulse from the second oscillator but the XOR of this pulse and the last bit of the shift register (inspired on the pseudorandom generator). The XOR is the transistor/opamp combination that actually forms a controllable unity gain/minus unity gain amplifier, a very simple ringmodulator, so to speak.  
  
Tip: An interesting option is to feed the three bits at the end of the shiftregister into the 3 'selection' inputs of a CMOS 4051 eight-to-one/one-to-eight analog switch and e.g. quickly switch between eight audio signals. You can take these three bits from the pins 2, 3 and 12 on the 4021.  
  
The shiftregister used should not be too long, four to eight stages already does a perfect job. Some CMOS shiftregisters can recirculate, which would hold the pattern.  
  
One can expand by having multiple parallel shiftregisters alternatingly clocked on positive and negative flanks of the oscillator pulse and e.g. using the triangles from the oscillators to crossfade between multiple DAs on the multiple shiftregisters, etc. By expanding the number of oscillators and shiftregisters the number of available havoc waves explodes. Basically the rungler is an open ended circuit that can be expanded and chained into multi-rungler networks.  
  
In the current issue of Leonardo Music Journal (issue 19) is an article about the Blippoo Box, the Benjolins Big Brother, and there is more on the rungler circuit in the article as wel as some other thingies I used in the Benjolin as well.  
  
Imho a rungler circuit works best in an analog electronics implementation. It is definitively more alive and surprising due to the slight instabilities in the analog circuitry. I did digital implementations, but they can't beat the 'organic behaviour' of the analog versions. But this is just personal taste..."



***

**for more info on how the rungler works in the benjolin check here**
https://www.perfectcircuit.com/signal/rob-hordijk-benjolin?srsltid=AfmBOoridSCh3vihVIRBp_x0k8mH3sRfQhpEKPsi3AbwdOElnfBs2nQR

#synth