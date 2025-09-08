<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works
This project implements a custom text scroller on a 7-segment display, showing the word “Cimarron UABC”.
Each character is represented by a truth table that maps the 4-bit counter output (Q3..Q0) to the seven display segments (a–g).
The combinational logic was minimized and implemented only with 2-input gates (AND, OR, NOT).
A synchronous counter built with D-type flip-flops generates the sequence of states 0 through 12, each corresponding to a character in the message.
When the counter reaches the last state, it resets to 0 and the sequence repeats, so the text scrolls continuously on the display.
## How to test
Open the project in Wokwi.
Run the simulation: the wokwi-clock-generator drives the counter, which cycles through the 13 predefined states.
Observe the output on the 7-segment display: the characters “Cimarron UABC” will be displayed in sequence.
You can adjust the clock frequency in the JSON configuration of the clock generator (e.g., "frequency": "1") to make the scrolling faster or slower.
## External hardware
7-segment display (common cathode, simulated in Wokwi)
Wokwi clock generator (simulated clock source
