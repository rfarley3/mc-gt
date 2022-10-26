# MC-GT
MC-707 and MC-101 (how-to and projects) for Guitar.

707 uses BMC, same as AIRD GT-1000 and GX-100, versus COSM in the GT-1, GT-100 
ESC2 chip, per FB group.
707 has JC-120, Clean Twin (Fender Twin Reverb), MS1959 I/II (Marshall 1959 
Plexi), BG Lead (MESA/Boogie), Metal 5150 (Peavey EVH5150), Match Drive 
(Matchless D/C-30), Sldn Lead (Soldano SLO-100).
GT/GX additionally has (what appears to be) Katana models, Fender Deluxe Reverb, 
Tweed (Fender Bassman), Diamond (Vox AC-30), Orange Rockerverb, Bgnr Ub (Bogner 
Uberschall high gain).
707 lacks variety of pedals, such as no subtypes for Overdrive, Distortion, 
Fuzz. Also lacks harmonist, spring reverb, and some more guitar centric effects.

Download [here](https://drive.google.com/file/d/1mEYfxMzKl6clu3RVLRFRe4MgGoXVuBfW/view?usp=sharing) v0 md5 6a14979d9c5432f797797a2da064b36b.

## Wiring
There are a few ways to connect things up.
You probably just want to do Raw/Direct from Guitar.


### Raw/Direct from Guitar
Plug Guitar into EXT IN L/MONO and set switch to LINE.
* Sh+Input
	* EXT IN Mono
	* Turn large encoder down, set EXT IN VOLUME 0
	* REC SRC 7 or whichever you'll want to loop, like the final output track


### Mono Headphone Amp, MFX with Line Out, or Pedal Output
Same as any mono line-in, ex: Raw/Direct from Guitar.
Use volume on device to avoid levels with distortion.


### Stereo Headphone Amp, MFX with Line Out, or Pedal Output
707 supports stereo input, if you need it to be mono to maximize input devices, 
look up a Rane 'Why not Wye' stereo to mono summer and follow Mono instructions.
If you put a stereo (TRS) into EXT IN L, then you drop the Right (Ring) signal.
Stereo is same as mono, except:
* Use a TRS to 2 x TS adapter
	* Left (Tip) into EXT IN L
	* Right (Ring) into EXT IN R
* Sh+Input
	* EXT IN Stereo


### DI Box
Same as any microphone.
Plug XLR into TRS adapter into EXT IN L/MONO and set switch to MIC.
* Sh+Input
	* Mic Sense 7
	* EXT IN Mono
	* Turn large encoder down, set EXT IN VOLUME 0
	* REC SRC 7 or whichever you'll want to loop, like the final output track


### Using Return instead of EXT
You will loose the ability to use send-return loop (so neither external pedal 
chain nor 4/7 cable method), but using EXT and Return gives you 4 channels of 
input. For instance, you could put a microphone on EXT L, an EP on RET R, and 
the guitar on RET L.

Send-return POS is separate from Audio Insert.
Returned audio is not sent through clip's MFX, but will go through filter, pan.
TODO verify if return requires line-in. It can not handle microphone. Unknown if 
707 return is designed for high-z input (Guitar). Assume RET must be line-in.

For mono:
* Plug Guitar into RET L/MONO
* Sh+Input
	* RETURN Stereo, Level 255, POS Off
	* REC SRC 7 or whichever you'll want to loop, like the final output track

For stereo:
* Use a TRS to 2 x TS adapter
	* Left (Tip) into RET L
	* Right (Ring) into RET R
* Sh+Input
	* RETURN Stereo, Level 255, POS Off
	* REC SRC 7 or whichever you'll want to loop, like the final output track


### Using a Physical Amp or External Pedals
Determine which track you want to use for the external pedal chain and use 
Sh+Input send-return position.

According to the internet, you should be able to use a physical amp (preamp 
and/or poweramp) with the 707 using what is called the 4 cable method for mono 
and 7 cable method for stereo.
I'm not a sound engineer and haven't worked on amps or played electric guitar 
anywhere near long enough to warrant you listening to me here. Don't be dumb. 
TODO TEST.
See write up [here](PhysicalAmpCab.md)

## Tracks
Chain the tracks, with only the final track's output in MIX OUT.
Final track's slider controls the volume for output (input through effects chain).
Final track's knobs control send to master delay and reverb.
Use master delay and reverb settings to save 2 tracks.
That's up to 10 chained effects (verified per FB group).

This documentation leaves Track 1 and 8 free.
Track 1 could be a Tone (Aux backing track, external EP, external MIDI keyboard 
sending to Channel 1, Mic in, etc.) or a Drum sequence.
Following this documentation should set REC SRC 7, which makes Track 8 a great 
candidate for a Looper.


### Initial Track
* Sh+SEL for Track 2
	* Tone
	* Sound Source Clip
	* Audio Insert EXT L
		* If stereo, then EXT L/R
		* If you used Return, then RET L for mono and RET L/R for stereo
	* Audio Output Assign (TODO there may be a better way, but it shouldn't be MIX OUT)


### Middle Tracks
* Sh+SEL for Track 3 through 6
	* Tone
	* Sound Source Clip
	* Audio Insert n-1
	* Audio Output Assign (TODO there may be a better way, but it shouldn't be MIX OUT)


### Final Track
* Sh+SEL for Track 7
	* Tone
	* Sound Source Clip
	* Audio Insert 6
	* Audio Output MIX OUT


## Optional Sane Settings
* Sh+Project
	* PC IN > PC LEVEL 0
	* Measure 1-4
	* COM > Project Level 127
* Sh+Input
	* Turn large encoder down, set EXT IN VOLUME 0 to keep it out of MIX OUT
	* Use Audio Insert for EXT IN to bind to a track
* Sh+Tempo
	* Turn large encoder to match BPM to what you are playing


## Playing
Create scenes of clips for presets.
Example: one type of Hendrix could be tremolo chorus into phaser 1 and plexi.
Alternatively, activate an entire empty row, then copy and paste any clip from 
any track (2-7) into that row in the order you want (in tracks 2-7).

Press play for Scatter to work, but be sure to set the BPM (Sh+Tempo).
TODO interesting scatters.

### Groups/Themes of FX per Track
Reference for [Roland view of categories](https://static.roland.com/manuals/SPD-SX_PRO_reference_v102/eng/30557213.html).
A [basic flow of guitar pedal chain](https://rolandcorp.com.au/blog/wp-content/uploads/elementor/thumbs/effects_chain-op5h7sbk8o9o0jmqhetslzqi7csgw6ascnpa8lczmg.png) with [write-up](https://rolandcorp.com.au/blog/order-effects-chain-simple-guide), ignoring how much of a personal preference this is.

For this project:
Track 1: Drums
Track 2: Dynamics (Compressor)
Track 3: Filter (Wah) and some Modulation/Pitch
Track 4: Dirt (Tone producers)
Track 5: Preamp (without speakers/cab sim)
Track 6: Modulation/Pitch (Tone modifiers)
Track 7: Ambience/Output (lofi/phono/tele, trem, pan, some delay, speakers/cab 
sim).
Track 8: Looper (record source track 7)
Master Delay and Reverb are on, Track 7 clips' knobs control send-to.

A mapping of which MFX is at which clip is [here](ClipMap.md).
