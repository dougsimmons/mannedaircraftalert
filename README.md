# mannedaircraftalert
Analyzes ADS-B pings for flight paths to sUAS / model aircraft pilots to get out of the way, assisting the spotter.

Presently this is the beginning of a build log. Just at the idea stage. Though it's not the worst idea.

The purpose of this software (just starting the project) is to mitigate the threat of RC model aircraft flyers getting anywhere near the flight paths of manned aircraft not just to avoid a collisions and near-misses but to avoid disturbing the pilots and to mitigate the odds of any such noteworthy incident.

Especially relevant for RC clubs, further especially for RC glider/sailplane pilots who often exceed 400ft: AMA guidelines dictate that when high altitude flight is expected, a responsible and capable spotter must keep an eye out for manned aircraft to alert RC pilots to descend and get out of the way, and the spotter must take this job seriously. That's not only a vague definition for an important rule that could disqualify you from AMA insurance protection, if you've ever flown a glider in a sanctioned club, you know as well as I that guidelines tend to be forgotton. 

Large model gliders often exceed 1000ft. A 1.3m wingspan aircraft flown by an irresponsible pilot even without FPV can exceed 1500ft before losing visual orientation. I'm guilty of that. But a manned aircraft in a landing pattern that is flying 200 knots at 600ft toward the RC flying site rises above the auditory horizon line of the spotter at only 50km away from the field, yielding far too short a warning for all the glider pilots to duck down and clear the way safely. More than several seconds is necessary to hedge this threat.

For manned aircraft that are transmitting ADS-B and ModeS transponder pings, a device with antennas monitoring the common frequencies, in this scenario, yields at least 20% more distance of the RF horizon, and if the device has a connection to the Internet (via wifi, cellular modem, LoRa), it can process transponder pings from aggregator networks such as ADSBExchange, and also with the aid of known flight paths, it can identify flight paths of concern from a much greater distance.

I am building a birdhouse-sized setup using a Raspberry Pi, a cheap pair of antennas monitoring 1076MHz and 978MHz (the two common frequencies), a cheap USB cellular modem, a seven inch monitor and so forth, plus an inexpensive voltage regulator / buck converter, with common RC connectors, to take a lipo (or any other chemistry) of a voltage between 6V and 38V (two cell to eight cell lipo), ramps it down and outputs a SBC/Raspberry Pi-friendly 5.2V with up to 5A, probably sufficient to power the Pi, the two SDR receivers, the monitor and whatever else. No need for further power complications, no solar, no car battery, just bring the thing to the field and grab any lipo lying around, pop it in, it lights up. If the software determines there is an incoming flight path that poses a threat, the software triggers some sort of audible or visual alert.

The hard part of this project is not the hardware, it's programming the software to sound the alarm accurately, that is with as few false negatives and false positives as possible. A device that cries wolf will be soon ignored or discarded, and the opposite is also useless. 

I'm unsure of the best approach programming-wise, R, Python, something with machine learning, I don't know yet, but damnit I'll figure it out, and step one for me is to create this repo. I'll log updates of the project here. 

Cheers, Doug Simmons. 
