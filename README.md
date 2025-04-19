# Ferguson_Sound
A soundcard for the Ferguson Big Board based on the 76489 PSG.   

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

