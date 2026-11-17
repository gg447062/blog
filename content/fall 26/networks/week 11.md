
this week i tried out connecting my arduino to sandbox370. i had to do a google search to remember how to print out the mac address for the arduino, but once i did that everything else went pretty smoothly. i stared with the `simpleGet` example from the `httpClient` library and got it sending requests to my server. i wanted to fetch random lyrics from my api so i gave the `client` constructor the port (8080) of that api's express script. i was successfully fetching the data, but i was quite confused because i was getting back old html from my server that i could have sworn i deleted. i realized i had never updated my `index.html` page from an older idea for the api. i changed that in real time as the arduino was making calls to the server so it was a fun experience to see the response change as soon as i saved the `index.html` file on my remote host.

the response changing in realtime:

![[week 11-1794945004765.webp]]

it was a little confusing that with just the port number it could reach the express script even though the request was just calling the `world-clique.club/`. i tried setting the port to 80 and calling the full url `world-clique.club/lyrics` but i kept getting a `301 moved permanently` response. i also tried changing the port to 80 and calling  just the base url `world-clique.club/` again but i still got the 301 response. i'm not sure why this didn't work.

i reset the port to 8080 and decided to just call the script from the `lyrics/random` endpoint.  the `client.get()` function has a string passed to it as the endpoint to which it would send its request. i wanted to make that a variable so i could change it on the fly, so i instantiated a variable `char endpoint` and passed that to the `client.get()` function. i immediately got this error: `Compilation error: invalid conversion from 'const char*' to 'char' [-fpermissive]` which caused me a headache for a bit until a few google searches and a stackoverflow post gave me the simple solution of renaming the variable as `char endpoint[]` which solved the error. from what i understand calling it with the brackets allows for strings of different lengths to be passed whereas the `char endpoint` on its own did not. i noticed up above in the code that the `char ssid[] and char pass[]` both were defined the same way. i'm guessing these are declared like this because the `ArduinoHttpClient` has written functions that expect that data type in order to be flexible with the lengths of strings that are passed in because urls vary so much terms of length.

![[week 11-1794945016618.webp]]

finally, i successfully got my code working and the lyrics to a random song coming every five seconds!
![[week 11-1794945028947.webp]]