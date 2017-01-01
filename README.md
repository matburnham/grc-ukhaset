# grc-ukhaset
GNU Radio Companion UKHASnet decoder

A UKHASnet decoder written as a GNU Radio Companion flowgraph. I wrote this mainly to understand how to filter, demodulate, correlate and unpack a simple protocol before moving onto more advanced things.

![Flowgraph](/docs/flowgraph.png?raw=true "Flowgraph")
![Screenshot](/docs/screenshot.png?raw=true "Screenshot")

## Usage
1. Run in GNU Radio Companion.
2. See packet output in output.txt

## Known issues
1. I didn't figure out how to capture the packet length from the [UKHASnet protocol](https://github.com/UKHASnet/protocol/blob/master/protocol.md) after synchronising. This means the output text is never terminated.
2. My testing has been done with a node fairly close by, so the signal strengths are high and all over the band, I imagine the parameters will need to be adjusted to hear distant nodes better. If I could fix point 1 then I can remove the squelch which should give less environment and node consistent results.
3. I wanted to put the latest packet decode in a label on-screen but can't find a suitable widget which had a way to feed data into it.
4. The clock recovery using Mueller and Muller is probably wrong, but it works so I'm not changing what's not broke.
