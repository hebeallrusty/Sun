# Sunrise / Set calculator

This project calculates the sun rise and set times (including Civil Twighlight, Nautical Twighlight, Astronomical Twighlight and the 'Golden Hour')

Returns time decimally and does not use the datetime library so can be used with micropython or python interchangeably (code was written on a pi pico rp2040)

Returns a dictionary containing the rise and set tuple (or False if the sun does not rise/set at location)

Algorithm is based on that within Almanac for Computers, 1990; of which an example webpage is given, and it is this method that is followed.

All inputs are decimals

Usage:
SunTimes(Year, Month, Day, Latitude, Longitude, Optional:Timezone offset)

Examples:
```python
from Sun import SunTimes
a = SunTimes(2023,5,7,55.885,-3.764,0)

# for full list:
print(a)

# for Official times:
print(a['Official'])

for Setting Time:
print(a['Civil'][1])

for Rising Time:
print(a['Civil'][0])
```


