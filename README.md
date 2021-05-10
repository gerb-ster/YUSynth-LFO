# YUSynth LFO

I'm working on some new modules, one of them is this VC-LFO adaptation from YUSynth. As far as I can determine this is a VCO that generates a saw waveform which is then run thru some wave shapers to create a saw, tri, pulse and sine wave.

I've made some modifications:

- I've powered it with +/- 12v instead of the +/- 15v.
- I've ommited the range switch section, after breadboarding it I found the range with the 1 uF cap quite sufficient.
- I also changed some resistor values to make sure the output is 10vpp around 0v for all waveforms.
- I rearranged the wave shapers a bit; the tri/sine section comes after the saw buffer, this way the tri/sine section outputs a 10vpp around 0v without the need for extra components.

In the YUSynth design there was 1 unused op-amp section; I've used that one to invert the saw into an extra ramp output.

The original design:
http://yusynth.net/Modular/EN/LFO/VC-LFO2.html


## Status

- done: first schematic & board design
- done: breadboard and test
- todo: design frontpanel
- todo: order PCB and build prototype