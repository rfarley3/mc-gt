# Sane Settings for 707 Projects
Notes from the docs, various YouTube videos, and Roland training sessions.


## System
CTRL/COM
* Knob Direct
* Pad curve log
* Threshold 0
* Sensitivity 10 to 35
* Gain 0
* USB Mix Select PRE-T-FX
* Direct USB Mixout Off
* USB Driver Generic
* Call Scene type 2 (for banks)
* Output Cue to Mixout Off (means headphones only)

MIDI
* Sync On
* Sync Out USB On
* Control Tx On
* Control Tx USB On
* Rx Auto 9 to 15
	* Avoid 1-8 for v1.8 Arp bug, auto MIDI channel should not match any track 
	number

Metronome
* Type 1
* Level 12
* Pos phones
* Count in

Display
* Contrast 6
* Backlight 2
* Brightness 1
* Glow 2
* Demo 10

TODO motion, tempo, input


## Project
COM
* Project level 127
* Wave Preview 150-200
* Step len 64 (aka 4 measures between scene changes)

Sh+Tempo
* PC IN Level (set value)

Sh+Input
* EXT IN (set value)
* Mic Sens (set value, probably 7)

Sh+Note
* Chord designer type 2 (adds in more than 1+5)

Other things
* Track 1 delete drum and replace with drum with compressor
* Track 8 seems often reserved for looper


## Track
* Enter+Measure to change steps, 4 or 8 changes default clip step len
* Sound Source Clip
* MIDI Tx MIDI Note On (to send that track over MIDI)
* Hold Sel for the track to show level, pan, delay, reverb values
	* Use C1-C4 to change values, freeing up knob assigns (Filter, Mod, FX knobs)
	* C1 Level, C2 Pan, C3 Delay, C4 Reverb


## Clip
* Sh+Sound CTRL Octave +/- to avoid shifting octaves while changing tracks
* Sh+Quant Clip % (higher means less swing, but stays truer to manual entry)
* Scale changes pulse from 1/16 to 1/8
