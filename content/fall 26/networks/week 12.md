
**tom's talk tips**

- be ruthless about side points
- one idea per sentence
- know your slides per minute
- pause at the end of point

----

**homework**

*reading*

this week the readings all seemed to point to the fact that the development of smart devices has paid very little attention to security and privacy violations. smart internet connected devices have successfully been incorporated into the market and our everyday lives as viable and profitable products, with apparent lack of concern for the necessary security protocols or the implications on privacy.

the article *Smart home device alerts New Mexico authorities to alleged assault* did a great job of spinning a privacy violation into a rescue operation. the fact the smart home device called the police in the right situation was purely happenstance, and in any other situation that would be a grave mistake. i found it funny that they quoted the sheriff saying "The unexpected use of this new technology to contact emergency services has possibly helped save a life" as if the technology calling the police wasn't just a result of it eavesdropping and calling the police of its own accord.
 
the guardian article was way more on point in addressing the double edged sword of networked devices. what you gain in convenience you give up in privacy. it also touches on the interconnectedness of people's lives, where your convenience is directly related to someone else's workload or income, as highlighted by the opentable example. the network of the world wibe web to which these devices connect functions as a mirror for the social and political networks that connect lived experiences across as the globe. in terms of networks, the vice article brings up the point that when you connect your Thing to the internet, you're opening it up to scrutiny by all of the curious users of that network, malicious or otherwise. and unfortunately, at the time of writing, a majority of those Things connected to the internet were known to be easy prizes for the industrious hacker.


*mqtt*

i had very limited success with the mqtt client examples. i got the arduino mqtt client successfully running and ostensibly sending to the mosquitto test broker but i couldn't tell if the messages were getting through. i got the node client running with the shiftr broker but as soon as i tried to switch to the mosquitto broker, i got a weird error:

![[week 12-1795549962616.webp]]

the way i interpreted this was that attempting to change the broker destination caused some kind of type error where the variable on which  `destroy` was being called was of a type that didn't have a `destroy` method. i did a quick google search and didn't find anything that was immediately helpful. so then i tried replacing the `mqtt` protocol with `wss` and `ws` and i got a different but equally strange error

![[week 12-1795550048187.webp]]

this seems to be an error within the library itself, but i wasn't able to figure out what was happening. i gave in and gave up.