# Fusion Compositing Examples

This page lists the example Fusion .comp files that come built-in with the KartaVR product download.

<a name="angular-to-cube"></a>
## Angular to Cube.comp

This example shows how to convert an angular fisheye image into each of the cubic panorama formats.

![Angular to Cube](images/examples-angular-to-cube.png)

<a name="boxworld-cubic-renderer3d"></a>
## Boxworld CubicRenderer3D.comp

![Screenshot](images/examples-boxworld-cubic-renderer3d-screenshot.jpg)

This example shows how to render elements from Fusion's 3D animation system to a cubic panorama format output.

![Boxworld CubicRenderer3D](images/examples-boxworld-cubic-renderer3d.png)

<a name="boxworld-cylindrical-renderer3d-advanced"></a>
## Boxworld CylindricalRenderer3DAdvanced.comp

![Screenshot](images/examples-boxworld-cylindrical-renderer3d-advanced-screenshot.jpg)

This example shows how to render elements from Fusion's 3D animation system to a cylindrical 360 x 90 degree format output.

![Boxworld CylindricalRenderer3DAdvanced](images/examples-boxworld-cylindrical-renderer3d-advanced.png)

<a name="boxworld-domemaster-renderer3d"></a>
## Boxworld DomemasterRenderer3D.comp

![Screenshot](images/examples-boxworld-domemaster-renderer3d-screenshot.jpg)

This example shows how to render elements from Fusion's 3D animation system to an angular fisheye based domemaster 180 degree format output.

![Boxworld DomemasterRenderer3D](images/examples-boxworld-domemaster-renderer3d.png)

<a name="boxworld-domemaster-renderer3d-advanced"></a>
## Boxworld DomemasterRenderer3DAdvanced.comp

![Screenshot](images/examples-boxworld-domemaster-renderer3d-advanced-screenshot.jpg)

This example shows how to render multi-channel elements from Fusion's 3D animation system to an angular fisheye based domemaster 180 degree format output.

![Boxworld DomemasterRenderer3DAdvanced](images/examples-boxworld-domemaster-renderer3d-advanced.png)

<a name="boxworld-equirectangular-renderer3d"></a>
## Boxworld EquirectangularRenderer3D.comp

![Screenshot](images/examples-boxworld-equirectangular-renderer3d-screenshot.jpg)

This example shows how to render elements from Fusion's 3D animation system to an Equirectangular/LatLong/spherical format output.

![Boxworld EquirectangularRenderer3D](images/examples-boxworld-equirectangular-renderer3d.png)

<a name="boxworld-equirectangular-renderer3d-advanced"></a>
## Boxworld EquirectangularRenderer3DAdvanced.comp

![Screenshot](images/examples-boxworld-equirectangular-renderer3d-advanced-screenshot.jpg)

This example shows how to render out multi-channel elements from Fusion's 3D animation system to an Equirectangular/LatLong/spherical format output.

![Boxworld EquirectangularRenderer3DAdvancecd](images/examples-equirectangular-renderer3d-advanced.png)

<a name="boxworld-oculus-stereo-renderer3d"></a>
## Boxworld Oculus Rift Stereo Renderer3D.comp

This example shows how to use an Oculus Rift DK1 or DK2 HMD display as the output device from the Fusion 3D system using the Boxworld example scene.

![Boxworld Oculus Rift Stereo Renderer3D](images/examples-boxworld-oculus-rift-stereo-renderer3d-screenshot.png)

To use this macro you need to mount the Oculus Rift DK1 or DK2 HMD as a regular monitor on Mac/Windows/Linux. This is done by disabling the "Direct to Rift" option in the Oculus Rift drivers.

In Fusion select the "Windows  > New Image View"  menu item. Then drag this floating image view onto the Oculus Rift display monitor and then resize the image view to be fullscreen.  You can now load the rendered image in Fusion on the new view using the 3 hotkey and the content will show up on the Rift's screen. It helps to turn off the View window's "Show Controls" (Command+K) and "Show Checker Underlay" options.

Clicking on the view and selecting the Fit (Command+F) option will make sure the image fills the HMD screen.

![Boxworld Oculus Rift Stereo Renderer3D Nodes](images/examples-boxworld-oculus-rift-stereo-renderer3d-nodes.png)

<a name="colorcorrector-masked"></a>
## ColorCorectorMasked.comp

![Screenshot](images/examples-colorcorrector-masked-screenshot1.jpg)

The first example shows a vertical gradient effect that is used to fade off the saturation on the image at a certain point. This vertical gradient effect would typically be used to fix a brightness or contrast effect in the sky or tripod zone, or to apply a graduated neutral density filter type effect.

![Screenshot](images/examples-colorcorrector-masked-screenshot2.jpg)

The second example shows a horizontal gradient effect that is used to fade off the saturation on the image at a certain point. This horizontal gradient effect would typically be used to fix seam issues where the contrast might not line up on the left and right frame edge on a LatLong panorama.

![Screenshot](images/examples-colorcorrector-masked-screenshot3.jpg)

