
# kvrCreateStereo

The Kartaverse "kvrCreateStereo" fuse allows you to reformat stereo 3D imagery between mono, dual input, horizontal (SBS), and vertical (OU) frame layouts.

The kvrCreateStereo node works in Resolve (Free), Resolve Studio, and Fusion Studio. It is able to act as a direct replacement for the Resolve Studio requiring "Splitter" and "Combiner" stereo 3D nodes.

When converting between stereo 3d layouts, the term "Dual In" is used in the Inspector panel to represent the "Dual Input" connection mode where you have an Image1 and Image2 set of inputs that feed separate left and right eye view media into the kvrCreateStereo node.

It is helpful to get in the habit of adding an Autodomain node directly after a kvrCreateStereo node. This will optimize the Fusion DoD (Domain of Definition) active content frame sizing information which is useful for optimizing rendering efficiency.

![kvrCreateStereo Fuse](Images/fuse-kvrCreateStereo.png)

# kvrCubic

The "kvrCubic" fuse allows you to combine individual face based 90° FOV cubic imagery into CubeMap, 180VR, and 360VR based frame layouts. It supports monoscopic and stereo 3D output.

![kvrCubic Fuse](Images/fuse-kvrCubic.png)

The kvrCubic node now supports full cross-platform usage with Metal/OpenCL/CUDA GPU compatibility.

# kvrPlane

The Kartaverse "kvrPlane" fuse allows you to place a flat image into a 180VR, or 360VR image projection. It supports monoscopic and stereo 3D output.

![kvrPlane Fuse](Images/fuse-kvrPlane.png)

This node performs a "plane to sphere" style of conversion. The kvrPlane node now supports full cross-platform usage with Metal/OpenCL/CUDA GPU compatibility.

The node based layout is typically:

    Text+/Loader/MediaIn -> kvrPlane -> AutoDomain -> kvrViewer

There are onscreen control handles in the viewer window which make it quick to position content visually using a "Center" X/Y point control to apply yaw/pitch rotation to the imagery when it is projected into the spherical image projection.

If you are working with non 1:1 aspect ratio source imagery, the "Resolution Gate Fit" control allows you to fit the imagery using either a "Stretch", "Width", or "Height" option. This is great if you want to place a small logo or other custom graphic element and not have to worry about the source image's dimensions and aspect ratio.

## kvrPlane Image Resolution

The kvrPlane node works with the idea that the plane image data is texture mapped to the "front" face of an imaginary cubemap surface. This means the plane at full width takes up a 90° FOV area.

When the auto-resolution mode is used, the kvrPlane node takes the current image input resolution as the size of a 90° cubic face. So a 180° monoscopic output would be processed as two times the image input resolution, and a 180° SBS stereo output would be processed as four times the image input resolution. Also, a 360° monoscopic output would be processed as four times the image input resolution, and a 360° Over/Under stereo output would be processed as four times the image input resolution.

# kvrCropStereo

The kvrCropStereo fuse allows you to re-crop stereo 3D footage with individual control over the left and right eye content.

![kvrCropStereo Fuse](Images/fuse-kvrCropStereo.png)

This stereo 3D aware cropping process makes it easy to pre-process production footage before applying image projection conversions.

![kvrCropStereo Image View](Images/fuse-kvrCropStereo-viewer.png)

The fastest way to get the initial positioning updated for the kvrCropStereo crop regions is to choose the stereo 3D setting you want like mono, or stereo 3D horizontal/vertical. Then click the "Reset" button to auto-fit the left/right eye view crop regions to the image canvas dimensions.

If you want to get the initial sizing updated

# kvrLens

Apply lens distortion correction using brown-conrady, syntheyes, and panotools lens models.

![kvrLens Fuse](Images/fuse-kvrLens.png)

Lens distortion correction can be used to correct for optical issues like barrel or pincushion effects:

![kvrLens Viewer 1](Images/fuse-kvrLens-viewer-1.png)

![kvrLens Viewer 2](Images/fuse-kvrLens-viewer-2.png)

