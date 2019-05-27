---
layout: blog
draft: false
title: "KMG Second Weekend: Saturday"
date: 2019-05-25T13:43:51+09:00
categories: journal
tags:
  - KMG
  - 3D Printing
  - laser cutting
---

Second weekend of training at KMG. Today Kenji hosted an Arduino workshop which involved building cars, the parts of which he had CNC milled and built in advance.

{{< img "arduino_car_workshop.jpg" "Arduino Car Workshop" >}}

The workshop was a big success, with around a dozen participants. The workshop practically ran itself, as everybody was focused on the task, and freely cooperated with each other to build the cars. (At Connor's request, I provided a quiet background of unreleased kqvc tracks on shuffle.)

Meanwhile, Connor showed me the layout of the workshop, explained the laser cutter in more detail, and taught me how to 3D print nylon.

# KMG layout

{{< img "clean_room_layout.jpg" "Clean Room Layout" >}}

Connor showed me the layout of the "clean room" which houses 3D printers and a laser cutter. The bottom shelves store resin, 3D printer filament, IPA, blocks for an ongoing KBC order, and other miscellaneous items. The top shelves have boxes for paint, glue, tape, and a box of various tools. Connor built a beautiful custom tool caddy out of laser cut parts.

{{< img "tool_caddy.jpg" "Tool caddy" >}}

Although the room is already fairly well organized, I made a list of some possible improvements:
- Clear plastic case to organize 3D printer nozzles
- Label and sort supply drawer
- Buy acetone (for 3D printer beds), and lens cleaner (for laser cutter)
- Remove and sort useful tools from donated red box, discard the rest
- Make labels for shelves and tool caddy

# Laser cutter

KMG owns a Trotec laser cutter. The sales-rep contact at Trotec is named Sato-san, and I should contact him for information about replacing proprietary parts such as the large cartridge filter. He also has information about a lens cleaner, which is apparently orange and superior to the current blue lens cleaner.

Connor showed me how to remove and clean the lens and mirrors. The lens is very delicate and expensive, so one must treat it with care, using a towel on the bed when removing it. One cleans the lens with lens cleaner and microfiber cloth, and takes care not to tighten too hard when re-inserting it.

{{< img "laser_cutter_lens.jpg" "Laser Cutter Lens" >}}

Connor also showed me how to adjust the air assist. The air assist blows the smoke created by the laser out of the way, to keep the lens clean and maintain laser strength. Therefore, the air should be blowing as close to the point of contact as possible. The metal frame of the air assist was bent, so we removed it and pried it straight. We also noticed that the hose coupler on the air assist was somewhat broken, and we need to order another one (after checking the size.)

There is apparently a way to test just the air assist with a piece of paper and combination of buttons on the machine, but Connor couldn't remember it so we just tested it by drawing some simple lines on a piece of scrap wood.
Before cutting one must calibrate the height of the bed with a "focus tool", a metal bracket with a brass piece which balances on an edge of the laser cutter. After balancing the tool, slowly raise the bed until it barely touches the tool.

I then took the opportunity to try out the different modes of the laser cutter. The primary cutting options are cut, vector engrave, and raster engrave.

## Cut
Cuts all the way through the material. If you cut too far, the material will be blackened. Fast speed and high power.

## Vector Engrave
Engraves a single line vector into the material. Slow speed (3% max) and low power.

## Raster Engrave
Engraves a filled shape into the material one line at a time. Fast speed and low-medium power.

You can specify the types of cuts by color coding an SVG in Adobe Illustrator or other program. The colors are customizable, but at KMG we generally use black for raster engraving, red for vector engraving, and blue for cutting. You generally want to cut last, as cutting out a shape makes the material loose, much as in CNC machining.

{{< img "laser_cutter_settings.jpg" "Laser cutter settings" >}}

# 3D printing nylon
Connor introduced me to his homegrown technique for 3D printing nylon on the Prusa MK3. Most people would not print nylon on an open machine, only on machines with a temperature-controlled chamber. However, Connor came up with a technique that works:

1. Change the nozzle from brass to hardened steel (necessary for nylon, as it is carbon fiber-filled)
  1. Raise nozzle temperature to 285℃.
  2. Lift up the extruder and turn the machine sideways for easier back access.
  3. Put cardboard on the bed to protect it when the nozzle falls out.
  4. Get a small 7mm wrench and a larger adjustable wrench.
  5. Grip the heater block with the adjustable wrench and loosen the nozzle with the 7mm wrench, turning counter-clockwise (when viewed from the bottom.)
  6. Unscrew the nozzle by hand.
  7. Replace nozzle with a hardened steel V6 nozzle by hand, then firmly tighten with wrench.
2. Perform first-layer calibration with PLA, but raise up a little bit to compensate for a layer of tape which will be placed on the bed.
  - To remove the PLA after calibration, perform a "cold pull" by setting the nozzle temperature to 95℃ and pulling the filament out. (Usually one performs a cold pull at 90℃, but steel nozzles often have a cooler temperature than the thermistor detects in the heater cartridge.)
3. Set nozzle temperature to 260℃.
4. Prepare a bed of masking tape on which to print the part.
  - Put masking tape on a piece of cardboard, coat evenly with spray glue 55.
  - Move masking tape onto the bed in the location of the print.
  - Rub tape flat with something not sticky (such as the glossy side of sticker paper) and a fabric button.
5. Print the part with 2mm retraction preset.
  - Note: Nylon filament must be kept in a dry box, at is quite sensitive to humidity. At KMG Connor has designed an ingenious dry box which sits on a rack, with a hole to feed into the machine.

The resulting print might be a little messy on the outside, because nylon heats at a higher temperature than PLA, but the small amount of mess can be sanded down or shaved off with a box cutter.

{{< img "rescued-earless-seal-3.jpg" "cute seal" >}}
*image from [Azarashi Paradise](https://twitter.com/aguhiyori)*