The third example shows a horizontal gradient effect that has three control handles added to the gradient. These controls are used to fade off the saturation on the image at a certain point. This horizontal gradient effect would typically be used to fix a contrast issue with one part of a stitched camera view in a LatLong image.

![ColorCorectorMasked](images/examples-colorcorrector-masked.png)

<a name="conversions"></a>
## Conversions.comp

![Screenshot](images/examples-conversions1-screenshot.jpg)

This example shows several of the most common panoramic conversions you would typically do with the KartaVR toolset.

![Screenshot](images/examples-conversions2-screenshot.jpg)

![Conversions 1](images/examples-conversions1.png)

![Conversions 2](images/examples-conversions2.png)

<a name="cubic-to-domeaster180"></a>
## Cubic to Domemaster180.comp

![Screenshot](images/examples-cubic-domeaster180-screenshot.jpg)

This example shows how to convert a set of six cubic 90 degree FOV images into a domemaster 180 degree angular fisheye image.

![Cubic to Domemaster180](images/examples-cubic-to-domeaster180.png)

<a name="cubic-faces-to-equirectangular"></a>
## CubicFaces2Equirectangular.comp

![Screenshot](images/examples-cubic-faces-to-equirectangular-screenshot.jpg)

This example shows how to take a set of six cube map images and merge them into an equirectangular/LatLong/spherical format panorama.

![CubicFaces2Equirectangular](images/examples-cubic-faces-to-equirectangular.png)

<a name="cubic-renderer3d"></a>
## CubicRenderer3D.comp

This example shows how to render elements from Fusion's 3D animation system to cubic panorama format outputs.

![Screenshot](images/examples-cubic-renderer3d-screenshot1.jpg)

![Screenshot](images/examples-cubic-renderer3d-screenshot2.jpg)

![CubicRenderer3D](images/examples-cubic-renderer3d.png)

<a name="cylindrical-conversions"></a>
## Cylindrical Conversions.comp

![Screenshot](images/examples-cylindrical-conversions-screenshot.jpg)

This example shows how to convert equirectangular/spherical/latlong format imagery into a cylindrical projection. There is also an example that takes cubic imagery into a cylindrical projection and then goes back to cubic again.

![Cylindrical Conversions](images/examples-cylindrical-conversions.png)

<a name="cylindrical-renderer3d"></a>
## CylindricalRenderer3D.comp

This example shows how to render elements from Fusion's 3D animation system to a cylindrical panorama format output.

![Screenshot](images/examples-cylindrical-render3d-screenshot1.jpg)

This example shows one of the extra render channels that the CylindricalRenderer3DAdvanced node can output. In this case the UV pass channel is displayed.

![Screenshot](images/examples-cylindrical-render3d-screenshot2.jpg)

![CylindricalRenderer3D](images/examples-cylindrical-renderer3d.png)

<a name="defocus-blur-glow-sharpen"></a>
## Defocus Blur Glow Sharpen Unsharpen.comp

![Defocus Blur Glow Sharpen Unsharpen](images/examples-defocus-blur-glow-sharpen.png)

This example shows a quick demo of the new filter effects in the KartaVR. The filters wrap around the left/right frame boundaries of a panoramic image. Note: The gradient controls in the macros let you selectively fade out the effect of the filters.

![Screenshot](images/examples-defocus-blur-glow-sharpen-blurpanoramicwrap-screenshot1.jpg)

The BlurPanoramicWrap macro is used to create a title graphic with the Text+ character generator applied as an effects mask. The alpha channel on the text is inverted so it results in the background of the image being filled with a soft blurry effect while the text is clear.

![Screenshot](images/examples-defocus-blur-glow-sharpen-glowpanoramicwrap-screenshot2.jpg)

The GlowPanoramicWrap macro nicely wraps the effect around the frame border so incandescent glow effects don't get clipped if the object source is on the edge of a rendered image.

![Screenshot](images/examples-defocus-blur-glow-sharpen-glowpanoramicwrap-screenshot3.jpg)

The BlurPanoramicWrap macro can use the built-in gradient controls to fade the effect out in parts of the frame to create looks like a foggy/hazy effect.

![Screenshot](images/examples-defocus-blur-glow-sharpen-blurpanoramicwrap-screenshot4.jpg)

The BlurPanoramicWrap macro can used to easily blur out the tripod zone.

![Screenshot](images/examples-defocus-blur-glow-sharpen-blurpanoramicwrap-screenshot5.jpg)

<a name="domemaster-renderer3d"></a>
## DomemasterRenderer3D.comp

This example shows how to render elements from Fusion's 3D animation system to an angular fisheye based domemaster 180 degree format output.

![DomemasterRenderer3D](images/examples-domemaster-renderer3d.png)


<a name="equirectangular-tripod-repair"></a>
## Equirectangular Tripod Repair.comp

The top example shows tripod rig removal by taking an LatLong/Equirectangular/Spherical image, extracting the bottom "nadir" camera view, applying a paint node to do clone patching, and then finally bringing the cubic view back into the LatLong format and merging it with the original panorama.

