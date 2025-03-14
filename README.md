The EBB SB2209 CAN (RP2040) overheats, which can lead to reduced
extruder torque, lost extruder steps, and in extreme cases MCU crashes.
It needs active cooling, especially in an enclosed machine printing
high-temperature plastics like ABS.

This repo contains a description of how I added active (forced air)
cooling of the EBB SB2209 CAN (RP2040) in the Stealthburner toolhead of
my Voron 2.4.
