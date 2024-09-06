# kvrSuperSTMap Effects Template

## Overview

The "kvrSuperSTMap" Effects Template is the next-generation update for the STMapperInline Effects Template in Resolve/Fusion.

![Controls.](Images/kvrSuperSTMap_Controls.png)

## Open Source Software License

- LGPL 3.0

## Software Required

- Resolve Studio or Fusion Studio v17-19+ 
- Reactor Package Manager + Kartaverse
- Reactor Atom Packages Used:
	- STMapper
	- KartaVR LensProfiles

## Edit Page Usage

The "kvrSuperSTMap" Effects Template can be used on a Resolve Edit page timeline to transform VR imagery between different image projections with the addition of an STMap warping template image. 

kvrSuperSTMap allows video editing timelines to apply image projection transforms at the clip level, or on an adjustment effect layer. This is perfect for SBS 180VR workflows involving camera original dual fisheye imagery.

![Effects](Images/kvrSuperSTMap_Effects_Tab.png)

Add the "kvrSuperSTMap" effects template to a Resolve Edit page timeline clip. 

In the Inspector page, you can then link in STMap warping template using the "ST Map Filename" filed. 

The stereo convergence properties can be refined with the X/Y Shift controls. This results in the left and right eye SBS views having the optical frame center adjusted as a pre-processing stage before the STMap warping stage happens. This allows for compensations of the floating optics that exist in a Canon EOS dual fisheye lens.

![Timeline](Images/kvrSuperSTMap_Timeline.png)

If your timeline resolution and aspect ratio don't match the native footage resolution, you will need to use the Inspector window's "Retime and Scaling > Scaling > Stretch" control. This will corect for aspect ratio differences and avoid black bars being added to the clip border:

![Fit](Images/kvrSuperSTMap_Resize.png)

## Fusion Page Usage

The "kvrSuperSTMap" macro node is also available in the Fusion page, too. This is great for more complex VFX + VR workflows.

![Node Logic](Images/kvrSuperSTMap-Comp.png)

## Node Logic

If you double-click on the kvrSuperSTMap node in the Fusion page nodes view you can see the internal wiring logic of the node.

![Node Logic](Images/kvrSuperSTMap_GroupOperator.png)
