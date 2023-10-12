# Filament "Pre-Extruder" for 3D-printers

An open-source Klipper-enabled filament-pushing "pre-extruder". The idea is to overcome the friction in the reverse bowden and spool holder by pre-feeding the main extruder.

The implementation is via a bunch of Klipper Macros and "[extruder_stepper]" that's linked to the main extruder.

The yet-untested main idea is that the pre-feeder extrudes a tad more than the main extruder consumes, thereby creating "pressure" inside the reverse bowden. Then there is in turn a little switch on the pre-feeder and a flexible mechanism and once the pressure reaches a certain level the switch is triggered. That then triggers a Klipper Macro which reduces the rotation distance (thereby reversing the differential speed of the pre-feeder) and reducing the reverse bowden pressure until the switch is released, when the rotation distance is again restored and pressure slowly built up again.
