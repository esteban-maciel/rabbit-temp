# Rabbit Temp

Sense Hat API Ref: https://pythonhosted.org/sense-hat/api/

## Boilerplate

Import the sense_hat library and create an object to control the hat.

```python
from sense_hat import SenseHat
sense = SenseHat()
```
## LED Matrix Notes

We want to set the color of the LEDs on the hat depending on the temperature. Something like:

Red (too hot or humid)  : 66 >

Green (ideal temp)      : 60 - 65 F

Blue (too cold)         : 64 <


Set these ranges in python in case we need to change them later on:

```python
import math

red = range(66, math.inf)
green = range(60, 65)
blue = range(-math.inf, )
```

We can set the color of the entire matrix using a list of 64 lists that use RGB for the color code. For example,

```python
from sense_hat import SenseHat
sense = SenseHat()



room_temp = #get the current temp from the sense hat.

if room_temp > 65:
    sense.setPixels([255, 0, 0])
