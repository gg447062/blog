
this week right after class i got a domain name, world-clique.club, and followed all the steps to use digital ocean's name servers and connect my domain to my public ip. it's now live at [world-clique.club](http://world-clique.club/). pretty exciting!

before getting the domain name, i was using 'undnet' as a temporary server name for my nginx config files. once i got the domain, i updated all the config files and the directory names, but i forgot a very important step that lead me to annoying 404 errors. when i updated the config file, i totally forgot to restart nginx so the config changes didn't take effect but the directory names had changed so it couldn't find the related files. i had to look up the command again, but running `sudo systemctl reload nginx` did the trick and once again my server worked as intended.

i then added the ssl certificate using certbot following the [digital ocean tutorial](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-20-04) and all went smoothly. my site is now secure!

![[week 9-1793850365834.webp]]

in the tutorial it mentioned adding this line to the server config : `add_header Strict-Transport-Security "max-age=63072000; includeSubDomains; preload" always;`. i wasn't sure exactly what it did or if it was absolutely necessary but i added it anyways just to see what would happen. i also didn't know where to add it because after running the certbot setup my nginx config file now had two `server {}` entries, one created by me and one created by certbot. i assume they both are reached due to the `301` redirect so i just put it in the `server {}` block that i wrote

as far as my api goes, i decided to make use of another api, the nasa eonet (earth observatory natural event tracker) [api](https://eonet.gsfc.nasa.gov/docs/v3#eventsAPI). i got pretty far along before i realized that they send an rss feed as a response, so i scrapped that idea. i decided to make a lyric archive for the band deee-lite which is the name-sake for my domain name. it's available at `https://world-clique.club/lyrics`

also, with arjuns encouragement i'm finally getting over my deep mistrust of vim and taking a stab at using it to edit my code files. i had one too many frustrating experiences trying to edit git merge conflict messages with vim, but with just a 5 minute intro to using it, i'm more open than i was before.

#nginx