![kvrLens Viewer 3](Images/fuse-kvrLens-viewer-3.png)

# kvrLensStereo

Apply lens distortion correction to stereo 3D footage using Brown-Conrady, Syntheyes, and Panotools lens models.

![kvrLensStereo Fuse](Images/fuse-kvrLensStereo.png)

# kvrSTMapGenerator

The "kvrSTMapGenerator" fuse allows you to generate an initial STMap template.

![kvrSTMapGenerator Fuse](Images/fuse-kvrSTMapGenerator.png)

The "Auto Resolution" checkbox will use the connected source footage resolution for the width and height of the STmap gradient pattern. 

If you disable the "Auto Resolution" checkbox, you can manually define a resolution override to allow you to increase the STMap width and height to a different (usually larger) size than the source imagery. This is a useful control to have access to if you are going to apply a post-cropping effect to the STMap, further down in the comp, with a node like kvrCropStereo and want the final STmap frame size to be a certain size.

For more information about STMap warping workflows check out the document:
[Google Docs | KartaVR Workflows | Creating ST Maps](https://docs.google.com/document/d/1lQ-wc9ucLJqj-HL7iKMNWA71klV5O1fk2-JicRB6gDY/edit?usp=sharing)

An STMap gradient image is able to hold pre-computed warping data in an image's red and green channels. You need to save an STMap in a 16-bit or 32-bit per-channel image with lossless compression to avoid artifacts. ZIP or ZIPS (ZIP Scanline) is a good choice for an EXR image codec for storing STMaps.

![kvrSTMapGenerator Fuse](Images/fuse-kvrSTMapGenerator-viewer.png)

Bonus DCTLs: Resolve Edit and Color page compatible DCTL files are included in the folder:

        Reactor:/Deploy/Bin/Kartaverse/LUT/

# kvrGrade

The kvrGrade fuse allows you to quickly color correct stereo 3D footage with individual control over the left and right eye content.

![kvrGrade Fuse](Images/fuse-kvrGrade.png)

# kvrVignette

The kvrVignette node allows you to quickly and easily generate a 180VR stereo 3D compatible dual fisheye lens masking pattern.

A radial vignetting effect can be used with a "multiply" transfer mode to fade out the perimeter edge-zone area of an 180VR dual fisheye video clip. This technique masks the edges of the left and right eye views so you can guide the viewer's attention to where it matters most. Most importantly, using a vignetting process on your 180VR immersive media is an affordable way to hide the lens element that is visible in the opposite eye view of a dual fisheye lens based camera rig.

![kvrVignette Fuse](Images/kvrVignette_output.png)

## Vignette Edit page usage

A new Resolve Edit page "Generator" macro version of the kvrVignette tool is available. Select Edit page the Effects tab's "Toolbox &gt; Generators &gt; KartaVP &gt; Color &gt; kvrVignette" entry and drag it to a video track above your 180VR video content.

![kvrVignette Generator 2](Images/kvrVignette_generator_2.png)

Once the generator has been added to the video track, change the clip's Inspector panel based "Settings &gt; Composite &gt; Composite Mode" control to "Multiply" so the vignetting effect darkens the 180VR dual fisheye video clip content.

![kvrVignette Generator 2](Images/kvrVignette_generator_2.png)

## Vignette Fusion page usage

In the Fusion page create the following node layout:

![kvrVignette Nodes](Images/kvrVignette_nodes.png)

This node graph setup allows the "kvrVignette" to create the radial lens masking pattern, and the Merge node controls the final blending and layer transfer mode properties:

	MediaIn1 > kvrVignette1 > Merge1.Foreground
	MediaIn1 > Merge1.Background
	Merge1 > MediaOut1

For a Canon R5C Dual Fisheye Stereo Lens setup, you would likely want to use the following Inspector window based "kvrVignette" and "Merge" node settings:

![Edit Page Timeline](Images/kvrVignette_adustment_layer_controls_1.png)

## kvrVignette Attributes

- Projection:
	- Diagonal Field of View: 180
- Stereo:
	- Mode: Horiz
	- [x] Solid Alpha
- Image:
	- [x] Auto Resolution
- Masking:
	- Mask Diameter: 0.82
	- Mask Softness: 0.7

Merge

- Apply Mode:
	- Multiply

![Edit Page Timeline](Images/kvrVignette_adustment_layer_controls_2.png)

# kvrViewer

Preview fisheye, 180VR, 360VR, and flat media in 2D mono, or stereo 3D. The node can be used to reframe VR footage with onscreen controls.

You can also convert stereo 3D circular fisheye content into 360VR and 180VR output. This is great if you want a parametric way to process media from lenses like the Canon RF 5.2mm dual fisheye lens.

![kvrViewer Fuse](Images/fuse-kvrViewer.png)


The kvrViewer node can display 360VR content where it acts like a panoramic media viewer. The onscreen control handles allow you to quickly navigate around in the scene and zoom in/out.

![kvrViewer Viewer 2](Images/fuse-kvrViewer-viewer-2.png)

The kvrViewer node can be used to generate "Tiny Planet" views of a scene.

![kvrViewer Viewer 2](Images/fuse-kvrViewer-viewer-3.jpg)

The kvrViewer node can display dual fisheye SBS content where it generates 180VR (180&deg;x180&deg;) stereo 3D output:

![kvrViewer Viewer 1](Images/fuse-kvrViewer-viewer-1.png)

# kvrReframe360Ultra

The kvrReframe360Ultra node allows you to perform an "overcapture" effect that reframes immersive 360VR footage into "flat" media that can be played back on conventional displays. This node is also available as an Edit page Effects Template.

![kvrReframe360Ultra Fuse](Images/fuse-kvrReframe360Ultra.png)

The kvrReframe360Ultra node can be used to generate "Tiny Planet" views of a scene.

![kvrReframe360Ultra Viewer](Images/fuse-kvrReframe360Ultra-viewer.jpg)

# kvrWarpStitchUltra

The kvrWarpStitchUltra node is used to stitch circular fisheye images into a latlong image projection. The node has parametric controls for adjusting the FOV, pan/tilt/roll, frame cropping, integrated masking, and colour correction.

![kvrWarpStitchUltra Fuse](Images/fuse-kvrWarpStitchUltra-1.png)

![kvrWarpStitchUltra Fuse](Images/fuse-kvrWarpStitchUltra-2.png)

![kvrWarpStitchUltra Fuse](Images/fuse-kvrWarpStitchUltra-3.png)

![kvrWarpStitchUltra Fuse](Images/fuse-kvrWarpStitchUltra-4.png)

The example composite "Under The Bridge" shows how multi-view 360VR video stitching can be achieved with the help of the kvrWarpStitchUltra node:

![kvrWarpStitchUltra Under the Brdidge Example](Images/fuse-kvrWarpStitchUltra-under-the-bridge.jpg)

## WarpStitch Tips

When the Fusion viewer window is active and has the foreground user input focus, you can tap the TAB button on your keyboard to quickly cycle through the different overlay controls. This lets you switch between adjusting the Optical Frame Center, circular mask diameter, and the rectangular cropping values.

If you copy one WarpStitch node, then use the Paste Instance option, you can then keep most of the controls linked across each of the panoramic views you are warping. Then you can use the Inspector view's "right-click > Deinstance" contextual menu item to individually unlink attributes you want to make unique per-view such as the "Optical Frame Center", and "Rotate Sphere > Pan" controls for the copied nodes. This is handy if you want to be able to eye-ball in values like the Mask Softness or Diagonal Field of View values across several fisheye images at the same time to refine your stitch.

## Introduction to WarpStitch

1. Use a Loader or MediaIn node in Fusion to import footage that was filmed with a circular fisheye lens. Select this node.

2. With the Nodes view active, press the "Shift + Space" hotkey to display the Select Tool dialog. Type in "WarpStitch" and then press the "Add" button to insert a new KartaVR WarpStitch node into your composite. WarpStitch should now be connected to your Loader or MediaIn node.

3. It is a good idea to insert an "AutoDomain" node into the composite right after a WarpStitch node, so Fusion will effortlessly handle the frame size and aspect ratio changes performed by WarpStitch. An AutoDomain node can be added using the "Shift + Space" hotkey to display the Select Tool dialog. Type in "AutoDomain" and then press the "Add" button.

4. Select the WarpStitch node in your comp. In the Inspector window there is a "View Mode" ComboMenu control, which is at the top of the list of controls for the node. The "View Mode" ComboMenu lets you switch between seeing the "Final Result", the "Original Image", or a variety of diagnostic modes like "Initial Crop", "Rotated Image", "Vector Mask", "Masked Image", "Warped Image", and "Color Corrected Image" which are useful for inspecting the intermediate stages of internal data processing performed by the WarpStitch node.

	There are four tabs present labeled "Lens", "Color", "Image", and "Settings".

	The "Lens" tab provides the controls needed to adjust the warping process including:
	- Defining the lens center with the "Optical Frame Center" control
	- Modifying the original image's rotation is possible with the "Image Orientation >  Angle" control. It allows you to choose between 0, 90, 180, and 270 degree rotations.
	- Applying vector masking to your imagery is done with the "Circular Fisheye Masking" / "Rectangular Masking" / "Split View Masking" controls
	- Adjusting the FOV for the circular fisheye lens is done with the "Diagonal Field of View" control. A typical circular fisheye lens might have a 180 degree FOV.
	- Rotation of the spherical image projection output is done via the Rotate Sphere controls which provide access to rotating the warped image via a set of "Tilt", "Pan" and "Roll" controls. If you wanted to rotate a panoramic image horizontally by 180 degrees you would set the Pan control to 180.

	The "Color" tab provides the controls needed to perform basic per-camera view color corrections to help your footage better match up when blended. The Exposure, Gamma, Levels, and Output Levels controls allow you to adjust the overall brightness and contrast in the image along with the shadows and highlights. The Saturation and Vibrance controls allow you to make the colors "pop" and appear more vivid. The White Balance section provides Color Temperature and Tint controls which allow you to compensate for per-camera differences in the color of the lighting.

	The "Image" tab allows you to adjust the image aspect ratio settings for the final warped image. Additionally, the "Output ST Map" checkbox tells the WarpStitch node to output a "UV Pass" warping template image called an "ST Map" which can be used to store a pre-computed image projection transform into an image's red and green color channels. The "Edge Settings > Edge" control can help fix seam artifacts.

	The "Settings" tab allows you to assign your own intool scripting based "Frame Render Scripts", along with providing access to a pair of Edit Code buttons labeled "Edit Fuse" and "Reload Fuse" that can be used to manually tweak the default range of WarpStitch's user interface controls or to adjust any other aspect of the fuse's code.

5. Switch back to the "Lens" tab.

	Adjust the "Initial Crop > Optical Frame Center" control to place the onscreen "X" shaped onscreen viewer control in the center of the circular fisheye image. If you click in the Fusion viewer window so it has the user input focus, you can tap the TAB key several times to quickly toggle the active onscreen control widget so the "X" shaped onscreen viewer control is highlighted in red and can be dragged around visually with your cursor.

	Note: If you are working with footage from a 1-piece panoramic camera that places both the front and back fisheye images inside the same image frame in a "SBS" side by side layout, you can typically start out by changing the "Optical Frame Center" value from "0.5" over to either "0.25" or "0.75" as an initial starting point before you would then refine the value further.

	Change the "View Mode" to "Initial Crop".

	The "Initial Crop > Frame Border Padding" slider can be used to help "uncrop" a circular fisheye image that has been captured on a 16:9 video sensor that would cut off part of the circular fisheye image frame area.

	If your camera body was rotated when mounted on the panoramic camera rig, you can adjust the "Image Orientation > Angle" setting to correct for this view rotation. The "View Mode" control labeled "Rotated Image" lets you verify the image orientation adjustment is set as you'd expect so you can be sure you have the correct "upright" axis defined for the image before it is warped into a spherical image projection.

6. Change the "View Mode" to "Masked Image" to see the circular masking applied to the imagery. To adjust the circular fisheye masking setting, you can use the Inspector and drag the slider for the "Vector Masking > Circular Fisheye Masking > Mask Diameter" control to line up with the border of your fisheye lens image data, or the circular shaped onscreen control handle can be used to resize the mask visually.

	The "Vector Masking > Circular Fisheye Masking > Mask Softness" slider allows you to adjust how hard or soft you want the mask edge to appear. Additionally, you could set the "View Mode" to "Vector Mask" to see just the black/white masking output if you want to see the precise size of the mask used and its overall softness.

7. The "Warped Image > Diagonal Field of View" control can be adjusted to change the FOV of the circular fisheye image. Typical wide angle fisheye lenses are somewhere in the range of 180 - 220 degree FOV. You need to change the "View Mode" control to "Warped Image" or "Final Result" to see the effects of the FOV modifications. The Rotate Sphere controls for Tilt, Pan, and Roll are used to adjust the placement of the fisheye image inside the final spherical image projection.

8. Switch to the Color tab. This tab allows you to perform "Quick 'n Dirty" modifications to each of the camera views you are processing. This is a time saver if you need to apply small color tweaks. The "View Mode" control has a "Color Corrected Image" option that allows you to see the result of these changes. If you need to perform more complex color corrections you could always add a separate ColorCorrector node to the comp per-camera view.

	Change the "View Mode" over to "Final Result" to see the effects of all the settings applied at once. This "Final Result" option is the setting WarpStitch should be left at when you are done with all your adjustments and want to look at the footage downstream in your composite.

9. Repeat the main steps shown in sections 1-8 to set up each of the per-camera views you want to warp into a spherical image projection. For speed of adjustment consider using the copy/paste instance approach along side the Deinstance controls tip to rapidly deploy many near identical camera views.

10. Connect each of the WarpStitch per-camera view processed composite branches together using either a series of Merge nodes chained together, or with a kvrMergeLayers node that supports blending multiple image input connections that are fed into the same node simultaneously.

# Macro

## kvrDualFisheye

The kvrDualFisheye macro allows you to stitch 360VR content from dual fisheye footage that was captured on front/back lens based cameras.

Internally the macro uses KartaVR fuses to power the stitching process.

![kvrDualFisheye Fuse](Images/fuse-kvrDualFisheye-1.png)

## Effects Template Usage

In the Resolve Edit page, the "kvrDualFisheye" macro can then be dragged from the Effects Library "Effects > KartaVP > Warp" category onto a clip in the timeline. Select the clip and then open the Inspector view to adjust the parameters using the "Effects > Fusion > kvrDualFisheye" item.

In the inspector view, if you click the little magic wand icon next to the right of the heading "kvrDualFisheye" you can hop into the Fusion page to customize the macro node. Double clicking on the "kvrDualFisheye" node in the Fusion page allows you to expand the group to access the nodes that are stored inside the group object.

![kvrDualFisheye Edit page](Images/fuse-kvrDualFisheye-2.jpg)

# VR Subtitles

## vTextFromSubtitles

Vonk Ultra includes a node that allows you to read timecode synced closed caption subtitle .srt data. The output is a text datatype that can be connected to the StyledText field on a Text+ node.

![vTextFromSubtitle Fuse](Images/fuse-vTextFromSubtitles.png)

The Vonk Ultra example "Demo Subtitle.comp" shows the node graph layout required for loading subtitles into Fusion:

![vTextFromSubtitle Viewer](Images/fuse-vTextFromSubtitles-viewer-1.png)

Typical Node Connections:

        vTextFromFile > vTextFromSubtitle > Text+

The vTextFromSubtitles node supports both "flat" and immersive 360VR text caption creation through the use of an image projection conversion node like Kartaverse's "kvrPlane" fuse.

