# Ferguson_Sound
A soundcard for the Ferguson Big Board based on the SN76489 PSG sound chip.   
![SN76489AN_soundboard1](https://github.com/user-attachments/assets/5053c796-8be4-4c9b-b8f4-1175f97176e0)

The parallel port on the Ferguson Big Board uses the Z80 PIO to give 2 x 8bit bidirectional user ports.  
This soundcard was created to make use of port A. 

The board itself is rather simple consisting of 3 parts. 

1, The programmable sound generator chip (PSG) SN76489 and clock crystal oscillator. 
2, The amplifier based on he classic LM386 op amp chip. 
3, The VU meter using LM3915N-1 to pulse the LED's in tune to the music.  

This is derived from several sources 
https://github.com/bchiha/Ready-Z80/tree/main/16-SN76489_Sound_Generator 

https://github.com/jblang/SN76489

https://github.com/abaffa/z80cpm_emulator

![Ferguson Sound FRONT](https://github.com/user-attachments/assets/09cd5240-40b9-423a-947e-0404da7a5da0)



So you've built the card: 

On the Big Board make sure you set the jumpers pins 7-8, 9-10, 11-12, 13-14, 15-16 all on.  This sets the port for output only.
see the single blue jumper and the 4 red jumpers.  
![FS-1](https://github.com/user-attachments/assets/c3136a83-06ee-40ab-99eb-81af4cd1815d)

You'll need to give the board +5V, I just brought a cable from the main board power block to the soundcard power block.  
The ground plane is connected to the 10 ground pins of the connector so you could just wire in a single 5V from the rails directly below the power connector.

JP1 = selects non-amplified or amplified output.  Non amplified goes to the 3.5 mm Jack then into powered speakers.   Amplified out can go direct into a 8ohm speaker or if to connect an RCA jack direct into a TV.   
JP2 = selects bar or dot mode for the VU meter (if installed) 
JP3 = selects to use internal audio for the VU meter, or external input for the VU meter (really just to test it.).    

I have tried with the 4MHZ full size dip 16 crystal oscillator, but I put in the footprint for the smaller oscillator package.  it should accomodate other frequencies 3.57mhz etc.  or you can steal a clock signal from the Z80-PIO pin 25 (Bandit !). 
similarly you can just jumper the power switch so its always on - you can always turn it down with the pot.       

So once it is built and jumpered, switch on and you should be treated to some excellent feedback.  
quickly boot into CPM and run the M.COM file to mute the noise, phew. 

The port resides at 08 and 09 hex 


