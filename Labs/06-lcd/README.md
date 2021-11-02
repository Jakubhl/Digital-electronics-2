# Lab 6: Jakub Hlaváček

Link to your `Digital-electronics-2` GitHub repository:

   [https://github.com/Jakubhl](https://github.com/Jakubhl/Digital-electronics-2)

### LCD display module

1. In your words, describe what ASCII table is.
   * ASCII
   => table with custom characters, which can be used to show on LCD display as one variable. All you have to do, is to write ASCII table coordinates of this custom character. 
   
2. (Hand-drawn) picture of time signals between ATmega328P and LCD keypad shield (HD44780 driver) when transmitting three character data `De2`.

D = 0x44 = 0b1000100
e = 0x65 = 0b1100101
2 = 0x32 = 0b0110010

   ![](images/prubehy.jpg)


### Stopwatch

1. Flowchart figure for `TIMER2_OVF_vect` interrupt service routine which overflows every 16&nbsp;ms but it updates the stopwatch LCD approximately every 100&nbsp;ms (6 x 16&nbsp;ms = 100&nbsp;ms). Display tenths of a second and seconds `00:seconds.tenths`. Let the stopwatch counts from `00:00.0` to `00:59.9` and then starts again. The image can be drawn on a computer or by hand. Use clear descriptions of the individual steps of the algorithms.

   ![](images/flowchart.jpg)


### Custom characters

1. Code listing with syntax highlighting of two custom character definition:

```c
/* Variables ---------------------------------------------------------*/
// Custom character definition
uint8_t customChar[16] = {
    // WRITE YOUR CODE HERE
  B00100,
  B01000,
  B10011,
  B10000,
  B10011,
  B01000,
  B00100,
  B00000,
  
  B00000,
  B11000,
  B00111,
  B00100,
  B00100,
  B00100,
  B00100,
  B00100
   
};
```


### Kitchen alarm

Consider a kitchen alarm with an LCD, one LED and three push buttons: start, +1 minute, -1 minute. Use the +1/-1 minute buttons to increment/decrement the timer value. After pressing the Start button, the countdown starts. The countdown value is shown on the display in the form of mm.ss (minutes.seconds). At the end of the countdown, the LED will start blinking.

1. Scheme of kitchen alarm; do not forget the supply voltage. The image can be drawn on a computer or by hand. Always name all components and their values.

   ![](kitchen.jpg)
