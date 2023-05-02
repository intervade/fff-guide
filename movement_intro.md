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

- [i3/Mendel](##i3/Mendel)
- [Box Style](##Box Style)
- [CoreXY](##CoreXY)
- [Delta](##Delta)
- [Scara](##Scara)
- [Polar](##Polar)

## i3/Mendel
Without a doubt, this is the most prevalent motion system for consumer printers. It's seen everywhere from the Prusa MK4 to the infamous Ender 3.

Insert picture here

For these machines, the X axis is moved by a motor most often on the left side of the machine, tied to the X gantry where the hotend assembly is seen. The entire bed is the Y gantry, with a Y motor in the rear for it. The Z axis functions by moving the X axis up and down. However, with this being the most popular and cheapest option, there are many different factors to consider for it.

### The bed
As stated before, the heated bed is the Y axis. This means that even if the actual footprint of the frame is somewhat compact, the required space will always be larger than expected due to the bed moving back and forth, extending past the frame. Additionally, the bed is not exactly a light component, and if you ever look to push your machine to its limits in the future, the bed's weight will be one of the limiting factors. Keep in mind, that does *not* mean that this limit cannot be overcome.
### Z Axis
This is where flexibility in machine design plays a role. In machines that cut costs, there is often only one motor to support the Z axis from one side, leading to a cantilever design as on the Ender 3. As the X axis moves about, this can exaggerate the problem, but not always. If the printer is properly tuned, one leadscrew should be sufficient to get usable prints. Yet, it is agreed upon that having the Z axis support by two motors, one on each side of the X axis, is better overall. This choice is seen for example on the Prusa MK4.

## Box Style

## CoreXY

## Delta

## Scara

## Polar
