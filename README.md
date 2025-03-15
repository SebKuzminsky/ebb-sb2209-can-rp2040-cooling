The EBB SB2209 CAN (RP2040) overheats, which can lead to reduced
extruder torque, lost extruder steps, and in extreme cases MCU crashes.
It needs active cooling, especially in an enclosed machine printing
high-temperature plastics like ABS.

This repo contains a description of how I added active (forced air)
cooling of the EBB SB2209 CAN (RP2040) in the Stealthburner toolhead of
my Voron 2.4.


# The problem


## Intermittent failure to extrude

Extrusion would sometimes stop briefly and then restart, and sometimes
would stop and then never restart.

![](/images/extrusion-problem-0.jpg)

![](/images/extrusion-problem-1.jpg)

## High temperature readings

The NTC 3950 sensor on the EBB SB2209 CAN (RP2040) board would often
read >75 °C.




# The fix

The solution is to improve the cooling of the EBB SB2209 CAN (RP2040)
board.


## Heatsink

Make sure there's a heatsink on the SB2209 as shown
on page 9 of [EBB SB2209 CAN V1.0（RP2040）Build
Guide_20240626.pdf](https://github.com/bigtreetech/EBB/blob/master/EBB%20SB2209%20CAN%20(RP2040)/Build%20Guide/EBB%20SB2209%20CAN%20V1.0%EF%BC%88RP2040%EF%BC%89Build%20Guide_20240626.pdf).


## Better Stealthburner cable door cover

Replace the Stealthburner "cable door cover" with an alternate part that
has a fan mount and better ventilation.

I was using the stock Voron-Stealthburner
[cable_door_for_pcb.stl](https://github.com/VoronDesign/Voron-Stealthburner/blob/main/STLs/Clockwork2/cable_door_for_pcb.stl)
part, and I switched to a part called "Voron Stealthburner
EBB SB2209/2240 fan cover" by Sven Kah, available here:
<https://www.printables.com/model/986553-voron-stealthburner-ebb-sb22092240-fan-cover>

This cable door cover has holes for ventilation, and has a mount for a
30xx fan for forced air.

I know that some folks use alternate Stealthburner parts promoted by
BigTreeTech, if so you may have to find or design a different cable
door cover to fit your toolhead.  If you do, please open a PR to this
repo with the details.


## Fan

I'm using the 3010 24V Honeybadger axial fan from Fabreeko ($8):
<https://www.fabreeko.com/products/3010-performance-axial-fan>

Any 30xx fan should work, just make sure you match the fan to the voltage
available on the EBB SB2209 CAN (RP2040), which can be configured for 5V,
12V, or the board's supply voltage, 24V in my case.

The fan mounts pretty cleanly to the cable door cover, just threading
the screws into the plastic.  I used four M3x16 BHCS.

Other fans that people have recommended (i have no personal experience with these):
* Delta
* GDSTime
* NMB
* Noctua
* Orion
* Sunon
