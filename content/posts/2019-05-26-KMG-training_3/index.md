---
layout: blog
draft: true
title: "KMG Second Weekend: CNC milling a custom coaster"
date: 2019-05-26T18:24:37+09:00
categories: journal
tags:
  - KMG
  - CNC
  - design
  - Fusion 360
  - Nomad
---

In order to practice both design and CNC, Connor assisted me in the design of a custom Agargara coaster.

#TODO {{< img >}}

My image for the coaster was an ashtray shape: a round base with a raised lip, and a logo engraved in the middle. Simple enough to design in a couple hours, and CNC'ing would involve using a few different tools.

Connor guided me through the steps of designing the object. First, we measured the dimensions of the material, and planned the dimensions of the coaster on paper. Then in Fusion 360, we drew a few concentric circles, extruded them out, and subtracted the middle cylinder to create a raised lip.

Connor suggested **drafting** the outer edges, which means extending them in a slope. We also put fillets, curved slopes, in the inside ring, each the size of the tool radius, to create a smooth curve over the lip and down to the bottom.

Designing the object was fairly quick. Then came the tedious part: programming the tool paths.

## Tool paths
We programmed the tool paths in the following order:

1. 3D adaptive: 1/8" square mill to quickly remove the large areas on the inside and outside. We set the optimal load to tool diameter * .25, the max roughing step down to diameter * .5, and made sure to check "machine shallow areas" to ensure the tool reached the bottom.

My one important take away from the project was: always check the simulation closely! There are often small details and mistakes that you might not realize at first glance.
