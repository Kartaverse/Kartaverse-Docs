# Creating Fusion Viewer Custom Guides

The latest build of Fusion added a really nifty improvement that unlocks the "Guides:/" PathMap folder as a location that can be used for holding user created guide overlays.

This approach interfaces with the existing guide overlay technology that is found in the "Guides > Show Guides" menu in the viewer windows where you would traditionally add "Safe Title" overlays.

Here is a custom guide file that draws a 3x4 grid layout. The file is called "3x4.guide" and can be saved into the "UserPaths:Guides" or "Reactor:/Deploy/Guides/" folder.

	Guide
	{
		Name = "3x4",
	
		Elements =
		{
			HLine { Y1="33.3333%", Pattern = 0xF0F0, Color = { R = 1.0, G = 0.75, B = 0.05, A=1.0 } },
			HLine { Y1="66.6667%", Pattern = 0xF0F0, Color = { R = 1.0, G = 0.75, B = 0.05, A=1.0 } },
			VLine { X1="25%", Pattern = 0xF0F0, Color = { R = 1.0, G = 0.75, B = 0.05, A=1.0 } },
			VLine { X1="50%", Pattern = 0xF0F0, Color = { R = 1.0, G = 0.75, B = 0.05, A=1.0 } },
			VLine { X1="75%", Pattern = 0xF0F0, Color = { R = 1.0, G = 0.75, B = 0.05, A=1.0 } },
		},
	}

The .guide file structure is a lua table that allows you to define various graphics primitives including horizontal and vertical lines, rectangles, etc. 

The guide measurements can be entered in percentages like "10%" or using fixed pixel values relative to the top/bottom/left/right edges of the window "10T", "10B","10L", "10R".

With the guide file format you can draw lines with a dashed pattern, and with custom RGB colors. Lua style comments can be added using "--" characters to a guide.

When drawing rectangle shapes you can apply a "FillColor" color value to the area inside or outside of the rectangle to create a solid color area. The alpha (A) value in the RGBA color defines the opacity of the fill color.

You can define a blending mode as [XOR](https://en.wikipedia.org/wiki/XOR_gate) if you want to control how overlapping shapes are handled.

## Shapes:

	VLine { X1 = "38.26%", Pattern = 0xC0C0, Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 } },
	HLine { Y1 = "61.74%", Pattern = 0xC0C0, Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 } },
	Rectangle { Pattern = 0xCCCC, X1 = "0%", Y1 = "0%", X2 = "61.74%", Y2 = "100%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },

## Line Pattern: (Using HEX values)

	Pattern = 0x0000,
	Pattern = 0xC0C0,
	Pattern = 0xF0F0,

## Blend Mode:

	BlendMode = "XOR",

## Colors:

	Color = { R = 1, G = 1, B = 1, A = 0.5 },
	FillColor = { R = 0, G = 0, B = 0, A = 0.75 },

## Rectangle Fill Style:

	FillMode = "Inside",
	FillMode = "Outside",

## "Golden Rectangle.guide" Example:

	Guide
	{
		Name = "Golden Rectangle",
	
		Elements =
		{
			-- 21
			Rectangle { Pattern = 0xCCCC, X1 = "0%", Y1 = "0%", X2 = "61.74%", Y2 = "100%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
	
			-- 13
			Rectangle { Pattern = 0xCCCC, X1 = "61.74%", Y1 = "0%", X2 = "100%", Y2 = "61.74%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
	
			-- 8
			Rectangle { Pattern = 0xCCCC, X1 = "76.56%", Y1 = "61.74%", X2 = "100%", Y2 = "100%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
	
			-- 5
			Rectangle { Pattern = 0xCCCC, X1 = "61.74%", Y1 = "75.74%", X2 = "76.56%", Y2 = "100%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
	
			-- 3
			Rectangle { Pattern = 0xCCCC, X1 = "61.74%", Y1 = "61.74%", X2 = "69.19%", Y2 = "75.74%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
	
			-- 2
			Rectangle { Pattern = 0xCCCC, X1 = "69.19%", Y1 = "61.74%", X2 = "76.56%", Y2 = "71.3%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
	
			-- 1
			Rectangle { Pattern = 0xCCCC, X1 = "69.19%", Y1 = "71.3%", X2 = "72.875%", Y2 = "75.74%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
	
			-- 1
			Rectangle { Pattern = 0xCCCC, X1 = "72.875%", Y1 = "71.3%", X2 = "76.56%", Y2 = "75.74%", Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 }, FillMode = "Inside", FillColor = { R = 0, G = 0, B = 0, A = 0.0 }, },
		},
	}


## "Golden Ratio.guide" Example:

	Guide
	{
		Name = "Golden Ratio",
	
		Elements =
		{
			HLine { Y1 = "38.26%", Pattern = 0xC0C0, Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 } },
			HLine { Y1 = "61.74%", Pattern = 0xC0C0, Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 } },
			VLine { X1 = "38.26%", Pattern = 0xC0C0, Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 } },
			VLine { X1 = "61.74%", Pattern = 0xC0C0, Color = { R = 1.0, G = 0.75, B = 0.05, A = 1.0 } },
		},
	}

# Built-in Guides

Fusion ships with several preset guide examples.

## 10px.guide
This example shows how to define the guide placement using pixel values.

	Guide
	{
		Name = "10 Pixels",
	
		Elements =
		{
			HLine { Y1="10T" },
			HLine { Y1="10B" },
			VLine { X1="10L" },
			VLine { X1="10R" },
		},
	}


## Safe Frame.guide

	Guide
	{
		Name = "Safe Frame",
	
		Elements =
		{
			HLine { Y1="10%", Pattern = 0xF0F0 },
			HLine { Y1="90%", Pattern = 0xF0F0 },
			HLine { Y1="95%" },
			HLine { Y1="5%" },
			VLine { X1="10%", Pattern = 0xF0F0 },
			VLine { X1="90%", Pattern = 0xF0F0 },
			VLine { X1="95%" },
			VLine { X1="5%" },
			HLine { Y1="50%", Pattern = 0xF0F0, Color = { R = 1.0, G = 0.75, B = 0.05, A=1.0 } },
			VLine { X1="50%", Pattern = 0xF0F0, Color = { R = 1.0, G = 0.75, B = 0.05, A=1.0 } },
		},
	}

## Thirds.guide

	Guide
	{
		Name = "Thirds",
	
		Elements =
		{
			HLine { Y1="33%", Pattern = 0xC0C0, Color = { R = 1.0, G = 1.0, B = 1.0, A = 1.0 } },
			HLine { Y1="67%", Pattern = 0xC0C0, Color = { R = 1.0, G = 1.0, B = 1.0, A = 1.0 } },
			VLine { X1="33%", Pattern = 0xC0C0, Color = { R = 1.0, G = 1.0, B = 1.0, A = 1.0 } },
			VLine { X1="67%", Pattern = 0xC0C0, Color = { R = 1.0, G = 1.0, B = 1.0, A = 1.0 } },
		},
	}


## WHD.guide

	Guide
	{
		Name = "WHD",
	
		Elements =
		{
			HLine { Y1 = "8.7%", BlendMode = "XOR" },
			HLine { Y1 = "83%", BlendMode = "XOR" },
			Rectangle { Pattern = 0x0000, X1 = "0%", Y1 = "8.7%", X2 = "100%", Y2 = "83%", Color = { R=1, G=1, B=1, A=0.5 }, FillMode = "Outside", FillColor = { R=0, G=0, B=0, A=0.75 }, },
		},
	}
