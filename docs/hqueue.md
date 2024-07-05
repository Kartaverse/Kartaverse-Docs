# KartaLink HQueue Render

## Overview

Are you currently using Houdini HQueue to manage the 3D rendering jobs on your render farm? If that is the case then you might find the following comp script handy:

The "HQueue Render.py" comp script allows Fusion Studio to submit compositing jobs for rendering via Houdini HQueue. The script works great in both a "local queue", and for larger render farm usage scenarios.

![KartaLink HQueue Render](Images/KartaLink-Submit-Fusion-Comps-to-Houdini-HQueue.png)

## Open Source Software License

- LGPL 3.0 License

## Known Issues

The script currently works with macOS and Linux based HQueue Client render nodes.

Windows support is currently under development. On Windows the following error is reported by HQueue when a job is run:

	[WinError 2] The system cannot find the file specified 
	ERROR: Could not run command.

## Installation

This toolset is available in the Reactor package manager under the category heading "Kartaverse/KartaLink/Scripts".

Note: If you haven't heard of the "HQueue" render farm management software before, it is the license-free render farm manager from SideFX Software.

![Reactor Package Manager](Images/KartaLink-HQueue-Render-Reactor-Package-Manager.png)

## Usage

Step 1. Make sure you have defined the Reactor PathMap settings in your Fusion Render Node preferences. This will allow Reactor downloaded fuses and plugins to work correctly.

Step 2. Open the HQueue management webpage. (Typically this defaults to "http://localhost:5000"). Use the HQueue webUI to create an HQueue "Client Group" called "Fusion".

![HQueue Groups 1](Images/HQueue-Groups-1.png)
![HQueue Groups 2](Images/HQueue-Groups-2.png)

Step 3. Open a Fusion comp. Select the "Scripts > KartaLink > HQueue Render" menu item to submit a Fusion composite to your render farm.

Set the "Frames Per Task" value to define how large of a frame chunk you want each job task to use. A value of zero sets the job to render as a single job task.


![KartaLink HQueue Render 2](Images/HQueue-WebUI-2.png)

![KartaLink HQueue Render 3](Images/HQueue-WebUI-3.png)

![KartaLink HQueue Render 4](Images/HQueue-WebUI-4.png)

![KartaLink HQueue Render 5](Images/HQueue-WebUI-5.png)