The lower example shows tripod rig removal by taking an LatLong/Equirectangular/Spherical image, rotating the view by 90° on the X axis to make it easier to work with the ground and sky pole zones, applying a paint node to do clone patching, and then finally bringing the view back into an upright LatLong format and merging it with the original panorama.

![Equirectangular Tripod Repair](images/examples-equirectangular-tripod-repair.png)


<a name="equirectangular-to-fisheye"></a>
## Equirectangular2Fisheye.comp

![Equirectangular2Fisheye](images/macro-equirectangular-to-fisheye.jpg)

The Equirectangular2Fisheye macro converts an equirectangular image into an angular fisheye image projection. This node has an FOV control that can be animated along with XYZ rotation support.

![Equirectangular2Fisheye](images/examples-equirectangular-to-fisheye.png)

<a name="equirectangular-stereo-to-fisheye-stereo"></a>
## EquirectangularStereo2FisheyeStereo.comp

![EquirectangularStereo2FisheyeStereo Screenshot](images/examples-equirectangular-to-fisheye-screenshot.jpg)

The EquirectangularStereo2FisheyeStereo macro converts a pair of left and right equirectangular images into the angular fisheye image projection. This node has an FOV control that can be animated along with XYZ rotation support.

![EquirectangularStereo2FisheyeStereo](images/examples-equirectangular-stereo-to-fisheye-stereo.png)

<a name="equirectangular-renderer3d"></a>
## EquirectangularRenderer3D.comp

This example shows how to render elements from Fusion's 3D animation system to an Equirectangular/LatLong/spherical format output.

![EquirectangularRenderer3D](images/examples-equirectangular-renderer3d.png)

<a name="equirectangular-renderer3d-advanced"></a>
## EquirectangularRenderer3DAdvanced.comp

This example shows how to render out multi-channel elements from Fusion's 3D animation system to an Equirectangular/LatLong/spherical format output.

![EquirectangularRenderer3D](images/examples-equirectangular-renderer3d-advanced.png)

<a name="facebook-cubemap3x2"></a>
## Facebook Cubemap3x2.comp

The first example shows how to convert a Facebook Cubemap 3x2 format panorama to an equirectangular/LatLong/spherical format image.

The second example shows how to convert a Facebook Cubemap 3x2 format panorama to a Gear VR Mono Cubemap format image.

The third example shows how to convert an equirectangular/LatLong/spherical format panorama to a Facebook Cubemap 3x2 format image.

The fourth example shows how to convert a Gear VR format panorama to a Facebook Cubemap 3x2 format image.

![Facebook Cubemap3x2](images/examples-facebook-cubemap3x2.png)

<a name="facebook-vertical-strip"></a>
## Facebook Vertical Strip.comp

The first example shows how to convert a set of six cubemap face images into the Facebook Vertical Strip cubemap format.

The second example shows how to convert a Facebook Vertical Strip cubemap into an Equirectangular/LatLong/Spherical image projection.

The third example shows how to convert a Facebook Vertical Strip cubemap into a GearVR/Vray/Octane Render horizontal strip cubic image projection.

![Facebook Vertical Strip](images/examples-facebook-vertical-strip.png)

<a name="fulldome-crossbounce-sim"></a>
## Fulldome Crossbounce Sim.comp

![Fulldome Crossbounce Sim](images/examples-fulldome-crossbounce-sim.png)

This comp is a demo that simulates the rough effect of fulldome crossbounce lighting. Adjust the screen gain control to adjust the reflectivity of the dome screen. A good starting point is a screen gain value between 0.1 to 0.25

Here is a view of a raw crossbounce lighting simulation that was created with the "Crossbounce Blend" control set to 0:

![DomemasterCrossbounceSim Fullcolor Macro](images/macro-domemaster-crossbounce-sim-raw.png)

Here is a view of a raw crossbounce lighting simulation that was created with the "Crossbounce Blend" control set to 0, and the "Crossbounce Saturation" was set to 0 to create a desaturated greyscale / luminance style output:

![DomemasterCrossbounceSim Greyscale Macro](images/macro-domemaster-crossbounce-sim-greyscale.png)

This is a view of a crossbounce lighting simulation where the simulation data was automatically composited over the original fulldome plate footage. This was created by setting the "Crossbounce Blend" control to 1:

![DomemasterCrossbounceSim Comped Macro](images/macro-domemaster-crossbounce-sim-comped.png)

<a name="gearvr-mono-to-equirectangular"></a>
## GearVR Mono to Equirectangular.comp

This example shows how to convert a  GearVR/Octane Render/Vray horizontal strip cube map into an Equirectangular image.

![GearVR Mono to Equirectangular](images/examples-gearvr-mono-to-equirectangular.png)

<a name="gearvr-stereo-to-equirectangular-stereo"></a>
## GearVR Stereo to Equirectangular Stereo.comp

This example shows how to convert a stereo GearVR/Octane Render/Vray horizontal strip cube map into an Equirectangular Stereo Over/Under image.

![GearVR Stereo to Equirectangular Stereo](images/examples-gearvr-stereo-to-equirectangular-stereo.png)

<a name="latlong-to-cube"></a>
## LatLong to Cube.comp

