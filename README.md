# Sound Study Modular AirWAV

##Information for re-use, adaptations or derivative works

Sound Study Modular is trademarked, and should not be used on any of works you create from these files.

We ask that if you want to re-use all or part of the files provided on github that you change the name of the product to something else

##What is this module?

The Sound Study Modular Air Wav is a virtual radio module, so it behaves a bit like a radio. It is designed to be a source of unexpected audio, not a drum loop player or a sample mangler.

Like a radio, this module works on a series of banks and stations. Each of the 16 banks can contain many different stations. Each station is .raw audio file stored in a bank directory on the SD card. Choose a bank by pressing and holding the RESET switch. Choose a station by turning the STATION knob or plugging a voltage into TUNE.
Detailed controls and displays
Adding samples to the SD Card

Full instructions and tools are in the <a href="http://www.soundstudymodular.com/assembly-instructions/air-wav-assembly-instructions/#sdCard">Setting up the SD Card</a> Section.

##Bank and meter LEDs

The LEDs at the top do two jobs. When audio is playing, they act as a simple VU meter. While choosing banks, they show the bank number in binary

- 0 ○○○○

- 1 ●○○○

- 2 ○●○○

- 3 ●●○○

- 4 ○○●○

- 5 ●○●○

- 6 ○●●○

- 7 ●●●○

- 8 ○○○●

- 9 ●○○●

- 10 ○●○●

- 11 ●●○●

- 12 ○○●●

- 13 ●○●●

- 14 ○●●●

- 15 ●●●●

##Station knob

This is how you choose which file to play from the current folder. It works exactly like a radio tuning knob.

You can put up to 75 files in each folder, but with that many files it might be hard to accurately tune to a station.
If you're between stations, you might get a rapid juddering sound as the module slips between stations. Just retune the knob. If you find it a big problem, put fewer files in each directory so the channels are more spaced out.
Like real radio stations, the files continue to play in the background - they don't re-trigger each time you select a new station.

##Start knob

This knob sets where the file will play from if you press the RESET button. It does nothing until you press the 'Reset' button! (This behaviour can be changed by editing settings.txt)

It's quite a coarse control, with a resolution of 512 steps. So, if you have a 30 minute radio show, the smallest shift you can make will be around 3.5 seconds. If you're playing a 4 second loop, the control will be finer.

##Reset button & LED

TAP the Reset button restarts the current track at the point determined by the Start knob or the Start CV input.

If you're playing a large file (a 30 minute .raw file is 150mb) it will take a few milliseconds to skip to the end of the file, so the button feels less responsive than it does with smaller files, or the earlier parts of bigger files.

HOLD the Reset button for more than 200ms to change banks. Keep the button held down to skip through all 16 banks.

Bank position is saved on the module after power-down.

##SD Card Slot

Full details of the SD file structure are here: <a href="http://www.soundstudymodular.com/assembly-instructions/air-wav-assembly-instructions/#sdCard">SD Card Details</a>

It's possible to hot-swap SD cards. If the module detects the SD card has been removed, it will reboot. When the module boots up, it looks for an SD card for a while - the bank LEDs flash when no card is present. After a while it will give up, and you'll need to turn the power on and off.

##Tune CV Input

This is the CV equivalent of the Station Pot. If the CV changes, the module will immediately re-tune to the relevant station.

The module 'understands' 0v to +5v signals, and is protected against higher or negative voltages.
The CV input is added to the knob position; if the knob is at 12 o'clock and 2.5v is applied to the CV, it's the equivalent of the knob being fully clockwise. Unfortunately you can't 'pull the pot down' by applying a negative voltage.

##Start CV input

This is the CV equivalent of the Start pot. Like the start pot, it does nothing until a 'Reset' CV is received. This CV input behaves like the Tune CV - it's zero to +5v, added to the pot position.
Reset Trigger input

A positive clock here triggers the reset button. It should not trigger the bank change.
##Output

This is a normal modular-level audio output.

The output level is set by the trimmer on the back of the module

The output is AC-coupled so cannot output control voltages
