# Using a Physical Preamp
I'm not a sound engineer and haven't worked on amps or played electric guitar 
anywhere near long enough to warrant you listening to me here. Don't be dumb. 
TODO TEST.

You can use send-return to use a physical/external pedal chain.
Some guitar preamps cab be used like pedals for color or overdrive (ex: Orange 
Terror Stamp, Katana FX Loop).
This will set up your 707 to provide pedals both before your amp and within your 
amp FX loop.

While the 707 uses newer modeling chips, it doesn't have all the guitar specific 
effects and modelers of the GT-1000, GT-1000Core, or GX-100.
You can still use their manuals/forum discussions for examples of wiring, 
pros/cons, etc.
Some Line 6 forums have good conversations about what you'll read here.


## Why
According to the internet, the best way to use a physical amp (preamp and/or 
cab) with fancy MFX pedalboards is what is called the 4 cable method (4 CM) for 
mono and 7 cable method (7 CM) for stereo.
The 707 has enough ins and outs to do 4 or 7 CM.

This would allow you to use a physical preamp instead of a GtAmpSim MFX.
No need to model if you have the real thing.
Also more compute for other MFX.


## Disclaimer
Danger, read up on 4 CM.
There are people who know what they are talking about, it's not me.
You are messing with lots of voltage and could destroy your 707, Amp, or both.

Big thing is if you have a tube power amp section it needs a load, don't bypass 
it or unplug the speaker.
If you have a solid state power amp section, it should be fine without a load.
But if you are following the above, you hopefully aren't bypassing anything.
Also, validate that the signal level from your preamp is safe for 707.
Finally, don't connect amp external speaker (might be labelled cab out) to 707 
input unless you know what you are doing (have the right L-pad/attenuator).

Default to guidance from GT models, but use your best judgement and don't take 
risks.


## How, at a High Level
Basically, use your amp's FX Loop (sometimes labelled Preamp Out and Power In).

* Guitar into 707 External input.
* 707 Send to Amp guitar input.
* Amp FX Loop Send to 707 Return.
* Sh+Input Send/Return POS set to track you want to use in chain.
* Use speaker modeling in your final track and MIX OUT should be what you want.

With speaker modeling off, the 707 can use your physical poweramp/cab.
* 707 MIX OUT to Amp FX Loop Return.

You could be mad here and put an external chain anywhere a wire goes in/out of 
the 707.
And anywhere it goes into the 707 could be stereo...


## Wiring
This is in terms of mono signal chain.
For stereo, you must split any TRS into two TS for Left and Right, or else 
you'll loose the right channel.
You'll also need to track which 707 MFX are mono vs stereo to avoid merging 
channels, the parameter guide shows which is what.

* Plug Guitar into 707 EXT IN L/MONO and set switch to LINE
* Sh+Input
	* EXT IN Mono
	* Turn large encoder down, set EXT IN VOLUME 0
	* REC SRC 7 or whichever you'll want to loop, like the final output track
* Plug Amp FX Loop Send into 707 RET L/MONO
* Sh+Input
	* Return POS 4 is the track with all the GtAmpSim preamp MFX, yay consistency
		* Changing Return POS conveniently also changes Send POS
		* You will not need to change POS track's Audio Insert
		* Returned audio is not sent through clip's MFX
			* so you can use any clip on that track
			* but will go through filter, pan
	* Return Level 255
	* Return Mono for 4 CM, Stereo for 7 CM
* Plug 707 SEND L/MONO into Amp Guitar In
	* Adjust Send Level low to high to protect preamp
* Plug 707 MIX OUT L/MONO into Amp FX Loop Return
	* Adjust MIX OUT Volume low to high to protect poweramp
	* Consider high pass filter to protect the speaker