This example shows how to convert a LatLong/Equirectangular/Spherical image into each of the cubic panorama formats.

![LatLong to Cube 1](images/examples-latlong-to-cube.png)

![LatLong to Cube 2](images/examples-latlong-to-cube2.png)

<a name="latlong-to-gearvr-stereo"></a>
## LatLong to GearVRStereo.comp

This example shows how to convert a pair of LatLong/Equirectangular/Spherical images to the GearVR stereo format. Then the comp shows how to extract that Gear VR stereo image and convert it into a stereoscopic horizontal cross image.

![LatLong to GearVRStereo](images/examples-latlong-to-gearvr-stereo.png)

<a name="logo-over-tripod"></a>
## Logo Over Tripod.comp

![Logo Over Tripod](images/examples-logo-over-tripod-screenshot.jpg)

This example places a flat logo image over the tripod zone in an Equirectangular/LatLong/Spherical panoramic image.

![Logo Over Tripod](images/examples-logo-over-tripod-nodes.png)

<a name="meshuv-conversions"></a>
## MeshUV Conversions.comp

The first example shows how to convert a Pyramid image projection into an LatLong/Equirectangular/Spherical image.

The second example shows how to convert a LatLong/Equirectangular/Spherical image into a Pyramid Mesh UV baked texture map.

The third example shows how to convert a LatLong/Equirectangular/Spherical image into a Facebook Cubemap 3x2 Mesh UV baked texture map.

The fourth example shows how to convert an Angular Fisheye 360 degree image into a Facebook Cubemap 3x2 Mesh UV baked texture map.

The fifth example shows how to convert a set of Cubic Face panoramic images into a Facebook Cubemap 3x2 Mesh UV baked texture map.

![MeshUV Conversions](images/examples-meshuv-conversions.png)

<a name="ricoh-theta-s-stitch"></a>
## Ricoh Theta S Stitch.comp

This is a KartaVR example that warps and stitches the raw footage from a Ricoh Theta S panoramic camera.

![Ricoh Theta S Stitch](images/examples-ricoh-theta-s-stitch.png)

<a name="roller-coaster-ride-cubic"></a>
## Roller Coaster Ride CubicRenderer3D

This roller coaster ride example shows how to render elements from Fusion's 3D animation system to a cubic format output.

A roller coaster track model with a camera path based animation is imported from an FBX file. Then a Fusion transform3D node is used with the "Invert Transform" checkbox to prepare the scene for easy rendering with the CubicRenderer3D node.

The example has a side by side pair of CubicRenderer3D cameras that can give you a previz grade stereoscopic 3D rendered result of the scene. The node RightViewTransform3D is used with an expression to apply a stereoscopic camera separation offset type of effect.

The output from the stereo pair of CubicRenderer3D cameras is then routed into a Gear VR cubic image format with the help of the "CubicFaces2GearVRStereo" node.

Note: Fusion doesn't support raytraced lens shaders so it is not possible to render omnidirectional stereo output at this point in time.

![Roller Coaster Ride Cubic](images/examples-roller-coaster-ride-cubic.jpg)

![Roller Coaster Ride Cubic Nodes](images/examples-roller-coaster-ride-cubic-nodes.png)


<a name="roller-coaster-ride-cylindrical"></a>
## Roller Coaster Ride CylindricalRenderer3D

This roller coaster ride example shows how to render elements from Fusion's 3D animation system to a cylindrical format output.

A roller coaster track model with a camera path based animation is imported from an FBX file. Then a Fusion transform3D node is used with the "Invert Transform" checkbox to prepare the scene for easy rendering with the CylindricalRenderer3D node.

The example has a side by side pair of CylindricalRenderer3D cameras that can give you a previz grade stereoscopic 3D rendered result of the scene. The node RightViewTransform3D is used with an expression to apply a stereoscopic camera separation offset type of effect. Note: Fusion doesn't support raytraced lens shaders so it is not possible to render omnidirectional stereo output at this point in time.

![Roller Coaster Ride Cubic](images/examples-roller-coaster-ride-cylindrical.jpg)

![Roller Coaster Ride Nodes](images/examples-roller-coaster-ride-cylindrical-nodes.png)

<a name="roller-coaster-ride-domemaster"></a>
## Roller Coaster Ride DomemasterRenderer3D

This roller coaster ride example shows how to render elements from Fusion's 3D animation system to a domemaster angular fisheye format output.

A roller coaster track model with a camera path based animation is imported from an FBX file. Then a Fusion transform3D node is used with the "Invert Transform" checkbox to prepare the scene for easy rendering with the DomemasterRenderer3D node.

The example has a side by side pair of DomemasterRenderer3D cameras that can give you a previz grade stereoscopic 3D rendered result of the scene. The node RightViewTransform3D is used with an expression to apply a stereoscopic camera separation offset type of effect. Note: Fusion doesn't support raytraced lens shaders so it is not possible to render omnidirectional stereo output at this point in time.

![Roller Coaster Ride Domemaster](images/examples-roller-coaster-ride-dome.jpg)

![Roller Coaster Ride Domemaster Nodes](images/examples-roller-coaster-ride-dome-nodes.png)

