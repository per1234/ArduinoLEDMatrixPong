# Sure Electronics 16x32 bi-color LED matrix Arduino library

## The display library

### Principle

This library manages all the communication between the Arduino and the LED matrix.

It works using a local buffer: draw all you want in the local buffer using the clear() and draw(x, y, color) functions. Once you are done, send only the parts which have changed to the screen using the function commit().

### Installation

The library is made of only 2 files:
 * led_matrix.h contains the functions declaration and documentation,
 * led_matrix.cpp contains the actual code.

Add both files to your sketch directory and add this line on top of your sketch:
#include "led_matrix.h"

Then you can use the LEDMatrix class provided by the library. Read the .h file for more information.

## The pong example

The pong example is based on the one found here: http://scuola.arduino.cc/en/content/controlling-sure-electronics-3216-led-matrix-arduino-uno . The principles for writing the display library were also found on this page.

It is a bit improved:
* It obviously uses the library available here.
* The screen is not blanked at each step any more, which prevents blinking, and improves the speed.
* You can set the game speed using a third potentiometer.
* It is easy to set the game speed, bars size and number of points in the code.
* The Game Over "wave" changes direction depending on the winner.

The circuit to build is almost the same as on the version here: http://scuola.arduino.cc/en/content/controlling-sure-electronics-3216-led-matrix-arduino-uno . You just need to add one more potentiometer (on A2 by default) to set the ball speed.