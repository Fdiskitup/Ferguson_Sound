The VGM (Video Game Music) player .com file is used by typing :
6VGMPLAY Filename.VGM 
where file name is the name of the VGM you want to play.  simple enough. 
7VGMPLAY.COM and 6VGMPLAY are basically the same but a single NOP delay difference means that 6VGMPLAY.COM plays the files slightly faster.  
Files come in a mixture of formats, VGM files from the BBC micro use a 4mhz clock chip.  Other formats, Sega, etc, use a 3.57 NTSC 60Hz clock.  
Add to that the possibility for a 2.5mhz Ferguson cpu clock with the PSG requirement for 32 clock cycles between data writes and you can see how a variable delay might be needed.  
Ideally we could add it as a command line switch or even a keypress during playback.  A volume attenuation control migt also be nice during playback.  