<a name="roller-coaster-ride-latlong"></a>
## Roller Coaster Ride EquirectangularRenderer3D

This roller coaster ride example shows how to render elements from Fusion's 3D animation system to an Equirectangular/LatLong/spherical format output.

A roller coaster track model with a camera path based animation is imported from an FBX file. Then a Fusion transform3D node is used with the "Invert Transform" checkbox to prepare the scene for easy rendering with the EquirectangularRenderer3D node.

The example has a side by side pair of EquirectangularRenderer3D cameras that can give you a previz grade stereoscopic 3D rendered result of the scene. The node RightViewTransform3D is used with an expression to apply a stereoscopic camera separation offset type of effect. Note: Fusion doesn't support raytraced lens shaders so it is not possible to render omnidirectional stereo output at this point in time.

![Roller Coaster Ride](images/examples-roller-coaster-ride-latlong.jpg)

![Roller Coaster Ride Nodes](images/examples-roller-coaster-ride-equirectangular-renderer-3d-nodes.png)

<a name="roller-coaster-ride-oculus-rift-stereo"></a>
## Roller Coaster Ride Oculus Rift Stereo.comp

This roller coaster ride example shows how the "OculusDK1StereoRenderer3D" macro that allows you to use an Oculus Rift DK1 HMD display as the output device from the Fusion 3D system.

![Roller Coaster Ride Oculus Rift Stereo](images/examples-roller-coaster-ride-oculus-rift-stereo-screenshot.png)

A roller coaster track model with a camera path based animation is imported from an FBX file. Then a Fusion transform3D node is used with the "Invert Transform" checkbox to prepare the scene for easy rendering with the OculusDK1StereoRenderer3D and OculusDK2StereoRenderer3D nodes.

To use this macro you need to mount the Oculus Rift DK1 or DK2 HMD as a regular monitor on Mac/Windows/Linux. This is done by disabling the "Direct to Rift" option in the Oculus Rift drivers.

In Fusion select the "Windows > New Image View" menu item. Then drag this floating image view onto the Oculus Rift display monitor and then resize the image view to be fullscreen. You can now load the rendered image in Fusion on the new view using the 3 hotkey and the content will show up on the Rift's screen. It helps to turn off the View window's "Show Controls" (Command+K) and "Show Checker Underlay" options.

Clicking on the view and selecting the Fit (Command+F) option will make sure the image fills the HMD screen.

![Roller Coaster Ride Oculus Rift Stereo Nodes](images/examples-roller-coaster-ride-oculus-rift-stereo-nodes.png)


<a name="roller-coaster-ride-acer-wmr-stereo"></a>
## Roller Coaster Ride Acer WMR Stereo.comp

![Roller Coaster Ride Acer WMR Stereo](images/macro-acer-wmr-stereo-renderer3d.png)

This roller coaster ride example shows how the "AcerWMRStereoRenderer3D" macro that allows you to use an Acer Windows Mixed Reality HMD display as the output device from the Fusion 3D system.

A roller coaster track model with a camera path based animation is imported from an FBX file. Then a Fusion transform3D node is used with the "Invert Transform" checkbox to prepare the scene for easy rendering with the AcerWMRStereoRenderer3D nodes.

To use this macro you need to mount the AcerWMR as a regular monitor on Mac/Windows/Linux.

In Fusion select the "Windows  > New Image View"  menu item. Then drag this floating image view onto the AcerWMR display monitor and then resize the image view to be fullscreen.  You can now load the rendered image in Fusion on the new view using the 3 hotkey and the content will show up on the AcerWMR's screen. It helps to turn off the View window's "Show Controls" (Command+K) and "Show Checker Underlay" options.

Clicking on the view and selecting the Fit (Command+F) option will make sure the image fills the HMD screen.

![Roller Coaster Ride Acer WMR Rift Stereo Nodes](images/examples-roller-coaster-ride-acer-wmr-stereo-nodes.png)


<a name="rotate-panorama"></a>
## Rotate Panoramas.comp

This example shows how to use the RotateEquirectangular, RotateGearVRMono, and RotateCubicFaces macros to adjust the XYZ rotation of your panoramic imagery.

![Rotate Panoramas Nodes](images/examples-rotate-panorama-nodes.png)


<a name="samsung-gear-360-stitch"></a>
## Samsung Gear 360 Stitch.comp

This example stitches the raw footage from a Samsung Gear 360 panoramic camera into an equirectangular/LatLong/spherical format panorama.

![Samsung Gear 360 Stitch](images/examples-samsung-gear-360-stitch.jpg)

![Samsung Gear 360 Stitch Nodes](images/examples-samsung-gear-360-stitch-nodes.png)

<a name="stereo-3d-roto-conversion"></a>
## Stereo 3D Roto Conversion.comp

This example shows how a 2D monoscopic panoramic 360&deg; image can be displaced into an omni-directional 3D stereoscopic image using the "DisplaceEquirectangular" macro node with a greyscale depthmap that was created using rotoscoping.

