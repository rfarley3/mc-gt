# Using MIDI to Control the 707
The [spec sheet](ffdfsdf) appears sparse, and while the MIDI implementation for 
the 707 and 101 is limited, there is more than that PDF.

There are 3 ways to use MIDI to control parameters.
1) CC mappings per the spec sheet
2) Knob Assigns and then using CC81-84 to control Knob 1-4, there are parameters 
here that are in neither CC nor Matrix
3) Use one of the possible matrix sources that are accessible via MIDI to 
control a destination parameter
	* Possible sources include CC numbers, sys-ctrl1-4, TODO the rest


## Other notes to help
What you cannot do:
* You can not control individual partials over MIDI unless through the matrix
	* For instance, some partials are not in a matrix's destination, or (and this 
	* is hard to explain in words, but idea from Ben Coe) creative uses of Step 
	* LFO values as the source with neg/pos depth, and you use the MIDI command to 
	* iterate the LFO steps.
* TODO more

Sanity checks:
* There are default matrix source/destinations in the Init patch that you should 
		double check.
* If you change a matrix in advanced mode, the simple mode will only show the 
		values for the first partial. I lost quite a while trying to figure out why 
		sys-ctrl1 was changing vibrato even when the simple menu showed no matrix 
		for it. Turns out partials 2-4 were still matrixing sys-ctrl1 to LFO Pitch 
		Depth.

# Table of Parameters to ways to call

