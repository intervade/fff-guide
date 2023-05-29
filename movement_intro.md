---
title: Movement
layout: home
---
# Introduction to Kinematics/Movement
No machine can operate without some sort of movement! Here are some ground rules.

- All systems of motion utilize an XYZ (Cartesian) coordinate system.
  - Except for polar printers, which use a cylindrical coordinate system.
- There must be at least one motor per axis.
- I am not including the E axis (the extruder) in these explanations.
- The pieces to be moved by the motors are referred to as the gantry.
- The platform where the print adheres is the bed.

With that said, let's actually start describing real machines.

- [i3/Mendel](#i3/Mendel)
- [Box Style](#Box Style)
- [CoreXY](#CoreXY)
- [Delta](#Delta)
- [Scara](#Scara)
- [Polar](#Polar)

## i3/Mendel
Without a doubt, this is the most prevalent motion system for consumer printers. It's seen everywhere from the Prusa MK4 to the infamous Ender 3.

Insert picture here

For these machines, the X axis is moved by a motor most often on the left side of the machine, tied to the X gantry where the hotend assembly is seen. The entire bed is the Y gantry, with a Y motor in the rear for it. The Z axis functions by moving the X axis up and down. However, with this being the most popular and cheapest option, there are many different factors to consider for it.

### The bed
As stated before, the heated bed is the Y axis. This means that even if the actual footprint of the frame is somewhat compact, the required space will always be larger than expected due to the bed moving back and forth, extending past the frame. Additionally, the bed is not exactly a light component, and if you ever look to push your machine to its limits in the future, the bed's weight will be one of the limiting factors. Keep in mind, that does *not* mean that this limit cannot be overcome.

### Z Axis
This is where flexibility in machine design plays a role. In machines that cut costs, there is often only one motor to support the Z axis from one side, leading to a cantilever design as on the Ender 3. As the X axis moves about, this can exaggerate the problem, but not always. If the printer is properly tuned, one leadscrew should be sufficient to get usable prints. Yet, it is agreed upon that having the Z axis support by two motors, one on each side of the X axis, is better overall. This choice is seen for example on the Prusa MK4.

## Box Style
Box style printers are also common, with the most popular example being the Creality Ender 5.

Insert picture

The X and Y axes are near the top of the machine, while the bed moves up and down. The Y motor is normally fixed near the rear of the build with one belt on the right and left to move the X beam equally. The moving X beam has the X belt, X motor, and hotend assembly.

### Z Axis
The Z axis for a box style or "bed dropper" can take multiple forms. Taking the Ender 5 once again, the bed is cantilevered with two smooth rods for support. The motion is generated from a single motor-leadscrew set up. However, this is the most basic form of the Z axis. There are options/mods to support the bed from one/two/three/ points.

- One point: simple, cheap
- Two points: more rigid assembly
- Three points: more rigid assembly, three-point auto bed leveling

## CoreXY
CoreXY takes the same general principles and machine setup as a box style, but the X and Y motors work in tandem. Both X and Y belts are connected to the X gantry, generally allowing for higher speeds and accelerations at baseline (without tuning e.g. [input shaper]). The same options for the box style Z axis apply.

## Delta
Delta printers are generally taller machines, since they translate three instances of vertical movement into XYZ motion. They have three motors, one per gantry, please finish this i dont understnad delta printers

## Scara
Imagine a robot arm printer! The bed is stationary, with the arm moving around it. The arm has two joints, corresponding to a motor each, resulting in XY motion. The Z axis results from a motor moving the arm up and down.

## Polar
Polar machines are interesting due to the rotation of the bed. Within the cylindrical coordinates, the bed rotating changes the angle, a motor moves either the bed or the hotend for the radius, and a final motor moving (most commonly) the hotend up in some way for Z.

Insert pic

## [I see some motion *systems*, how does motion actually work?]

[input shaper]: https://www.klipper3d.org/Resonance_Compensation.html
[I see some motion *systems*, how does motion actually work?]: https://github.com/intervade/fff-guide/pages/motion.html
