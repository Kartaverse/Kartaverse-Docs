# Fusion OpenUSD Node Attributes

This is a quick summary of the attributes used by Resolve/Fusion's OpenUSD nodes that were added between Fusion v18.5 and v19.0.

## uLoader (Replaces "SurfaceFBXMesh" and "SurfaceAlembicMesh")

This node supports loading USDA/USDC/USDZ assets. It can also bring in OpenVDB files that are wrapped inside a USD asset. External OpenUSD asset instances and references are supported.

Inputs:

		Filename (USDA/USDC/USDZ file)
		ClipTimeStart (in frames)
		ClipTimeEnd (in frames)
		TimeScale (Multiplier)
		FrameOffset (in frames)
		Reverse (Bool)
		Loop (Bool)

## uRenderer (Replaces "Renderer3D")

This node allows you to select the Hydra storm render delegate settings used to generate a final rendered image output.

Inputs:

		Width     (in pixels)
		Height    (in pixels)
		GlobalIn  (in frames)
		GlobalOut (in frames)

Render Settings:

		CameraSelector (Allows you to select the name of a pre-existing OpenUSD camera from the upstream OpenUSD nodegraph)
		Lighting
		EnableSkyDome
		EnableShadows
		Complexity

		RenderPurpose
		Purpose.Render
		Purpose.Proxy
		Purpose.Guides

		AuxChannels
		Channels.Z

Film Back Fit:

	ResolutionGateFit (Camera, Inside, Width, Height, Outside, Stretch)
	Iterations

## uCamera (Replaces "Camera3D")

Inputs:

		Clip.Far
		FocalLength
		FilmBack
		HorizontalAperture    (in mm)
		VerticalAperture    (in mm)
		HorizontalApertureOffset
		VerticalApertureOffset
		ShutterClose
		ShutterOpen
		StereoRole (Left, Right, or undefined = Centre)

Transforms:

		USDXf.Translate.X
		USDXf.Translate.Y
		USDXf.Translate.Z
		USDXf.Rotate.X
		USDXf.Rotate.Y
		USDXf.Rotate.Z
		USDXf.ScaleLock
		USDXf.Scale.X
		USDXf.Scale.Y
		USDXf.Scale.Z
		USDXf.PivotNest
		USDXf.Pivot.X
		USDXf.Pivot.Y
		USDXf.Pivot.z

## uMerge (Replaces "Merge3D")

Inputs:

		SceneInput2
		SceneInput3
		SceneInput4
		...

Transforms:

		USDXf.Translate.X
		USDXf.Translate.Y
		USDXf.Translate.Z
		USDXf.Rotate.X
		USDXf.Rotate.Y
		USDXf.Rotate.Z
		USDXf.ScaleLock
		USDXf.Scale.X
		USDXf.Scale.Y
		USDXf.Scale.Z


## uShape (Replaces "Shape3D")

Shape:

		USDGeomCapsule (Undefined = Capsule)
		USDGeomCone
		USDGeomCube
		USDGeomCylinder
		USDGeomIco
		USDGeomPlane
		USDGeomSphere
		USDGeomTorus

Transforms:

		USDXf.Translate.X
		USDXf.Translate.Y
		USDXf.Translate.Z
		USDXf.Rotate.X
		USDXf.Rotate.Y
		USDXf.Rotate.Z
		USDXf.ScaleLock
		USDXf.Scale.X
		USDXf.Scale.Y
		USDXf.Scale.Z


## uDomeLight (Replaces "AmbientLight")

Note: There are several extra light types including: uCylinderLight, uDiskLight, uDistantLight, uRectLight, and uSphereLight

Inputs:

	SceneInput1

Transforms:

		USDXf.Translate.X
		USDXf.Translate.Y
		USDXf.Translate.Z
		USDXf.Rotate.X
		USDXf.Rotate.Y
		USDXf.Rotate.Z
		USDXf.ScaleLock
		USDXf.Scale.X
		USDXf.Scale.Y
		USDXf.Scale.Z

Colors:

		Color.R
		Color.G
		Color.B
		Intensity
		Exposure
		EnableColorTemperature
		ColorTemperature
		Diffuse
		Specular
		Radius
		Image (Texture filename path)
		LightTextureFormat


## uImagePlane (Replaces "ImagePlane3D")

Inputs:

	Image (Image based input connection)

Transforms:

		USDXf.Translate.X
		USDXf.Translate.Y
		USDXf.Translate.Z
		USDXf.Rotate.X
		USDXf.Rotate.Y
		USDXf.Rotate.Z
		USDXf.ScaleLock
		USDXf.Scale.X
		USDXf.Scale.Y
		USDXf.Scale.Z
		USDXf.PivotNest
		USDXf.Pivot.X
		USDXf.Pivot.Y
		USDXf.Pivot.Z
		USDXf.UseTarget
		USDXf.Target.X
		USDXf.Target.Y
		USDXf.Target.Z


## uMaterialX 

This node applies external MaterialX .mtlx shaders to Fusion based USD geometry.

Inputs:

		MaterialFile  (MTLX filename based shader network)

## uReplaceMaterial (Replaces "ReplaceMaterial3D")

Allows you to replace the existing shading network on an OpenUSD based mesh asset.

Inputs:

		PrimSelection (Allows you to select an object in the OpenUSD hiearchy passed down the node graph)
		InvertPrimSelection (Allows you to texture the unselected OpenUSD objects passed down the node graph)

External MaterialX File:

		USDMtlInputs.MaterialX.MaterialFile (MTLX filename based shader network)
		USDMtlInputs.MaterialX.MaterialSelector (Allows you to select a shading group)


Texture Controls:

		USDMtlInputs.Type
		USDMtlInputs.Diffuse.Filename (Image filename based texture map resource)


		USDMtlInputs.Diffuse.DiffuseRed
		USDMtlInputs.Diffuse.DiffuseGreen
		USDMtlInputs.Diffuse.DiffuseBlue
		USDMtlInputs.Roughness
		USDMtlInputs.Clearcoat
		USDMtlInputs.ClearcoatRoughness
		USDMtlInputs.Opacity
		USDMtlInputs.OpacityThreshold

		USDMtlInputs.Workflowmode (Undefined = Metallic, 1 = Specular)

Metallic Controls:

		USDMtlInputs.MetallicGroup.Metallic
		USDMtlInputs.Specular.SpecularRed
		USDMtlInputs.Specular.SpecularGreen
		USDMtlInputs.Specular.SpecularBlue


## PointCloud3D (Still useful):

The legacy PointCloud3D node can connect to a uMerge node

Inputs:

		MakeRenderable = 1

Transforms:

		Positions [N]

