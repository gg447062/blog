i made the nime poster this week, with encouragement from emilia and design help from alua.

	poster duotone green: rgb(163,223,0)
	poster duotone pink: rgb(206,84,224)



i made a lot of progress this week making a custom power pcb and making a new enclosure to fit the modules i was making. for the enclosure i used some wood that was salvaged from an old project disassembled over the summer as well as a plywood panel i found in the basement. i was focused on making the modules truly modular and able to be added and removed without having to solder or desolder any connections. i had a lot of success using jst connectors for power and rca jacks for the module-to-module connections

power board right out of the bantam mill
![[class 10-1795546610323.webp]]

the enclosure walls cut and stained and ready to be glued to the base.![[class 10-1795546711308.webp|700x525]]


the envelope generator (top) and vca (bottom) attached to their panel. the jst connectors are the thinner red, yellow, and black wires coming off the boards. 
![[class 10-1795546724802.webp]]


i had a crisis with my instrument late on sunday night before the first rehearsal that spawned the name of my instrument: hungry bug. i tried to make a matrix mixer to be able to have multiple outputs from my instrument for things like effect sends. however, it didn't work when i first plugged it in. while i was probing the various connections with the oscilloscope, it began to make a wild screeching and buzzing sound. i thought i had shorted something and i went wild checking for the issue. i replaced the ics and  even desoldered and replaced the transistor in the oscillator circuit. nothing solved it. 

the matrix mixer, nice looking but sadly faulty![[class 10-1795546365903.webp]]

i decided to give up and leave and so i cleaned up my working area and headed for the train. i was despondent. i felt like all my hard work had come to nothing! i couldn't just leave things as they were though, so on the train home i began to try and brainstorm simple circuits that could be easily modified to make interesting sounds. i thought about the beautiful glitches and stutters my solar sounder makes when there isn't enough sun, which reminded me of power starving, a venerable circuit bending technique where the hacked circuit is fed less than it's designed voltage.

![[class 10-1795546130536.webp]]this made me think of hungry circuits and hungry ics, which remind me of bugs. conveniently "hungry bug" is also the name of the main character's favorite restaurant in dorohedoro, one of my favorite anime/mangas. thus i found an identity for the instrument. i even drew out a little 'artists rendering' of the instrument's final form.










my drawing of the final form of the instrument:
![[class 10-1795546401903.webp]]

when i returned to school the next day, i sat down to do some last ditch debugging before scrapping everything and starting from scratch (in hindsight this was pretty dramatic 😆 ). as i was testing it suddenly occurred to me to check the charge of the battery powering the speaker i was using to test (it may have been prisha's idea to check the battery cause she was providing technical and emotional support to my troubleshooting efforts). lo and behold, it was at only 5 volts, instead of the needed 9. with this discovery, my whole day was saved, and i looked back at my night of distress and self recrimination with slight embarrassment. once again it's always best to check for the simplest solutions to the problems before you go resoldering circuits at 2am. i had a successful first rehearsal with the instrument and i was pleasantly surprised at how much i liked the sound of it!

the iteration of the instrument used for the first rehearsal, the rca jacks and cables on view as the inter-module connectors.
![[class 10-1795546469486.webp]]

the instrument doesn't have the power starve function yet but i stuck with the name anyways because i think it's cute and sets the right vibe. however, more r&d is in the books for adding that feature to be true to the name. to be fair, the name did come about because of a power starve situation (fun fact the potentiometer typically used to perform the power starving operation is also called a dead battery potentiometer [src](https://www.kulturgueter-schuppen.de/books/dead-battery-music-dbm-circuits/page/the-art-of-power-starving)) so it does fit anyways.
