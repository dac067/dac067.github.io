---
layout: post
title:  "MIDI Ondes Martenot"
date: 2016-09-20
categories: [front, electronics]
thumbnail: ondes.jpg
---

![post-image]({{site.url}}/assets/ondes.jpg)

This is a MIDI controller that is based on the Ondes Martenot.

![post-image]({{site.url}}/assets/ondes4.jpg)

The Ondes Martenot is a French electronic instrument that was invented in the 1920s. It is
a synthesizer that uses a pulley system for controlling and playing notes. Instead of discrete
notes like a piano, the stringed pulleys allowed the users to slide between notes and octaves
without "steps". It is very similar to a Theremin, except that there is a physical interface
rather than playing in air.

My project utilizes Serial communication to route MIDI messages into a synthesizer program
to mimic the sound and interface of the Ondes Martenot.

![post-image]({{site.url}}/assets/ondes3.jpg)

For my variation, I wanted to capture the feel and vibrato capabilities of the ringed pulley
system. The main components of my project was an Arduino and a 10 turn potentiometer. The
Arduino uses analogread() to measure the voltage of the potentiomenter and maps that to a range
between 0 and 1023. The 10-turn capability allows for more precise control, a larger resolution,
and essentially more note capabilities. <br>

The shaft of the potentiomenter is attached to a plastic pulley. A string connects the
four pulleys of the project together. A spring is connected in the string loop to keep
everything in tension and minimize slippage. A wooden ring is also tied in the loop for
the user to slide with.

Other hardware components include
<ul>
<li>Microswitch for on/off</li>
<li>Slide potentiomenter for volume control</li>
<li>Row of 24 LEDs</li>
<li>Three 8-bit shift registers</li>
</ul>

When the microswitch is pressed, the synthesizer plays the note Middle-C.
The potentiometer controls the pitchbend amount of the played note. Sliding the ring right
shifts the note to a higher octave. Sliding the ring to the left shifts the note to a lower
octave.

The 24 LEDs are mapped to the current pitchbend amount. The 0-1023 resolution of the potentiometer
is subdivided into 24 sub-intervals. A LED lights up when the pitchbend value is within its subinterval.
The LEDs are controlled by three daisy-chained 8-bit shift registers.

![post-image]({{site.url}}/assets/ondes2.jpg)

On the embedded-code side, the Arduino reads digital values from the various potentiometers
and translates them to MIDI messages. A MIDI message is essentially a 8-bit number, of which
the the first 4 bits correspond to a certain command. The last 4 bits correspond to the value
to operate the command on. For example, 1001xxxx is a NoteOn event. The remaining 4 bits determine
the note that is played.

The Arduino sends these sequences into the Serial port of the computer via USB. A program called
"Hairless-midi" routes the Serial port output to a MIDI port. The MIDI port is then configured
with synthesizer software to play the notes. I am using KORG M1 because it had the highest
pitchbend capabilities so that I could cover more octaves.

This MIDI controller project is alright for the most part. A notable problem I had is that
the string slips from the pulley during slides. This results in inconsistencies when playing
notes. A specific position on the board won't always match with a specific pitchbend. The string
and pulley have to be reset between playing sessions.

For the next version of this project, I plan to ditch the potentiometer all together and
replace it with a soft touch strip. A touch strip is essentially a potentiometer, where
its resistance is controlled by pressure along the strip. With this, I would eliminate the
pulley slide problem without losing the feel and vibrato of the Ondes Martenot.
