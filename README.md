# Filament "Pre-Extruder" for 3D-printers

## Why?

The idea is to overcome the friction in the reverse bowden and spool holder that the main extruder has to work against by pre-feeding the main extruder.

## What is it?

An open-source Klipper-enabled filament-pushing "pre-extruder".

## How?

The implementation is via a bunch of Klipper Macros and "[extruder_stepper]" that's linked to the main extruder.

<p align="center" width="100%"><img src="/images/fp_c3.png?raw=true" alt="3D CAD View" width="600px" /></p>

<p align="center" width="100%"><img src="/images/fp_r2.jpg?raw=true" alt="The assembled pre-feeder proto" height="600px" /></p>

The yet-untested main idea is that the pre-feeder extrudes a tad more than the main extruder consumes, thereby creating "pressure" inside the reverse bowden. Then there is in turn a little switch on the pre-feeder and a flexible mechanism and once the pressure reaches a certain level the switch is triggered. That then triggers a Klipper Macro which reduces the rotation distance (thereby reversing the differential speed of the pre-feeder) and reducing the reverse bowden pressure until the switch is released, when the rotation distance is again restored and pressure slowly built up again.

<p align="center" width="100%"><img src="/images/fp_r1.jpg?raw=true" alt="The switch and spring mechanism" width="600px" /></p>

## Video of it working

<div align="center" width="100%" markdown="1">

  [![Short Video of both extruders extruding](http://img.youtube.com/vi/s7kXcfv4JuY/0.jpg)](https://youtube.com/shorts/s7kXcfv4JuY "Short Video of both extruders extruding")
  

</div>

## CAD

The CAD is available here as STEP and [in OnShape](https://cad.onshape.com/documents/6f2557d9a5eb1b365c3bf8f4/w/888f8c00c1b7e363eace9395/e/1c5648967865eb9401f046b9)
