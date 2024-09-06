# TouchDesigner RealTime Warping

## Overview

The [Derivative TouchDesigner](https://derivative.ca/download) software does a great job of applying a pre-made STmap map warping template image in a way that works live and real-time. With a bit of effoert to learn the workflow, you can use Kartaverse, or [PTGui Pro](https://ptgui.com/) to make the initial STMap template, that you then run inside of TouchDesigner.

This is a great way to warp Canon R5C + RF 5.2mm dual fisheye imagery into a 180VR Side-by-Side layout. It does require you to have a custom STMap template image created beforehand (which the Kartaverse [kvrFisheyeStrereo](kvrFisheyeStereo) node can help with).

![TouchDesigner](Images/TouchDesigner_STmaps.png)

## TouchDesigner STMap Usage: 

1. Create a new TouchDesigner project. Set the End/Rend frame range to the duration of the video footage you want to export. Customize the FPS parameter to 60 fps.

2. Use a "[MovieFileIn](https://docs.derivative.ca/Movie_File_In_TOP)" node to load an STMap template image, This might be an asset named something like "Media/EOS_R5C_RF52_STMap.0001.exr".

3. Use a node to bring in the Canon R5C video footage. You can import a pre-existing movie file from disk using a "[MovieFileIn](https://docs.derivative.ca/Movie_File_In_TOP)" node or you can import a live video feed into TouchDesigner with the help of either an [NDI](https://docs.derivative.ca/NDI) video stream, or a [video capture card](https://docs.derivative.ca/Video_Device_In_TOP).

4. Add a "[Remap](https://docs.derivative.ca/Remap_TOP)" node. Connect the Canon R5C footage and the STMap footage to the input connection on the Remap node.

5. Add a [MovieFileOut](https://docs.derivative.ca/Movie_File_Out_TOP) node and connect it to the Remap node. This is how the finished footage is exported from TouchDesigner. 

Choose if you want to save out an image sequence or a movie file.

Then customize the File attribute to define the filename for rendered footage.

When you toggle on the "Record" button", the MovieFileOut footage will be written to disk. You can turn on the "Pause" button if you want to pause the export process.

It is a good idea to turn off the "[x] Realtime" checkbox at the top toolbar area in TouchDesigner if you are offline rendering a Movie file to disk and don't want to have any skipped frames.

6. TouchDesigner allows you to send your final processed 180VR footage out to an HMD in realtime, or to an HMDI video output connection, or to a realtime internet video streaming platform with the "[videostreamout](https://docs.derivative.ca/Video_Stream_Out_TOP)" node.

## Extra Learning Resources

**kvrFisheyeStereo**  
Check out the Kartaverse [kvrFisheyeStereo](kvrFisheyeStereo) node that works in Resolve/Fusion.

---

**STMap Guide**  
For more information about ST Maps check out the article:  
[Google Docs | KartaVR Workflows | Creating ST Maps](https://docs.google.com/document/d/1lQ-wc9ucLJqj-HL7iKMNWA71klV5O1fk2-JicRB6gDY/edit?usp=sharing)

---
**Hugh Hou YouTube Video**  
This Hugh Hou video shows how to process Canon R5C camera + Canon RF 5.2mm dual fisheye lens media in Resolve:
[Edit Canon R5C & R5 VR180 w/ DaVinci Resolve 18 FREE - 3D 8K 60fps RAW LT Clog3 Workflow](https://www.youtube.com/watch?v=2GW7nb47rB4)

The tutorial covers the usage of "ST Maps" and the WarpStitch node. Included with the project files are Fusion and Resolve example comps, along with a TouchDesigner based real-time warping project file that can be used to do live 180VR video streaming, and supports real-time stitched previews from the Canon R5/R5C camera. Make sure to [download the supporting project files](https://drive.google.com/file/d/1H-owMeadqekZ42BgmqeaPHr9Ry2cHFP8/view).

@yt(2GW7nb47rB4,560px,317px,center)


