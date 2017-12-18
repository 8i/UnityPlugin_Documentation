Android
=======

Building for Android
--------------------

When building for Android, a custom build step must be used.

This can be found under the 8i/Android drop down menu at the top of the Unity Editor window.

Android is similar to desktop systems in that .hvr files are read from disk when being used to play a HvrActor. The Unity Plugin provides support to export .hvr data using an OBB file, and then unpack this data into the correct location within the app's internal storage. 

Hvr data cannot be read from disk while packed in the OBB. They need to be unpacked and written to the app's internal storage. The Unity Plugin provides a helper scene which does this. The scene is called "HvrUnpackingScene", and can be found under "8i/core/platform support/android/scenes/". By making this scene the first scene in the editor build settings (i.e. it will be launched when the app is launched), it will automatically unpack the assets, and then load the next scene.

"HvrUnpackingScene" uses the "LoadingSceneManager" class to unpack the data from the built OBB file. This class can be easily modified if any project specific changes are required.

**Custom Build Menu**
	**Build**
		This step will copy any hvr data that is required by the project into the StreamingAssets directory and then build the project to a specified location.

		Once the build step is complete, the files that were copied to the StreamingAssets directory will be cleared in order to reduce project bloat.


	**Build and run**
		Same as the 'Build' step, but will attempt to run the build on any attached devices once complete.


	**Prepare Assets for Build**
		This is a helper utility which will cpoy any required hvr data to the project's StreamingAssets folder, but will not build the project.

		Once this step is complete, the project can be built again via the standard Unity build process. There is no need to run the "Prepare Assets for Build" option again unless any new hvr data is required or has been removed from the build.

.. note::
	The Google Play Store imposes a size limit of 100mb for APK files uploaded for distribution. To allow larger data to be shipped with an APK, Android supports OBB files, also known as Application Expansion Files (`Read More`__.)
	
	Unity also supports these files, via a player setting called "Split Application Binary". This option will export many of the project resources to an OBB, rather than packaging them with the APK.
	
	In order to build succesfully with .hvr files in the project, this option must be turned on.  

.. note::
	Some devices do not seem to correctly allow the OBB file to be copied to the device when using the "Build and Run" option in Unity, and in some cases will silently fail to update the OBB when the project is built. If this occurs, the OBB file will need to be manually copied to the development device.
	
	So far only the Samsung Galaxy Note 5 has been observed with this issue. 


Performance
-----------

Performance Tips
	- Point Count
		As mobile platforms perform much slower than desktop systems it is recommended that hvr frames with point counts of 600k or less are used, with the recommended point count being around 300k.

	- Rendering Settings
		It is recommended to use the ‘Direct’ HvrRender render method on Android as it is the best performing renderer.

	- Render Method
		It is recommended to use the 'Point Sprite' render method in all cases. It is the best performing render method provided.
		The current alternative, 'Point Blend' does not work on some older devices, and is around twice as expensive to render.

.. __: https://developer.android.com/google/play/expansion-files.html