![Stereo 3D Roto Conversion 1](images/examples-stereo-3d-roto-conversion-1.png)

![Stereo 3D Roto Conversion 2](images/examples-stereo-3d-roto-conversion-2.png)

The composite starts with loading a 2D forest panorama image.

A series of BSpline rotoshapes are added to trace the depth of each of the major trees, bushes, and objects in the image. Then each of the rotosplines are give a specific greyscale shaded depth value from 0-1 which represents the depth from the back of the world to the front of the scene.

![DisplaceEquirectangular Depth map](images/macro-displace-equirectangular-rotoscoped-depthmap.png)

Finally, the "DisplaceEquirectangular" macro node pushes and pulls the pixels in the scene to turn the 2D panorama into a stereosopic 3D output. The composite has a stereo over/under output, an anaglyph stereoscopic live preview output, a depthmap output that is previewed as an anaglyph stereo image so you can see the results interactively as you are drawing the rotoshapes, and an animated "wiggle" stereo preview to check the depth in the scene.

The wiggle format GIF animation is helpful as it shows the generated "in between" stereoscopic camera views that are possible to create from an original 2D mono panorama.

![DisplaceEquirectangular Wiggle Animation](images/macro-displace-equirectangular.gif)

At the bottom of the comp is an example of the DepthBlurPanoramicWrap node that is applying a defocusing effect that varies based upon the distance from the camera.

![DepthBlurPanoramicWrap](images/macro-depth-blur-panoramic-wrap.jpg)

<a name="stereo"></a>
## Stereo.comp

This example shows the most common panoramic 360&deg; stereo format conversions that are done with the KartaVR.

![Stereo](images/examples-stereo.png)

<a name="text-imageplane-stereo"></a>
## Text+ Imageplane Stereo.comp

This example shows how to create text in Fusion that can be mapped onto a polygon image plane using Fusion's 3D system.

As a bonus a parallel stereo camera rig is created that allows you to render out equirectangular stereo imagery that can be viewed using the stereo side by side merge node, or the stereo anaglyph nodes in the composite.

![Text+ Imageplane Stereo](images/examples-text-imageplane-stereo.png)

<a name="text-matrix-domemasterrender3d"></a>
## Text+ Matrix DomemasterRender3D.comp

This example shows how to create a fulldome version of The Matrix "raining text".

![Text+ Matrix DomemasterRender3D](images/examples-text-matrix-domemasterrenderer3d.jpg)

A Text+ node is used to generate a tall hexadecimal text string. Then an offset node animates the text scrolling upwards continuously using an expression driven by the current frame value.

This texture map is applied to a polygon plane that is then duplicated into a grid like layout using two duplicate nodes.

The final scene is then rendered out to a 180° fulldome angular fisheye image prjoection using a DomemasterRenderer3D node. A rays node is used to create light streaks and a subtle color correction effect is applied to adjust the HDR lighting look from the rays.

A background node is used to add a solid black background color to the composite.

![Text+ Matrix DomemasterRender3D Node](images/examples-text-matrix-domemasterrenderer3d-node.png)


<a name="text-to-domemaster"></a>
## Text+ to Domemaster.comp

This example shows a quick and easy way to create text in Fusion that can be placed anywhere in a domemaster 180 degree image.

A Text+ node is created with a 1:1 aspect ratio. This Text+ node is connected to the "front" input on a CubicFaces2Domemaster180 node. You can use the XYZ Rotation controls on the CubicFaces2Domemaster180 node to place the text element anywhere in the angular fisheye frame.

![Text+ to Domemaster](images/examples-text-to-domemaster.png)

<a name="text-to-equirectangular"></a>
## Text+ to Equirectangular.comp

This example shows a quick and easy way to create text in Fusion that can be placed anywhere in a 360&deg; panoramic image.

A Text+ node is created with a 1:1 aspect ratio. This Text+ node is connected to the "front" input on a CubicFaces2Equirectangular node. You can use the **XYZ Rotation** controls on the CubicFaces2Equirectangular node to place the text element anywhere in the panorama.

As a bonus the output from the CubicFaces2Equirectangular node is connected to an Offset macro and a Stereo Merge node that allows you to create a simulated stereo depth value for the text.

![Text+ to Equirectangular](images/examples-text-to-equirectangular.png)

<a name="uv-pass-latlong-stereo-to-cubemap-3x2-stereo"></a>
## UV Pass LatLongStereo to Cubemap3x2Stereo.comp

This example shows how to use a UV pass map to reformat a pair of LatLong/Equirectangular/Spherical stereo images into the cubemap 3x2 stereo image projections.

![UV Pass LatLongStereo to Cubemap3x2Stereo](images/examples-uv-pass-latlong-stereo-to-cubemap-3x2-stereo.png)

<a name="uv-pass-texture-projection"></a>
## UV Pass Texture Projection.comp

This example shows how to perform UV pass based panoramic 360&deg; image transformations.

![UV Pass Texture Projection](images/examples-uv-pass-texture-projection.png)

<a name="uv-pass-video-stitching"></a>
## UV Pass Video Stitching Template.comp

