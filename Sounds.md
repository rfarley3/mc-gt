# MC-x0x Sound List Introduction

The sounds (Tones, Drums, Partial PCMs) don't have very intuitive names and 
there's no search on the x0x.
See [this](https://mc101soundlist.neocities.org/) for the 101 (missing the PCM 
and PCM-Sync entries) and [this](https://eriser.github.io/707/) for the 707.
Also, you can download `MC-707_SoundList_multi01_W.pdf` from Roland and search 
it.


## What do the sections in the PDF mean?
The sounds are in sections Tone, Drum Kit, Drum Inst, PCM Wave, and PCM-Sync 
Wave.

* Tones are for Tone tracks
* Drum Kits are for Drum tracks, and are pre-grouped Drum Instruments
	* There is a mapping of pads to instruments in the PDF
		* Usually bottom from left is kick, snare, 3x toms, 3x others; top is rim, 
		clap, closed high hat, open hh, 2x cymbals, tambourine/maracas, 
		cowbell/style-specific thing
	* Most of the kits are mixed, so a 909 will have some 727, 707, etc.
	* You can change a kit in your project (Sh+pad, Enter, Inst Select) without 
	changing the preset for other projects; same if you chop/load samples/wavs 
	into a project's drum track's pads
* Drum Instruments are assigned to pads in Drum Tracks
* PCM Wave are the possible wave/samples used in partials (Sound Design) when 
OSC OSCType is set to PCM, there are banks as well as a number
* PCM-Sync Wave are the possible wave/samples used in partials (Sound Design) 
when OSC OSCType is set to PCM-Sync, there are no banks, just a number


## What do the banks mean?

TODO some seem to be only VA, others PCM and LA.


## What Instruments are on the 707?

TODO make script to replicate this from PDF starting with parser from 
[this](https://eriser.github.io/707/) and its 
[repo](https://github.com/eriser/707).

Reviewing sound names reveals a number of devices named, abbreviated, or 
implied. This list shows the specific device (or its family, ex: Juno) and then 
lists its various substrings within presets.
There appear to be about 40 Roland devices and 5 non-Roland.

The presets don't always start with their device name, and sometimes they aren't 
surrounded by spaces (ex: ClassicJPpad, SL-Jn60sub1). Any case variants are 
included here.

Some prefixes indicate groups, such as SL for Synth Legends. Some of the presets 
have trailing MFX indicators, such as `w` for wide stereo (SDD-320, but 
sometimes CE-1), `comp` (compression via Equalizer), `w comp` or `w cmp` 
(SDD-320, not sure how the compression is done).
There are others like Lim (limiter), Atk, Bit (Bit Crusher), Dly, Rtry (Rotary), 
Trem, Cho, etc.

You can use this list as a reference to decode the preset name while scrolling, 
or to search the presets to find all the sounds for a particular device. Not all 
of these are in all sections (tone vs drum vs partial).

* Jupiter: Jupiter, JP, JP-4, JP6, JP8, JP-8, JP8000, JP80, JX-8P, JX, MKS-80 
(rack mount JP-8), XV, 5080 (rack mount XV-5080), JV, 1080 (rack mount JV-1080)
* Juno: Juno, JUNO, Alpha, Juno-D, Ju-D, JD, JD-8000, JD80, 106, Jn106, Jn60, 
Juno60, MKS-50 (rack mount Alpha Juno)
* SH: SH, SH101, SH-101, 101, SH-2000, SH2
* TR transistor rhythm: TR-606, TR-626, TR-707, TR-727, TR-808, TR-909
* CR-78 CompuRhythm: CR-78
* TB-303 bass line: TB, TB-303, TB303
* D-50: D-50, D50
* RD-1000 digital piano: RD-1000
* MC micro composer: MC500, MC202, 202
* GR guitar synthesizer: GR-300, GR-500, GR-700
* AX keytar: AX
* VP-330 vocoder and synth: VP330
* TM-2 trigger with drum kit: TM-2
* Pro-E, E-70 Music Style Card: SC1
* Moog: MG
* Prophet: P5
* Oberheim: OB
* Yamaha: CS
* Rhodes: MK-80
* Unknown
	* D-2000 (RD-2000?)
	* Compu (CR-78?)


## There are also named and inferred devices in MFX

TODO capture those.
