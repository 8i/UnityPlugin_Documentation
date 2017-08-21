Troubleshooting
===============

HVR Actors are not rendering
----------------------------
**The Graphics API may not be supported**
Windows
	The Graphics API may not be supported Go to ‘Edit/Project Settings/Player’ and make sure that the PlayerSettings ‘Graphics API for Windows’ is set to either DirectX11 or OpenGL2. These are the only supported graphics APIs at this time.

Android
	The Graphics API may not be supported. Make sure that under the PlayerSettings that the targeting GraphicsAPI is GLES3 and that your device supports GLES3. Under the PlayerSettings ‘Split Application Binary’ may be enabled. There is a known issue that on some devices, that when the ‘Split Application Binary’ option is enabled the HvrRender the shaders may not load correctly from the resources. Go to ‘Edit/Project Settings/Player’ and make sure that the option ‘Split Application Binary’ is not checked.

Android - DayDream
	The current release of the Unity Editor for DayDream ( 5.4.2f2-GVR13 ), will not use the AndroidManifest.xml file that we provide within the plugin. This means the hvr frames will not be extracted or read from the devices storage upon installing the build.
	It appears as though this build of the Unity Editor has a bug where it will not use and AndroidManifest.xml file that is not located at this specific location `project_name/Assets/Plugins/Android/AndroidManifest.xml`

	Until this is fixed within Unity, we recommend copying the AndroidManifest file from this location `8i/core/platform support/android/plugins/AndroidManifest.xml` to `project_name/Assets/Plugins/Android/AndroidManifest.xml`


Rendering Issues when using VR
------------------------------

If when using a Vive, if the actors do not render or there is a upside down and white copy of the world visible in the headset the issue may be VSync being enabled.
Go to build QualitySettings ‘Edit/Project Settings/Quality and make sure that all Quality Settings have the ‘V Sync count’ option set to ‘Don’t Sync’.

Cannot create HvrActor
----------------------

- Check that the plugin was fully extracted from the ‘8i Unity Plugin’.
- Make sure the Unity version is compatible with this version of the plugin.
- Check the console to see whether there are any errors blocking Unity from compiling.