This is a starting template for UV pass based panoramic 360&deg; video stitching. The final stitched panoramic video is written to disk using the saver node on the bottom right of the composite named "PanoramaSaver".

You can duplicate and modify this structure to support stitching any number of panoramic cameras in your video rig. As you modify this node graph, you can connect each panoramic 360&deg; video camera view together in the composite using the merge nodes on the right named "ViewMerge".

![UV Pass Video Stitching Template](images/examples-uv-pass-video-stitching-template.png)

To prepare your footage for use with this video stitching template the KartaVR "Generate UV Pass in PTGui" script should be used to turn your PTGui stitching .pts project file into a set of UV pass based panoramic warping images (ST Maps) that allow you to warp your video into the final panoramic image projection.

The node named "CameraLoader" is used to load in the footage from one of your panoramic video rig cameras. The "UVPassLoader" node is used to load in a matching uv pass warping image for that specific camera view.

The "BSplineMask" node is used along with an "AlphaMaskMerge" node to draw a custom rotoshape to select the part of a camera view you want to keep in the composite.

The "AlphaMaskMerge" node is disabled by default with the Fusion "pass through" mode as it can only be used when you have created an acutal mask shape in the BSplineMask node.

The saver nodes on the right hand side of the composite named "CameraMaskSaver" are used to allow you to export each of the camera view's custom BSpline alpha masks to disk if you want to use them later with an external compositing tool.

The "ColorCorrector" node is used to apply the primary color correction. Then the "ColorCorrectorMasked" node is used with the built-in gradient controls to adjust the masking of the color adjustments that will allow you to fine tune the brightness and color falloff in different regions in the frame like the pole area.

The "ViewerEquirectangular" node is used as a panoramic 360&deg; media viewer tool that simulates the playback of LatLong format media on an flat monitor view.

<a name="viewer-cubic-faces"></a>
## Viewer Cubic Faces.comp

This comp shows a process for easily extracting 16:9 rectangular video frames from panoramic cubic map based imagery.

![Viewer Cubic Faces](images/examples-viewer-cubic-faces.png)

<a name="viewer-equirectangular"></a>
## Viewer Equirectangular.comp

This comp shows a process for easily extracting a 16:9 rectangular video frame from a 360x180 degree LatLong/Equirectangular/Spherical immersive image.

![Viewer Equirectangular](images/examples-viewer-equirectangular.png)

<a name="viewer-equirectangular-stereo"></a>
## Viewer Equirectangular Stereo.comp

This comp shows a process for easily extracting stereoscopic 16:9 rectangular video frames from a 360x180 degree LatLong/Equirectangular/Spherical stereo immersive image.

![Viewer Equirectangular Stereo](images/examples-viewer-equirectangular-stereo.png)

<a name="viewer-mesh-stereo"></a>
## Viewer Mesh Stereo.comp

This ViewerMeshStereo example takes two LatLong/Equirectangular/Spherical images and does a panoramic defishing operation to turn them into a pair of left and right view images in a regular rectangular image format.

![Viewer Mesh Stereo](images/examples-viewer-mesh-stereo.png)

<a name="viewer-mesh"></a>
## ViewerMesh.comp

This example shows the result of displaying panoramic 360&deg; imagery with the ViewerMesh macro.

Each row of nodes in this document loads a different panoramic format into the compsite and displays them by using the appropriate custom format OBJ mesh file in the ViewerMesh macro.

![Viewer Mesh](images/examples-viewer-mesh.png)

<a name="wireframe-oculus-rift-stereo"></a>
## Wireframe Oculus Rift Stereo.comp

This example shows how the  "OculusDK1StereoRenderer3D"  and "OculusDK2StereoRenderer3D" node allows you to use an Oculus Rift HMD display as the output device from the Fusion 3D system. A wireframe version of the boxworld scene is rendered as a stereo image in the Oculus Rift output format.

![Wireframe Oculus Rift Stereo](images/examples-wireframe-oculus-rift-stereo-screenshot.png)

To use this node you need to mount the Oculus Rift DK1 or DK2 HMD as a regular monitor on Mac/Windows/Linux. This is done by disabling the "Direct to Rift" option in the Oculus Rift drivers.

In Fusion select the "Windows  > New Image View"  menu item. Then drag the floating viewer onto the Oculus Rift display monitor and resize the viewer to be fullscreen.  You can now load the imagery in the viewer using the 3 hotkey and the content will show up on the Rift's screen. It helps to turn off the viewer's "Show Controls" (Command+K) and "Show Checker Underlay" options.

Clicking on the view and selecting the Fit (Command+F) option will make sure the image fills the HMD screen.

![Wireframe Oculus Rift Stereo Nodes](images/examples-wireframe-oculus-rift-stereo-nodes.png)


<a name="looking-glass-renderer-3d"></a>
## LookingGlassRenderer3D.comp

This comp will render Fusion 3D system based content into a Looking Glass display 4x4 quilted grid format that can be displayed using the native Looking Glass display playback tools. You can expand the "LookingGlassRenderer3D" macro node's group to adjust any setting you want.

This is the node view in its regular compact form:

