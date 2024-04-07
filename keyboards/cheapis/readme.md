# Cheapis
The keyboard was designed by [dotleon](https://github.com/dotleon). I thought it would be a fun experiment to try out Cheapis with Gateron Low Profile switches. I searched for a lot of keyboards that supported low profile switches, but I couldn't find any that supported non-Choc or non-Cherry switches. They're not available in India at the moment.

Another thing is that the PCB was less than 100x100mm, so I got it manufactured for cheap. The original Cheapis uses a 7x10 layout, where you have:
1. 7 rows - 3 on each side with 5 keys, and 1 row containing the thumb cluster of both sides (4 keys)
2. 10 columns - Columns 4,5,6,7 have 4 keys (thumb cluster), and the rest have 3 keys.

I changed it to a 8x10 layout:
1. 8 rows - 3 on each side with 5 keys, and 2 thumb rows (1 for each side) containing the thumb cluster for that side (2 keys)
2. 10 columns - Columns 4,5,6,7 have 4 keys (thumb cluster), and the rest have 3 keys.

I have also used another pin instead of having the wire that goes from the left side to the right side. Since I'm using a breadboard, I can do all sorts of manipulations on it.

Extra steps to remove the direct wire connection between the two sides:
1. Solder the pads on both sides that says `left side of controller`. The right side was needed in the original too. You can solder any one side of the PCB, just remember to do it for both halves.
2. With this, pin 2 from top in Left side has become the row pin for Left thumb cluster. However, as we have the MCU soldered upside down, we need to get this to the other side. Pro micro has 8 pins on one side, and the other 10 on the other side. We've got it upside down, so the 10 pins are on the right side.
3. Connect the pin 2 from top on Left side to pin 1 in the right side using the breadboard. Voila, it should work now.

I also tried to get QMK to compile with RP2040, and it worked! I haven't tried it out yet though, since I don't have a RP2040 with me. The advantage of using RP2040 is that it has a more than 9 pins each side, which is what we need. So we don't have to do a left to right connection on the breadboard.
