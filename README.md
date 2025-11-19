# Alpenmeister S v2 Controller
also known as Meisterbox S

![A closed leverless controller with a shell printed in black. The controller has a lid with a embossed logo. The shell has two clasps for closing. The controller itself has 14 black or white buttons with low profile keycaps.](https://github.com/AlpenmeisterCustoms/AlpenmeisterS-v2/blob/main/pictures/meisterboxSv2_closed_front.png "Overview of the Alpenmeister S v2 Controller")
![A open leverless controller with a shell printed in black. The controller has a lid with a embossed logo. The shell has two clasps for closing. The controller itself has 14 black or white buttons with low profile keycaps.](https://github.com/AlpenmeisterCustoms/AlpenmeisterS-v2/blob/main/pictures/meisterboxSv2_open_front.png "Overview of the Alpenmeister S v2 Controller")

Alpenmeister S v2 Controller is licensed under [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/)  
Free to build and modify for personal use. If you want to sell this design, please contact me.

The goal here was to build a controller that is pocket sized, great for travelling (to locals) and that is, unlike most "box-controllers", an actual box. You can just wrap your USB cable around it and put it in your pocket, because it's barely larger than a large smartphone and weighs just below 200g.

It comes with an acrylic cover so you can put in your favorite artwork. It has a hidden compartment for a small passthrough authenticator dongle and also a second USB-C passthrough port for bigger converters like the Brook FGC. Switches are Kailh choc v2. Button caps are 1U and 1.5U. The layout is the Meisterlayout with two thumb buttons, two pinky buttons and a center button. It's designed as ergonomic as possible and sized down to the smallest footprint possible.

P.S. Why "Knochen"? Knochen means bone in German and the initial idea was to wrap the USB cable vertically, which would make it sort of shaped like a stylized dog bone.  
P.S.S. Shoutout to [Merlin](https://github.com/MerlinDesigns) for designing the v1 model case and always helping.

## Case Files

The repository contains five STLs in the `stls_to_print` folder which you'll need to print to make the Meisterbox S:

* 1x `knochenv2-bottom.stl`: the bottom of the shell
* 1x `knochenv2-top.stl`: the top of the shell
* 2x `knochenv2-pin.stl`: the pin used for the locking mechanism
* 2x `knochenv2-hinge.stl`: the rearhinges
* 2x `knochenv2-clasp.stl`: the clasp to securely close the box

You might need to orient the items on your print bed. You should be even able to print this on the print bed of a small 180mmx180mmx180mm printer. This build has been tested in PLA and PETG. Our recommendation is using PETG if you can, since that would make sure your controller won't warp when exposed to heat or become brittle because of sun exposure. If you use this controller to travel, those might be some conditions it might get exposed to.

You will also find files for the acrylic cover `optional/AlpenmeisterSv2-acrylic.step` and a cutout file for the optional artwork `optional/AlpenmeisterSv2-acrylic.dxf`.

## PCB Files

You can find the files necessary to order the PCB in `pcb/`. Ordering the PCBs will need some caution. If you want to order the boards please closely follow the instructions.

### How to Order the PCBs
1. Go to JLCPCB.com
2. Click on "Order now"
3. Click on "Add gerber file" and choose "MeisterboxS_gerber.zip"
4. Use the default options (see reference at the end of these instructions), except those mentioned here:
    - PCB Color: choose your color, we would recommend black
    - Surface Finish: HASL, we would recommend LeadFree
    - Confirm Production file: Yes
5. Use the switch next to "PCB Assembly"  
6. Use the default options for PCB Assembly, except those mentioned here:  

    - **Confirm Parts Placement: Yes  
       THIS IS IMPORTANT, JLCPCB will make a production file to match the files we provide, please check if all components are where they should be**
    - PCBA Qty: Choose the same amount as PCB Qty
    - Advanced Options: don't touch and leave as defaults

7. Click "Next"
8. Click "Next"
9. Click "Add BOM" File and choose "AlpenmeisterSv2_bom.csv", then click "Add CPL File" and choose "AlpenmeisterSv2_CPL.csv". Then click "Process BOM & CPL"
10. You will then be presented with the components that are used on the board, they should be in stock and selected. Only then click "Next". Do not proceed if some are missing and you don't know what they do.
11. You might then see a prompt saying "The system detects components that may be offset from the PCB, does it try to automatically align it?" (sic). Click "Cancel".
13. You'll be in your cart. Select the PCB we just configured and then go through the "Secure Checkout"

Please bear in mind: Do this at your own risk. It is your own responsibility to do the ordering process. We are not responsible for any mistakes in this instruction, as the actual ordering process might change at any time.
<details><summary>Click to see default options for reference</summary>

    PCB: 
    - Base Material: FR-4
    - Layers: 2
    - Dimensions: do not touch
    - PCB Qty: 5 is minimum
    - Product Type: Industrial/Consumer electronics
    - Different Design: 1
    - Delivery Format: Single PCB
    - PCB Thickness: 1.6mm
    - Silkscreen: White
    - Outer Copper Weight: 1oz
    - Via Covering: Tented
    - Min via hole size/diameter 0.3mm
    - Board Outline Tolerance: +/-0.2mm
    - Mark on PCB: Remove Mark
    - Electrical Test: Flying Probe Fully Test
    - Gold Fingers. No
    - Castellated Holes: No
    - Edge Plating: No
    PCB Assembly:
    - PCBA Type: Economic
    - Assembly Side: Top Side
    - Tooling holes: Added by JLCPCB
    - Parts Selection: By Customer
</details>


## Additional Hardware

You'll need some other hardware to assemble the whole controller:
* 14x Choc V2 switches
* 14x Choc hotswap sockets
* 9x 1U Tai-Hao THT Low Profile MX Blank Keycaps (you could print these if you'd like)
* 5x 1.5U Tai-Hao THT Low Profile MX Blank Keycaps (you could print these if you'd like)
* 4x 6mm M3 heat inserts 
* 4x 6mm M3 flat top screws
* 1x 2mm acrylic top plate
* 1x USB-C cable (you will need a right-angled one with a slim connector to make it fit)

## Assembly

1. Flash firmware onto board. Follow [these instructions](https://gp2040-ce.info/installation/). Use [this firmware](https://github.com/AlpenmeisterCustoms/GP2040-CE/actions/runs/19237635402/artifacts/4521340374).
2. Solder hotswap sockets to board.
3. Insert heat inserts into case.
4. Put 1.5mm filament through case and hinges + clasps, cut off excess filament. Put in the pins.
5. Put PCB into bottom case part.
6. Put acrylic plate on top of it.
7. Screw it together.
8. Insert switches and keycaps.
9. Enjoy.

## More licensing

Alpenmeister S v2 Controller is licensed under [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/)  
Free to build and modify for personal use. If you want to sell this design, please contact me.  
Alpenmeister S v2 Controller "case" (the STL files) is licensed under [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/)    
It is based on "[Parametric Box v2 (single clasp)](https://www.printables.com/model/540605-parametric-box-v2-single-clasp)" and was modified accordingly.


## Contact

You can find me (@alpen.meister) on the [Open Stick Community Discord](https://discord.gg/JqK6K5tu).
Or on [Alpenmeister.com](https://alpenmeister.com/en/)
