# NahamCon CTF 2021

>
> Rnbochsr March 14, 2021
>

What follows are my notes and write-ups for the NahamCon CTF 2021. This was my second CTF. I managed a dozen solves and landed in the top 25%. I'm pretty pleased with not only how I did in the ranking, but I also learned some valuable techniques for doing better in future CTFs. 

I'm looking forward to my next one. 
 -- Bradley
 
 
## Solved Challenges

### Read the Rules
Author: @JohnHammond#6971
Please follow the rules for this CTF!
Connect here: `link`
Read The Rules 

View page source for the flag
Thank you for reading the rules! Your flag is: 
`flag{90bc54705794a62015369fd8e86e557b}`


### The Mission
View page source for flag.
Thank you for reading the rules! Your flag is:
`flag{48e117a1464c3202714dc9a350533a59}`  


### esab64
Author: @JohnHammond#6971
Was it a car or a cat I saw?
Download the file below.
Attachments: `esab64`

This is a reverse text decode in `base64`. Use `rev` or `tac` to reverse the encoded text. Then decode using `base64 -d`. Reversing one last time puts the flag in the proper order. I did it in pieces first but you can do it in one step:
`rev esab64 | base64 -d | rev`
`flag{fb5211b498afe87b1bd0db601117e16e}`


### Abyss
Author: @JohnHammond#6971
A Vortex? No... an Abyss.
Click the Start button on the top-right to start this challenge. 

This is a neverending stream of text and junk characters. I hit `esc` and held it down to try and break it to no avail. I then tried to copy the text from my terminal into a text editor. Then search for `flag{`.
That gave me the answer that was buried in the abyss.
`flag{db758a0cc25523993416c305ef15f9ad}`


### Shoelaces
Author: @JohnHammond#6971
Do you double-knot your shoelaces? You gotta keep'em tied!
Download the file below.
Attachments: `shoelaces.jpg`.

Ran strings on the image file and got the flag.
`flag{137288e960a3ae9b148e8a7db16a69b0}`


### The Villages
Author: HTB Village
Come join the party at the HTB Village, and track down a flag!
I solved all the village challenges the same way. You visit the Discord server and the flag is in the server title.

* HTB Village `flag{437f3e5ecdd39a29d695e2e31603f5b4}` 
* INE Village `flag{e713de181584836c9499811f13cb0e62}` 
* IoT Village `flag{1ff473816ef21857cc62f838e8a33fc7}` 
* Live Recon Village `flag{2795da9d0d2055d259a3fb4d6b78629c}` 
* Red Team Village `flag{fd59547d85953cac9dd5f378daed2157}` 
* UHC-BR `flag{120c45c7b99d8cba1567441f5bef599e}` 


### Merch Store
Author: @nahamsec#5814
Check out our Merch Store! A portion of the proceeds go to support Women in CyberSecurity @WiCySorg!
Perform some online reconnaissance to track down a flag on the merch store! 

View the merchandise page's source for the flag. 
`flag{fafc10617631126361c693a2a3fce5a7}`


## Unsolved Challenges

### Car Keys
Author: @JohnHammond#6971
We found this note on someone's key chain! It reads... `ygqa{6y980e0101e8qq361977eqe06508q3rt}`? 
There was another key that was engraved with the word `QWERTY`, too... 

This is a QWERTY cipher. I just need to find the right movement and offset.
`ygqa` should equal `flag`, but I can't find an encoding that matches that.

As luck would have it, my trusty cipher website simply had trouble with this QWERTY cipher. I'm not certain why, but it did. I was right that, based on the flag format, `ygqa` was `flag`. After the competition I tried a different website and solved for the flag without issue. 
`flag{6f980c0101c8aa361977cac06508a3de}`


### Eight Circle
Author: @JohnHammond#6971
Abandon all hope, ye who enter here...
Download the file below.
Attachments: `eight_circle`

This is a `Dante Cipher`. Need to find the proper encoding. 
Update - I saw the challenge title, read the quote, and assumed that the cipher had to do with Dante's Inferno. I focused my OSINT search around those parameters. That yielded a match to the `Dante Cipher`. Perfect. Or so I thought. I couldn't find the proper encoding to decipher the ciphertext. 

As it turns out, the parameters of my search were too specific, so I missed the correct cipher. Searching more broadly for a cipher relating just to `eighth circle cipher` would have proven successful. While the cipher was related to Dante's Inferno, I learned after the competition that an esoteric programming language was named after the Eighth's Circle of hell in Inferno, Malbolge. Using a translator for it yields the flag.
`flag{bf201f669b8c4adf8b91f09165ec8c5c}`


### Chicken Wings
Author: @JohnHammond#6971
I ordered chicken wings at the local restaurant, but uh... this really isn't what I was expecting...
Download the file below.
Attachments: `chicken_wings`


### $Echo
Author: @Blacknote#1337
So I just made a hardcoded bot that basically tells you what you wanna hear. Now usually it's a $ for each thing you want it to say but I'll waive the fee for you if you beta test it for me.
Press the Start button on the top-right to begin this challenge. 


### Pollex
Author: @JohnHammond#6971
Image File ????
Download the file below.
Some people seem to have trouble reading this, understandably so. Sorry. The flag ends in these characters: 8fe36bc00}
Attachments: `pollex`

This is image manipulation. I tried `strings`. I tried `whirl and pinch` in GIMP.


### Veebee
Author: @JohnHammond#6971
Buzz buzz, can you find the honey?
Download the file below.
Attachments: `veebee.vbe`


### Bionic
Author: @JohnHammond#6971
Thank you for taking on The Mission. You can begin by exploring the CONSTELLATIONS public website, constellations.page. CONSTELLATIONS has "tried" to reduce their attack surface by offering just a static website. But you might find some low-hanging fruit to get you started. You should find the flag for this challenge ON THIS constellations.page website. With the flag of this challenge, you should also find a new URL that will assist in the next challenge. After solving this challenge, you may need to refresh the page to see the newly unlocked challenges. 

Searched the page's source and found nothing. 
Didn't see any hidden links or images on the page. 


### Treasure
Author: @congon4tor#2334
This movie is what pushed me to get into hacking. Good luck decrypting my note, I'm elite.
Download the files below.
Attachments: `note.txt` & `hackers.txt`

It is some cipher probably based on 13375p34k. I coudn't find the proper encoding.


### eaxy
Author: @JohnHammond#6971
Crypto is eaxy, it's all about math and keys :)
Download the file below.
Attachments: `eaxy`

Math and keys... Now I just have to figure them out. 
Could it be as easy as a ROT5 cipher? No, I tired that.


### DDR
Author: @JohnHammond#6971
It's Dance Dance Revolution! You already know how to play!
Download the file below.
Attachments: `ddr.png`


### Dice Roll
Author: @JohnHammond#6971
When you have just one source of randomness, it's "a die", but when you can have muliple -- it's 'dice!'
NOTE: You are welcome to "brute force" this challenge if you feel you need to. ;)
Download the file below and press the Start button on the top-right to begin this challenge.
Attachments: `dice_roll.py`

You get the Python script. It seeds the dice, how ever many of them there are, with 32 bits of randomness. Now you have to guess the upcoming number. 


### Prison Break
Author: @JohnHammond#6971
Read the `flag.txt` file that is `/just/out/of/reach`.
Press the Start button on the top-right to begin this challenge. 

This is a priveledge escalation challenge.


### AgentTester
Author: @jorgectf#3896
We've recently hired an entry-level web developer to build an internal system to test User Agents, let us know if you find any errors!
Download the files below and press the Start button on the top-right to begin this challenge.
Attachments: `agenttester.zip`

