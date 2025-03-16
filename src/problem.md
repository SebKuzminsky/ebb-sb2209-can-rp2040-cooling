# The problem


## High temperature readings

The NTC 3950 sensor on the EBB SB2209 CAN (RP2040) board would often
read >75 °C.


## Intermittent failure to extrude

Extrusion would sometimes stop briefly and then restart by itself,
and sometimes would stop and then never restart.

When i noticed that extrusion had stopped, i could pause the print and
manually command extrusion, and it would not extrude.  Then i would
provide just a little bit of downward force on the filament going in to
the extruder, and it would move freely and extrude fine.

This tells me the extruder was not clogged.

If i stopped pushing on the filament it would sometimes continue to
extrude fine by itself, and sometimes stop extruding again.

![](images/extrusion-problem-0.jpg)

![](images/extrusion-problem-1.jpg)
