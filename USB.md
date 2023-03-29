# Using USB with 707
How to hook up USB across various operating systems.
This is necessary for MIDI, but for sending audio to 707, you can skip USB and 
use the computer headphone/line out.
In which case, set GarageBand/DAW/OS output to External Headphones and follow 
the README Stereo Headphone Amp.

## Vendor vs Generic
It's easier to just use Generic, unless you need separate tracks.

Generic channels:
* 707 `Mix Out` is Mac `Audio IN`
* 707 `PC IN` is Mac `Audio OUT`

Vendor channels from Computer to 707 (p. 121):
* L & R channel to computer are 707 name
* 1 & 2 are `MIX`
	* p. 32 if USB Mix Select is POST-T-FX then will not record source of MIX OUT
	* With PRE-T-FX, then USB can be recorded because it will be mixed into source of MIX OUT (p. 121)
	* You can not insert MIX
* 3 & 4 are `PC` aka `PC IN` (p. 32)
* 5 & 6 are `Assign`, which is like MIX but also includes delay, reverb, all 
T-FX
	* You can not insert Assign

Vendor from 707 to Computer (p. 121):
* 707 name is L & R channel to computer
* `Mix Out` is 1 & 2
* `Ext In` is 19 & 20
* `Track 1` is 3 & 4
* `Track 2` is 5 & 6
* `Track 3` is 7 & 8
* `Track 4` is 9 & 10
* `Track 5` is 11 & 12
* `Track 6` is 13 & 14
* `Track 7` is 15 & 16
* `Track 8` is 17 & 18


## Mac
* MIDI > MIDI Status shows 1 MIDI Input Detected
	* Optional, MIDI isn't necessary for audio
	* You should see some up and down triangles
	* Use down to send test MIDI to 707
	* Watch for up triangle to turn blue when you send MIDI from 707
	* Also consider something like MIDI Monitor.app
	* You will have a different device for generic vs vendor driver
* Generic I/O config
	* Settings > Sound
		* Input `Audio IN`, or just use GarageBand/DAW preferences
		* Output keep on MB Pro Spkr or External Headphones
			* Just use GB/DAW preferences
			* If you want all system sound, then `Audio OUT`
	* GarageBand
		* Create New Track, Audio mic/line, Input 1 & 2, check I want to hear
		* Create New Track, Software Instrument (MIDI VSTi)
* Vendor I/O config
	* Audio MIDI Setup > MC-707
		* Output 44.1
		* Configure speakers, use channels 3 & 4
	* Settings > Sound
		* Input `MC-707`
		* Output keep on MB Pro Spkr or External Headphones
			* Just use GB/DAW preferences
			* If you want all system sound, then `MC-707`
	* GarageBand
		* Create New Track, Audio mic/line, Input 1 & 2, check I want to hear
		* Repeat for 19 for raw version of EXT IN L/MONO if needed
		* Or for 19 & 20 for raw version of EXT IN
		* Repeat for 3-18 for tracks 1-8 as needed
		* Create New Track, Software Instrument (MIDI VSTi)


## Linux
* Must use Generic driver (although I have seen a post saying Jack can support 
		Vendor driver, but I haven't confirmed)
	* lsusb shows as MC707 USBAudio
* I had luck with Alsa stereo hw1:0
	* Audacity and Helm worked, Ardour needs more time to figure it out
* Good app to sniff MIDI is TODO


## 707
* Sh+Knob > System CTRL/COM
	* USB Mix Select PRE-T-FX
	* Direct USB Mixout Off
		* Volume knob controls USB volume
	* USB Driver Generic
		* Restart if changed
* Sh+Project
	* PC IN PC Level 0
	* Do this for same reason as setting EXT IN Volume to 0 for a Mic
* Sh+Sel (track you want to use for audio from computer)
	* Audio Insert PC IN L/R
* Sh+Input
	* REC SRC (the track you inserted into)
* Plug in USB to computer
	* Be sure to leave space for any headphones you need to plug in
* To send MIDI to computer, make a TONE track, Sh+Sel > MIDI
	* Tx USB MIDI on
	* Tx USB MIDI NOTE on
* To sync DAW via MIDI, Sh+Knob > System CTRL/COM
	* MIDI Sync INT
	* MIDI Sync Out USB on
	* Rx Start Stop on
	* Rx Start Stop USB on
* To recv MIDI from computer, Sh+Knob > System CTRL/COM
	* MIDI Rx AutoChannel 12 (to avoid v1.8 Arp bug)
