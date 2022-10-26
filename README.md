# MC-GT
MC-707 and MC-101 (how-to and projects) for Guitar.


## Wiring
There are a few ways to connect things up.
You probably just want to do Raw/Direct from Guitar.


### Raw/Direct from Guitar
Plug into EXT IN L/MONO and set switch to LINE.
* Sh+Input
	* EXT IN Mono
	* Turn large encoder down, set EXT IN VOLUME 0
	* REC SRC 7 or whichever you'll want to loop, like the final output track


### Mono Headphone Amp, MFX with Line Out, or Pedal Output
Same as any mono line-in, ex: Raw/Direct from Guitar.
Use volume on device to avoid levels with distortion.


### Stereo Headphone Amp, MFX with Line Out, or Pedal Output
707 support Stereo input, if you need it to be mono, look up a Rane Why not Wye 
Stereo to Mono summer and follow Mono.
If you put a stereo (TRS) into EXT IN L, then you drop the Right (Ring) signal.
Stereo is same as mono, except:
* Use a TRS to 2 x TS adapter
	* Left (Tip) into EXT IN L
	* Right (Ring) into EXT IN R
* Sh+Input
	* EXT IN Stereo


### DI Box
Same as any microphone.
Plug into EXT IN L/MONO and set switch to MIC.
* Sh+Input
	* Mic Sense 7
	* EXT IN Mono
	* Turn large encoder down, set EXT IN VOLUME 0
	* REC SRC 7 or whichever you'll want to loop, like the final output track


### Using Return instead of EXT
You will loose the ability to use send-return loop (no 4 CM), but using EXT and 
Return gives you 4 channels of input, so you could put a microphone on EXT L, an 
EP on RET R, and the guitar on RET L.

Send-return POS is separate from Audio Insert.
Returned audio is not sent through clip's MFX, but does do filter, pan.
TODO verify if return requires line-in. It can not handle microphone. Unknown if 
707 return is designed for high-z input (Guitar). Assume RET must be line-in.

For mono:
* Plug into RET L/MONO
* Sh+Input
	* >>> RETURN Stereo, Level 255, POS Off
	* REC SRC 7 or whichever you'll want to loop, like the final output track

For stereo:
* Use a TRS to 2 x TS adapter
	* Left (Tip) into RET L
	* Right (Ring) into RET R
* Sh+Input
	* >>> RETURN Stereo, Level 255, POS Off
	* REC SRC 7 or whichever you'll want to loop, like the final output track


### Using a Physical Amp or External Pedals
TODO TEST.

See the GT-1000, GT-1000Core, or GX-100 manual for examples.
It should be possible to use the send-return loop to do a 4 CM (Cable Method).
Since send-return are both stereo, the 7 CM is also possible.
You can use this to send-return through a physical/external pedal chain,
or a physical amp.

This would allow you to use a physical preamp instead of a GtAmpSim.
Basically, use your amp's FX Loop (sometimes labelled Preamp Out and Power In).

* Guitar into 707 EXT L.
* Sh+Input Send/Return set to track with preamps.
* 707 Send to Amp guitar input.
* Amp FX Loop Send to 707 Return.

With speaker modeling off, the 707 could be both before and after the preamp,
but before the power amp, allowing you to use your physical cab.
For this, connect 707 line out to Amp FX Loop Return.

Danger, read up on 4CM. Big thing is if you have a tube power amp section it 
needs a load, don't bypass it.
If you have a solid state power amp section, it should be fine without a load.
But if you are following the above, you hopefully aren't bypassing anything.
Also, validate that the signal level from your preamp is safe for 707.
Finally, don't connect amp external speaker to 707 input unless you know what 
you are doing (have the right L-pad/attenuator).
Use guidance from GT models.

* Sh+Input >>> Return
	* POS 4 or whichever track is the preamp or part of chain you want external
		* Changing Return POS conveniently also changes Send POS
		* You will not need to change that track's Audio Insert
		* Returned audio is not sent through clip's MFX, but does do filter, pan
	* Level 255
	* Set Mono for 4 CM, Stereo for 7 CM


## Tracks
Chain the tracks, with only the final track's output in MIX OUT.
Final track's slider controls the volume for output (input through effects chain).
Final track's knobs control send to master delay and reverb.

This documentation leaves Track 1 and 8 free.
Track 1 could be a Tone (Aux backing track, external EP, external MIDI keyboard 
sending to Channel 1, Mic in, etc.) or a Drum sequence.
Following this documentation should set REC SRC 7, which makes Track 8 a great 
candidate for a Looper.


### Initial Track
* Sh+SEL for Track 2
	* Tone
	* Sound Source Clip
	* Audio Insert EXT L (unless stereo, then EXT L/R)
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
