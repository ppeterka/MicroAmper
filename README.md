#MicroAmper

Small size, full tube punch - and then some nifty features for home recording and practice, at a meager price. At least that's the plan :)

This is just a github page for a small DIY electronic project. And an experiment in how Github can be used for electronic DIY projects.

##Philosophy
The core is based on a simple yet fantastic 3 valve amp, but it is surrounded by components that round it out for anyone past 30, having kids, and no quality time for the 6 strings.

The goal is to have an amp head that is tonally versatile enough, and can be used either with a real speaker or without one, and still sound good and similar in both configurations - hence the reactive dummy load and the cab sim.

Also, to have a bit of depth, a reverb of some kind is required - that will be a story of its own as designing a reverb that sounds good is not exactly trivial or exact...

##Planned features
* Switchable boost/overdrive
* Low power output to be able to crank the hell out of the power section without getting arrested
* Real speaker out from the tube PA
* Dummy load for headphone/line-out applications
* Line out and headphone out with cab sim, and fake-stereo reverb (possibly also some kind of FX loop for those modulation effects and whatnot)
* Line in for bedroom pactice use - not passed to the line out (or switchable)
* Small as possible! Like fit into 33cm x 16 cm x 4.5 cm (Surprisingly I just happen to have a box that is exactly this size.)
* Powered from a generic 19V laptop charger. Yes, the voltages would be provided by SMPS modules
* Heater should be 6.3V, and should have a switch for ordinary/Russian double triode heater pinouts (6NxP valves for cheepz)

##Module plan

* Pre emphasis: Tube Screamer clone (Gain, Tone, Level controls and switchable clipping: something like symmetric, +1 Ge diode, +2 Ge diode)
* Preamp: AX84 ÜberSEL (2xECC83, high gain preamp, Gain, Bass, Middle, Treble, Level controls)
* Poweramp; AX84 Firefly power amp (1xECC82 self split PP)
* Reactive Dummy Load: by Aiken Randall 
* Cab sim: Condor cab sim from RunOffGroove (with the proposed Marshall characteristic)
* Reverb: fake stereo reverb based on Solstice by merlinb  (3x PT2399)
* Headphone amp: generic


## Resources

### Parts
 * Output transformer: http://hu.farnell.com/pro-power/ctfc6-4-5/transformer-6va-2x-4-5v/dp/1780836 
  * Not an audio OT - lets see how it fares. 
  * cheap, and seems decently sized for the 0.8-1W output provided by the planned output stage
  * small enough to fit the planned chassis
  * Zaa seems to be OK, as it is a 2x115V to 2x4.5V tranny, so the 4.5V would be good for 8R speakers
 * Box: It was the home of an SMC EZ Hub 100 5208TX 8port Fast Ethernet switch.
  * sturdy enough
  * size OK
  * con: holes in wrong places
  * some standoffs inside to hold PCBs and other stuff
  * there are 2 4cm diameter fan grilles on each side - can have mini speakers mounted there
  
## Modules

### Power
 * system power: generic 19V (or similar) laptop power adapter
 * high voltage: SMPS module that can supply up to 350V and 40W - plenty of power for all the stuff
  * Set to 300V?
 * 9V for the Tube Screamer clone
 * 6,3V for heaters: 3A buck module - should be enough, as ECC83s and ECC82s draw 300mA, and 900mA is well within the capabilities of the module.
  * might need some start-up magic not to fry the buck module when the tubes start cold
 * 5V: reverb circuits, headphone amp (amp for speakers inside, if there will be any)
  * 78L05 from 6.3V should do - or from 9V as that is less loaded, but that would mean power waste. Maybe an extra small buck module?
