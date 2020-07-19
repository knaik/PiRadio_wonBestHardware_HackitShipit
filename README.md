# PiRadio
Backup of Demo

## Inspiration
My Inspiration was to embrace both the hack and nautical (pirate) theme of this hackathon. I am going for the hardware nautical theme. I wanted it to be completely portable so if I were on a ship, I would be able to use it without the need for any internet.

## What it does
It turns a Raspberry Pi into a FM Transmitter, that can connect with a bluetooth audio device, essentially making a pirate radio. It can play local files as well.


## How I built it
I used a raspberry pi, bluetooth adapter, raspbian linux, a couple of wires connected to the gpio, and blueAlsa as way to pipe audio it recieves. It relies heavily on (PiFmRDS)[https://github.com/ChristopheJacquet/PiFmRds].

Most of the work I did was actually creating scripts and setting up the proper parameters to allow the different libraries to talk to each other. 


## Challenges I ran into
I currently only have a chromebook and so getting that into developer mode and installing crouton and setting up a dev environment took as long as setting up the raspberry pi and configuring blueAlsa to detect bluetooth and pipe that to SOX. I also needed to find a old school fm reciever to be able to test it. I ran into some antenna trouble and finding a clean unused fm frequency that wouldn't get me in trouble with the FCC.

I also could not edit a nicer video for my project, because I am working from a chromebook, but I managed the main features of my setup.

## Accomplishments that I'm proud of
I am proud of how it is completely standalone. With a startup script, it shows up as a bluetooth device and after finishing boot, the raspberry pi will keep working as long as the battery bank works. I calculated that the battery bank would allow it run for (~1000mA draw for the rpi + bluetooth, with a 26800mAh battery bank ) 24ish hours. Skipping tracks or changing the gain on the radio, while making audio clearer, would cut down on the battery life run time.  


## What I learned
I learned a lot about lower level linux operations in how it handles Audio. I also learned to appreciate how much can be done with so little.


## What's next for PirateRadio
Currently HD Radio has been pushed for digital radio broadcasts, however the format is encrypted and a license is needed to run a "pirate" radio station. I would love to reverse engineer the broadcast format, the codec used is known but there is DRM attached unfortunately. Most radio stations still have a fallback, and the honda civic I used only has an analog radio. 

Something else that has interested me is going all in on ICECast and running an internet radio station. 

