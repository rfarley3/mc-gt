# Mapping of Track-Clip to MFX
This changes as the project file changes.
Reference of what is where.
See README for groups/themes and why the default order was chosen.


## Presets to Try
Here are some interesting combinations:
* Blues-Rock
	* 04-03 T-Scream
	* 05-04 Clean Twin
	* 07-05 (changed to Built-in 1)
* Jazz LP Bin Dive
	* 02-02 Compressor
	* 03-05 CE-1 (subtle level)
	* 05-03 JC-120
	* 07-04 Phonograph
* Top Gun:
	* 04-02 OD (change low, like boost)
	* 05-07 Plexi (high gain)
	* 07-05 (changed to 4x12 MS Stack)
* 90's Grunge
	* 03-05 CE-1
	* 04-07 OD-1 (Fuzz was too hard and couldn't approx Big Muff)
	* 05-06 M/B
	* 07-05 (changed to MS Stack)
* 70's Psychedelic Uni-Vibe
	* 03-04 TremCh
	* 04-03 OD (Fuzz was too harsh)
	* 05-07 MS1959I
	* 06-02 Phaser 1
	* 07-05 (changed to MS Stack)


## Mapping

Track 1, Drum
* 01-01 Empty Drum
* 01-02 Rimshot on quarter notes, sort of metronome

Track 2, Dynamics
* 02-01 No FX
* 02-02 Compressor
* 02-03 Gate (TODO this isn't noise gate)

Track 3, Filter and some Modulation/Pitch
* 03-01 No FX
* 03-02 Auto Wah
* 03-03 Pitch Shifter -12sem
* 03-04 Tremolo Chorus
* 03-05 CE-1

Track 4, Dirt, Tone producers
* 04-01 No Fx
* 04-02 Overdrive
* 04-03 T-Scream
* 04-04 Distortion
* 04-05 Fuzz (very harsh, more OD than fuzz sounding)
* 04-06 Tone Fattener .5 odd 1.5 even
* 04-07 GtAmpSim OD-1 (sounds different than 04-02 model)
* 04-08 GtAmpSim OD-2 Turbo
* 04-09 GtAmpSim Distortion (TODO dupe?)
* 04-10 GtAmpSim Fuzz (TODO dupe?)

Track 5, Amp Models
* 05-01 No Fx
* 05-02 HMS Distortion
* 05-03 GtAmpSim JC-120
* 05-04 GtAmpSim Clean Twin
* 05-05 GtAmpSim Match Drive
* 05-06 GtAmpSim BG Lead
* 05-07 GtAmpSim MS1959I
* 05-08 GtAmpSim SLDN Lead
* 05-09 GtAmpSim Metal 5150

Track 6, Modulation Tone modifiers
* 06-01 No Fx
* 06-02 Phaser 1 12-stage
* 06-03 Step Phaser
* 06-04 Multi Stage Phaser
* 06-05 Chorus
* 06-06 Hexa-Chorus
* 06-07 Tremolo Chorus
* 06-08 Space-D
* 06-09 CE-1
* 06-10 Juno-106 Chorus
* 06-11 Flanger
* 06-12 JD Multi
* 06-13 Chorus->Flanger

Track 7, Ambience, Speakers/Cabs, Some Delays
* All knobs 1 are MFX specific param
* All knobs 2 are Delay Send
* All knobs 3 are Reverb Send
* 07-01 No Fx
* 07-02 Lofi Compress 2 pre 5 type
* 07-03 Bit Crusher 120 sample 6 bit down
* 07-04 Phonograph 50,30,EP,64,64,64 3 tot noise 65 wow 39 flutter 80 rand
* 07-05 Speaker Sim JC-120 2 mic
* 07-06 Tremolo
* 07-07 Auto Pan
* 07-08 Slicer
* 07-09 Rotary
* 07-10 VK Rotary
* 07-11 Reverse Delay
* 07-12 Tape Echo
* 07-13 BPM Looper
* 07-14 DJFX Looper
* 07-15 Telephone-ish by Phonograph 20,10,EP,0,0,4 10 tot noise 0 wow 0 flutter 
* 0 rand 37 tot w/f

Track 8, Looper, set with record source of track 7

Scatter, no changes
