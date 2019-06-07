---
layout: blog
draft: false
title: "KMG Second Weekend: Sunday ー Injection Molds"
date: 2019-05-26T13:13:38+09:00
categories: journal
tags:
  - KMG
  - 3D Printing
  - laser cutting
  - Fusion 360
  - SLA
---

The last official day of KMG training. In the morning, Connor showed me how to design an injection mold in Fusion 360 and print it on the Form 2.

# Injection molds
An injection mold is a reusable mold into which you can inject molten plastic, allowing one to easily create many copies of a single model. KMG has an injection mold machine, which takes plastic pellets, melts them down, and injects them into a mold.

When designing an injection mold, one should first check the dimensions of the *sprue*, or the tube through which plastic enters the mold. The dimensions, along with a sample diagram of a custom mold, can be found in the injection mold machine's handbook.

{{< img "injection_mold_manual.jpg" "Injection mold machine handbook" >}}

A mold must be split into two halves, and every face in each half must slope inwards, away from the meeting point, otherwise one will not be able to smoothly remove the object from the mold. The sprue should enter at the midpoint of the two halves.

One must also include a small hole for air ventilation, 1/8" wide, .002mm deep. The injection mold machine comes with metal support cases, into which you can insert a custom mold.

{{< img "injection_mold_example.jpg" "sample injection mold" >}}

However, Connor thinks it may be possible to use a mold without these support cases, in which case we would have more freedom in the size and shape of our custom molds. However, this still needs to tested.

To create a plastic injection mold, one must use plastic resistant to high temperatures. KMG has one printer capable of printing high-temperature plastic: the Formlabs Form 2.

# Stereolithography (SLA) 3D Printing
The Form 2 is an SLA, or Stereolithography printer. A laser hardens photosensitive resin into plastic one layer at a time. The build platform is at the top of the machine, and lowers into a tank of resin which is then cured by a laser. Objects are thus printed from the top down, opposite to the bottom up process of FDM (fused deposition modeling) printer which extrudes molten plastic down onto a bed.

{{< img "form2.jpg" "Form 2" >}}

There are a few problems to keep in mind when it comes to SLA printing. One such problem is "cupping", which is caused by pressure imbalances in hollow chambers. Thus if your model has any hollow parts, one must create drain holes with a diameter of at least 3.5mm to prevent uncured resin from getting trapped inside the print. The drain holes should be tangent to cavities in the object.

Another problem is that too much surface area contacting the window will cause the print to be pulled off of the build platform. This, combined with the cupping problem, means that it is quite difficult to print an object flat on the bed.

A third problem is that printing an object at a straight angle can result in small slivers of plastic, which cannot be effectively held up, even with supports.

The safest way to get around the above problems is to print at an angle, using support pieces to hold the object together. Supports are a pain, as they must be cut off and sanded, but printing at an angle, smallest point touching the bed, is the most surefire method of printing without any problems.

# Printing with the Form 2
1. Change out the resin and the tank if necessary. There are different types of resin: clear, black, grey, high-temperature, and so on. In this case, we needed to switch to high-temperature resin.
  1. Always wear gloves when handling resin.
  2. Get the orange resin cap ready to close the bite valve (the hole where the resin comes out.)
  3. Pull out the resin container from the back of the machine and cap the hole.
  4. Unlock and remove the build platform. Clean with IPA if needed.
  5. Remove resin tank and place in box. Keep resin out of light as much as possible. Caution: If tank is cracked, it needs to be replaced to prevent a resin spill.
  6. Shake new resin cartridge well, remove the orange cap, and slide it in the back of the machine.
  7. Take the new resin tank out of the box. Note: always treat resin boxes like a hot pizza, holding them flat, so the resin does not spill out.
  8. Place the new tank in the machine and press in with your thumbs until it clicks.
  9. Open valve on top of the resin cartridge in the back.
  10. Agitate the resin in the tank with a clean pallet scraper, pulling it towards you and wiping with the wiper blade (remove the wiper blade from the lock to make this easier.)
  11. Close the amber cover. Now you are ready to print!
2. Open PreForm, choose options to match your resin. The computer should automatically detect the type of resin you inserted (make sure the tank and cartridge resin types match.) Also choose the layer height: a general rule is 50 microns (0.005mm).
3. In Fusion 360, export the model to STL with the Make option.
4. Import the STL into PreForm and place it at an angle if necessary (see above).
5. Automatically generate supports from the menu.
6. Automatically layout the parts.
7. Print!

Other Form 2 maintenance notes:

- Most parts can be cleaned with IPA, except orange polycarbonate (cover, resin tank) and Acrylic (resin tank window) which should be cleaned with Novus 1. Make sure to use a soft microfiber sheet to clean the glass, which is particularly delicate.
- If the amber cover cracks, it can be replaced for free by contacting Formlabs.

{{< img "rc_car.jpg" "RC Car" >}}
{{< img "rc_jump.jpg" "RC Car" >}}

After a hard day designing and printing an injection mold, Connor blew off some steam by jumping an RC Car.
