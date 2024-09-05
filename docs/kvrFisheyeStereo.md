# kvrFisheyeStereo Effects Template

## Overview

The "kvrFisheyeStereo" Effects Template and example lens profile composites process footage from SBS 180VR cameras that use a dual circular fisheye lens layout. This includes Canon EOS VR gear.

## Open Source Software License

- LGPL 3.0

## Software Required

- Resolve Studio or Fusion Studio v17-19+ 
- Reactor Package Manager + Kartaverse
- Reactor Atom Packages Used:
	- STMapper
	- Vonk Ultra
	- KartaVR DragDrop
	- KartaVP
		- kvrFisheyeStereo
		- kvrCreateStereo
		- kvrCropStereo
		- kvrGrade
		- kvrLens
		- kvrViewer

**Note: The kvrFisheyeStereo effects template makes use of the "Global Align" and "Anaglyph" nodes that are not available in Resolve Free.**

### kvrFisheyeStereo View Mode Control

The "kvrFisheyeStereo" node has a "View Mode" control that allows you to inspect the internal processing stages used. If you want to export an STMap warping template set the "View Mode" control to "STMap". Then you can either use a Saver node set to export an .exr image to disk. 

Or you could right-click in the Viewer window, if you have the STMap displayed, and then choose the "Save Image..." option to write an .exr image to disk directly.


![View Mode](Images/kvrFisheyeStereo_View_Mode.png)

Otherwise, you will typically use a combination of the "RGB" output mode if you want to directly inspect the final RGB color version of the 180VR output, along with the "Global Align" mode to perform vertical and horizontal disparity corrections using the "GlobalAlign X Shift" and "GlobalAlign Y Shift" controls in the Inspector panel.

### JSON Data Exchange

When you select the kvrFisheyeStereo node, you now have access to "Import JSON" and "Export JSON" buttons in the Inspector panel. These controls allow you to quickly and easily work with the JSON lens calibration data files.

To kick things off, there are initial Canon R5C, R7, R6 presets along with RED V-Raptor 8K presets. More presets will be added in time. The bundled "Lens Profile" example Fusion .comp files are updated as well.

![JSON Example](Images/kvrFisheyeStereo_JSON_Example.png)

### STMap Usage

The STMaps you create with the kvrFisheyeStereo node are designed to be used on the Resolve Edit page with the help of the kvrSuperSTMap effects template. You can also take the STMap warping template .exr image file and use it with real-time live-streaming programs like [Assimilate LiveFX](https://www.assimilateinc.com/products/livefx/), or [Derivative TouchDesigner](https://derivative.ca/download) if you want to have on-set previews during a 180VR film production.

## Usage

**Step 1.** Install Reactor and add the "kvrFisheyeStereo" package to your Resolve based system.

![Reactor](Images/kvrFisheyeStereo_Reactor_Package.png)

**Step 2.** Open a Resolve video editing timeline in the Edit page.

**Step 3.** Display the Effects Library tab, and switch to the "Toolbox > Effects > KartaVP > Warp" section. Drag the "kvrFisheyeStereo" entry onto a video clip in the timeline.

![Effects Tab](Images/kvrFisheyeStereo_Effects_Tab.png)

**Step 4.** Click on the video clip in the timeline and switch to the Inspector's Effects tab. Modify the "Effects > Fusion > kvrFisheyeStereo" settings if the default value doesn't give you the output you desire.

![Timeline](Images/kvrFisheyeStereo_Timeline.png)

**Step 5.** 
If you modify the "kvrFisheyeStereo" Effects Template's "View Mode" control you can preview the different output modes.

The viewer window in the Edit page should update to show the result. If the view doesn't update instantly, you can try bumping the timeline playhead position forwards/backwards by one frame to force a refresh of the view.

In the inspector view, if you click the little magic wand icon next to the right of the heading "kvrFisheyeStereo" you can hop into the Fusion page to customize the macro node.

![Magic Wand](Images/kvrFisheyeStereo_Magic_Wand.png)

If you display the kvrFisheyeStereo node in the Fusion Viewer window you will be able to see the effect's output. 

![Nodes](Images/kvrFisheyeStereo_Node_Graph.png)

To save an STMap warping template image to disk, set the kvrFisheyeStereo node's "View Mode" control in the Inspector panel to "STMap".

![View Mode STMap](Images/kvrFisheyeStereo_STMap_Output.png)

Then right click on in the Fusion viewer window and select the "Save image..." contextual menu item. Give the new image a name and make sure to save it with the ".exr" image extension at the end of the filename.

![Save image](Images/kvrFisheyeStereo_Save_Image.png)

### Lens Profiles Presets Folder

If you have the "KartaVR Scripts | Open Folder" Reactor atom package installed, as well, there is a handy "Script > KartaVR > Open Folder > Open Kartaverse Lens Profiles Folder" menu item in Fusion.


![Open Folder Menu Item](Images/kvrFisheyeStereo_KartaVR_Open_Folder_Menu_Item.png)

This menu entry makes it possible to quickly hop into the folder were all the .json files live so you can access your presets:

		Reactor:Deploy/Scripts/Support/Kartaverse/LensProfiles/

![JSON Lens Profiles](Images/kvrFisheyeStereo_JSON_Lens_Profiles.png)

The kvrFisheyeStereo node is designed to process dual fisheye content into a 180VR SBS (180x180° cropped format). You can now start the lens calibration process from an initial .json preset file to streamline the tuning steps when you have a new camera body and lens.

When the kvrFisheyeStereo node is shown in the Inspector window, there are fields at the bottom of the view that list the "Camera", "Lens", as well as the "Lens Profile Version" number details. Use these attributes to label the camera body and dual fisheye lens that is in use. This step makes it easier to know what exact preset is loaded.

![Lens Profiles2](Images/kvrFisheyeStereo_JSON_Lens_Profile_Presets2.png)

If you click the kvrFisheyeStereo node's "Export JSON" button, the camera and lens information is written out to the JSON lens profile document. If you want to bring in an external lens profile preset simply click the "Import JSON' button.

![Lens Profiles 1](Images/kvrFisheyeStereo_JSON_Lens_Profile_Presets1.png)

### About the Lens Profile Comps

The Kartaverse Lens Profile atom package ships with a collection of comps examples. They show the basics of how the kvrFisheyeStereo macro works as a 180VR dual fisheye stereo conversion toolset. Each of the provided Fusion .comp files are tuned for a specific camera body like the RED V-Raptor 8K, Canon R5C, R7, and R6.

![Lens_Profiles](Images/kvrFisheyeStereo_Lens_Profiles_Folder.png)

The lens profiles example comps are located on disk at the following Pathmap location:

		Reactor:/Deploy/Comps/Kartaverse/KartaVP/Lens Profiles/

Note: If you change the sensor resolution on a camera body, this will typically modify the captured dual fisheye media's aspect ratio, and frame cropping. This sensor resolution adjustment typically requires the STMap to be regenerated so it matches the current dual fisheye lens stereo frame layout.

When the example comp files are opened up in Fusion Studio Standalone or the Resolve Studio Fusion page it looks like this:

![Comp Example](Images/kvrFisheyeStereo_Lens_Profiles_Comp.png)

The comp has Saver nodes that export the new STMap template, a Apple Vision Pro HMD formatted "Spatial video" SBS image at 16:9 aspect ratio, and a 180VR formatted RGB output that is processed using the STMapper fuse.

