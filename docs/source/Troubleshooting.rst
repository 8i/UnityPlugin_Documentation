Troubleshooting
===============

Improving Performance
---------------------

	Use lower resolution data
		We recommend using this table when choosing which resolution to use for your application.

		==================   ==   ==========================
		Resolution           PC   Mobile
		==================   ==   ==========================
		1,500,000            ✓	  ✖
		800,000              ✓    ✓ ( High End Required )
		600,000              ✓    ✓ 
		400,000              ✓    ✓ 
		==================   ==   ==========================

		The filename of the hvr file will tell you the resolution. This number represents the density of the data and the overall quality.
		
		The naming convention is [NAME]_[Resolution]_[FrameNumber].[Extension]

		Most files follow this naming convention. If you are not sure, please send an email to your contact at 8i.

		Ie: BOXER_200_tc_v01_800000_001009.hvr will be:
		
		==================   ================
		Name                 BOXER_200_tc_v01
		Resolution           800,000
		Frame                1009
		==================   ================

	Change the HvrActor render method
		It is recommended to use the 'Point Sprite' render method in order to improve performance.
		
		The alternative, 'Point Blend' is around twice as expensive to render.

	Change the HvrRender render mode
		The 'Direct' render mode provides the best performance and memory usage.
		
		There are downsides of this method which are outlined in the HvrRender section of this documentation.

HVR Actors are not rendering
----------------------------

	Windows
		The Graphics API may not be supported.
			Go to 'Edit/Project Settings/Player' and make sure that the PlayerSettings 'Graphics API for Windows' is set to either DirectX11 or OpenGL2. These are the only supported graphics APIs at this time.

	Android
		The Graphics API may not be supported.
			Make sure that under the PlayerSettings that the targeting GraphicsAPI is GLES3 and that your device supports GLES3.
		
		HvrActors using PointBlend are not rendering.
			The PointBlend render method does not work on some older mobile devices. It is recommended to use PointSprite for Mobile apps.

		HvrRender fails to load Standard shaders
			There is a known issue that on some devices, that when the 'Split Application Binary' option is enabled, the HvrRender component may not be able to load the Standard shaders. Go to 'Edit/Project Settings/Player' and make sure that the option 'Split Application Binary' is not checked.

	Android - DayDream
		The current release of the Unity Editor for DayDream ( 5.4.2f2-GVR13 ), will not use the AndroidManifest.xml file that we provide within the plugin. This means the hvr frames will not be extracted or read from the devices storage upon installing the build.

		It appears as though this build of the Unity Editor has a bug where it will not use and AndroidManifest.xml file that is not located at this specific location `project_name/Assets/Plugins/Android/AndroidManifest.xml`

		Until this is fixed within Unity, we recommend copying the AndroidManifest file from this location `8i/core/platform support/android/plugins/AndroidManifest.xml` to `project_name/Assets/Plugins/Android/AndroidManifest.xml`

Writing Custom HvrActor shaders
----------------------------
	When using the 'Standard' rendering mode for HrvActors, there is a slot where a material may be assigned.
	
	When writing custom shaders, you should make sure your 'Cull' shader parameter is set to 'Front'.
	
	**Culling Settings**
		'Off'
			It will look correct, but any transparency would have alpha applied twice.

		'Back'
			Since the mesh that the HvrActor uses is a cube based on the bounds of the HvrAsset, if the camera entered the bounds of the actor, the actor will dissapear as the backfaces of the mesh will not be rendered.

		'Front'
			Effectively draw onto the backfaces of the mesh and looks as expected.

Rendering Issues when using VR
------------------------------

	If when using a Vive, if the actors do not render or there is a upside down and white copy of the world visible in the headset the issue may be VSync being enabled.

	Fix:
		Go to build QualitySettings 'Edit/Project Settings/Quality and make sure that all Quality Settings have the 'V Sync count' option set to 'Don't Sync'.

Cannot create HvrActor
----------------------

	Possible Fixes:
		- Check that the plugin was fully extracted from the '8i Unity Plugin'.
		- Make sure the Unity version is compatible with this version of the plugin.
		- Check the console to see whether there are any errors blocking Unity from compiling.
