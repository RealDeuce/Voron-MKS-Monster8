# Monster8 for Voron v2.4

This is the config and any other files I end up needing for my install
of a Monster8 in my Voron v2.4.  So far, I don't have the board in my
hands, so this is untested based on their github project here:
https://github.com/makerbase-mks/MKS-Monster8

[Monster8-Klipper.cfg](./Monster8-Klipper.cfg) is a generic Klipper config that contains instructions
for standard build sizes.
[Monster8-350x350x430.cfg](./Monster8-350x350x430.cfg) is for my build.

Once I decide how to mount it (likely across the rails in front of the fans),
I'll put the STL files for the mount in here too.

## Wiring
B stepper motor → Driver0:X\
A stepper motor → Driver1:y\
Z0 (front left) stepper motor → Driver2:Z2 (leaving an empty connector between B/A and Z0)\
Z1 (rear left) stepper motor → Driver3:E0\
Z2 (rear right) stepper motor → Driver4:E1\
Z3 (front right) stepper motor → Driver5:E2\
Extruder stepper motor → Driver7:E4 (leaving an empty connector between Z3 and extruder)\
X endstop switch → X-\
Y endstop switch → Y-\
Hotend heater → HE0\
Hotend thermistor → TH0\
SSR input → H-BED\
Bed thermistor → TB\
Inductive probe (with BAT85) → Z+\
Hotend fan → FAN0\
Print cooling fan → FAN1\
Controller fan → FAN2\
Exhaust fan → HE2\
Single-colour 24V LED strip → HE1\
MKS Mini 13864 v3 → EXP1 and EXP2

Note that you do not need to populate a driver for E3 since it's not used in this configuration.