![LookingGlassRenderer3D.comp](images/examples-lookingglassrenderer3d-nodes-1.png)

If you want to tinker with the nodes inside the LookingGlassRenderer3D macro you can expand the group node by clicking on the little "line" icon on the top right side of the collapsed node shape.

When the group is expanded you will see all of the Camera3D and Renderer3D nodes that are packed inside of the macro that are used to render out the grid view.

![LookingGlassRenderer3D.comp](images/examples-lookingglassrenderer3d-nodes-2.png)

If you select the SceneMerge3D node inside the macro and view it on the right viewer window you will see the stereo camera rig and the model that is being rendered.

![16 Camera array](images/16-camera-linear-array.png)

<a name="looking-glass-4x4-quilted-anaglyph-stereo-3d-viewer"></a>
## Looking Glass 4x4 Quilted Anaglyph Stereo 3D Viewer.comp

This comp will decode a static Looking Glass display 4x4 quilted grid based linear array image and preview it on a desktop monitor as anagyph stereo 3D imagery.

The comp uses a pair of TimeStretcher + Crop nodes the clip out each of the quilted grid images into their own separate images. The stereo display works by having the right eye stereo view display one image view later in the linear camera array sequence then the left eye sees.

![LookingGlass Quilted Anaglyph Stereo 3D Viewer.comp](images/examples-looking-glass-quilted-anaglyph-stereo-3d-viewer-nodes.png)

To view the anaglyph output select the StereoAnaglyphHalfColorMerge node at the bottom left of the flow area. Then press the "1" or "2" keys to target the node's output at either the left or right viewer window in Fusion.

![anaglyph-viewer-output.png Node](images/anaglyph-viewer-output.png)

This composite allows you to convert the quilted multi-view image into a 16 frame long anaglyph stereo preview of the scene. When you hit play on the timeline it will automatically track the viewer window in stereo through the linear array footage.

![LookingGlass Quilted Anaglyph Stereo 3D Viewer.comp](images/anaglyph-stereo-preview.png)

You can change Fusion's timeline playback mode from "looped" playback to A "ping-pong" playback MODE that goes forwards and backwards in Fusion's timeline by clicking on this control in the bottom timeline area in Fusion's UI:

![Fusion Looped Playback](images/playback-control.png)

![Fusion PingPong Playback](images/playback-control-pingpong.png)

<a name="looking-glass-4x4-quilted-to-image-sequence"></a>
## Looking Glass 4x4 Quilted to Image Sequence.comp


![LookingGlass Quilted to Image Sequence.comp](images/examples-looking-glass-quilted-to-image-sequences.png)

This comp will decode a static Looking Glass display 4x4 quilted grid based linear array image and turn it into an image sequence.

Due to the way the timeStretcher node works inside of the "ImageGridExtractor" macro, you have to start the in-point in the timeline at the total number of quilted views. In this case there are 4x4 quilted views so the timeline starts on frame 16.

![LookingGlass Quilted to Image Sequence Output](images/examples-looking-glass-quilted-to-image-sequences-output.png)

<a name="looking-glass-5x9-quilted-anaglyph-stereo-3d-viewer"></a>
## Looking Glass 5x9 Quilted Anaglyph Stereo 3D Viewer.comp


![Looking Glass 5x9 Quilted Anaglyph Stereo 3D Viewer.comp](images/examples-looking_glass_5x9_quilted_anaglyph_stereo_3d_viewer.png)

This comp will decode a static Looking Glass display 5x9 quilted grid based linear array image and preview it on a desktop monitor as anagyph stereo 3D imagery.

The comp uses a pair of TimeStretcher + Crop nodes the clip out each of the quilted grid images into their own separate images. The stereo display works by having the right eye stereo view display one image view later in the linear camera array sequence then the left eye sees.

There are 5x9 quilted views so the timeline starts on frame  "Global In -45".

Quilted Image to Side-By-Side Stereo Preview:

![Looking Glass 5x9 Quilted Anaglyph Stereo 3D Viewer Output 1](images/examples-looking_glass_5x9_quilted_anaglyph_stereo_3d_viewer_output1.png)

Quilted Image to Anaglyph Stereo Preview:

![Looking Glass 5x9 Quilted Anaglyph Stereo 3D Viewer Output 2](images/examples-looking_glass_5x9_quilted_anaglyph_stereo_3d_viewer_output2.png)
<a name="looking-glass-5x9-quilted-to-image-sequence"></a>
## Looking Glass 5x9 Quilted to Image Sequence.comp

![Looking Glass 5x9 Quilted to Image Sequence.comp](images/examples-looking_glass_5x9_quilted_to_image_sequence.png)

This comp will decode a static Looking Glass display quilted grid based linear array image and turn it into an image sequence.

Due to the way the timeStretcher node works inside of the "ImageGridExtractor" macro, you have to start the in-point in the timeline at Global In (zero minus the total number of quilted views). In this case there are 5x9 quilted views so the timeline starts on frame  "Global In -45".

![Looking Glass 5x9 Quilted to Image Sequence Output](images/examples-looking_glass_5x9_quilted_to_image_sequence-output.png)
