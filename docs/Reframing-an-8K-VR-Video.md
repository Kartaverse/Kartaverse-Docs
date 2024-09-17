# Reframing an 8K VR Video

## Overview

This quick guide covers how to make a better vertical format social media VR reframe effect in a standard DaVinci Resolve 1080x1920px resolution video timeline.

## Using the new Workflow

Create the Resolve timeline at the correct frame size that matches your final output format.

Add the full length video clip to the Edit page **WITHOUT** any initial in/out point trimming performed in advance in either the Media Page, or the Edit page.

Set the clip-level mismatched resolution resizing in the Edit page inspector window to "Stretch".

Make a new compound from the footage by right-clicking on the clip in the Edit page timeline. In the contextual menu select "New Compound Clip…"

Open the Effects panel. Then expand and select the "Toolbox \> Effects \> KartaVP" section. Add a new "kvrViewer" effects template using the search field in the dialog. 

*Note: You may have to update your existing Kartaverse plugins inside the (free) Reactor package manager. For this workflow to really shine, you need to have an August 2024 or newer release of the KartaVP tools.*

In the Edit page Inspector window, switch to the Effects control page. Then click the little white "magic wand" icon, next to the entry for "kvrViewer". This allows you to access the effects template's internal nodes.

In the Fusion page, break the automatically created connection line going from the default "MediaIn1 \-\> kvrViewer1" node.

*Note: The next thing we are going to do is a little workflow trick brought to you by creative folks at Hugh Hou Films and the Kartaverse dev team. This workaround lets us bypass, in a single move, just about all of DaVinci Resolve's internal timeline based resolution limits and image resizing "image filter hits" that the conventional Edit page to Fusion page data I/O process causes by design. The visual difference from doing this extra step, is like night and day for image quality, when loading in 5.7K or 8K+ resolution media that will be used for horizontal to vertical format VR reframing conversions\! Nice. 👌*

Show the Media Pool tab at the top left of the Resolve Edit page. Drag the exact same video clip from the Media Pool bin into the Fusion page node graph area. For better organisation and tidiness, you might want to place this MediaIn2 node vertically, just above the initial MediaIn1 node.

Connect this newly added MediaIn2 clip to the kvrViewer nodes' Input1 image connection.

If you display the MediaIn2 clip in the Fusion viewer window, the top right corner of the image should list the original media's frame size, not the current timeline resolution. If you still see your camera's original 5.7K or 8K footage resolution listed, it means no image quality has been lost at this "direct media access" stage of the reframing process.

Adjust the kvrViewer node in the Inspector window to turn OFF the "auto-resolution" control. Auto-Resolution is typically used to match the input image resolution to the output image resolution and aspect ratio. We don't want this option to be used if going for vertical format video as our intended deliverable.

*Note: If we are going for a vertical format output the initial footage is sourced from either a 16:9 or 2:1 aspect ratio video file. The output image projection we want is going to be rendered to a 9:16 ratio for social media friendly vertical format video. 🎥*

For vertical format 1080p video output set the width to "**1080**". The set the height to "**1920**".

For vertical format 2160p video output set the width to "**2160**". The set the height to "**3840**".

Set the image projection to either "180VR" or "360VR," as required. This parameter needs to match your camera's native VR capture format. This image projection setting is simply defining the type of VR content we are loading into Resolve.

If the content is monoscopic video, enable the "Mono" setting on the kvrViewer node.

Save the Resolve project.

If you want to collapse left and right eye based SBS (Side-By-Side) or OU (Over/Under) stereo 3D footage down to monoscopic content, simply add a Kartaverse "kvrCropStereo" node to the node graph, just in front of the existing "kvrViewer" node. Set the kvrCropStereo node's Stereo "Input Mode" to match your stereo content frame layout. Then set the Stereo "Output Mode" to "Mono" so you are then going to be able to reframe a monoscopic 2D video for social media usage.

Return back to the Edit page timeline.

Bump the playhead either forwards, or backwards by a few frames to refresh the viewer window. This is needed to update the cached image shown in the Edit page viewer window.

At the bottom left of the Edit page viewer window a small square overlay control icon exists. Select the "Fusion Overlay" option to support accessing the kvrViewer on screen reframing view rotation and zooming controls.

Turn on the kvrViewer node's keyframe options in the Edit page Inspector \> Effects window for the "Center X/Y", "Angle", and "Zoom" controls.

Do your 360VR reframing steps as usual.

If you need to, use the Edit page Inspector windows' "magic wand" icon again to bring the kvrViewer Effects Template data into the Fusion page. 

You can then access Fusion's much more flexible animation curve based tangent editing tools to refine the motion of the reframing work. The Fusion page has its own keyframe adjustment controls that are accessed using the Spline and Keyframe panels.

Once you like the motion of your reframed content, and have completed editing your video:

On the Deliver page you ideally want to export MP4 H.265 video at a social media friendly 1080x1920px or a larger 2160x3840px frame size. This is a video resolution that has a (9:16 aspect ratio) vertical format layout.

Render this footage to disk using the Deliver page render queue.

You can then upload the final reframed "flat" video content to social media platforms like Instagram, TikTok, or YouTube shorts that feature vertical format video as the default frame size.

## Render in Place Usage

If you are going to be working on a hybrid social media post that intermixes VR and non-VR video, you might consider using the "Render in Place" feature.

This would be done on a copy of the VR reframing timeline's video track on the Edit page. The Render in Place command would help by caching a flattened copy of the final reframed content, in a way you will see zero delay for editing and playback.

This is often relevant if you are doing a video editing project that lasts more than half a day, or so. 

## Closing Thoughts

***Good Luck and happy reframing of your immersive memories\!\!\!*** 

May your social media feed become packed with even more exciting content from your life's adventures. 🤘
