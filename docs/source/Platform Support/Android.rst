Android Support
===============

Building for Android
--------------------

Android is similar to desktop systems in that .hvr files are read from disk when being used to play a HvrActor. The Android HVR playback system expects that all static data is stored in a directory named “8i” in the devices external public storage. There are two different ways you can get .hvr files into the correct location for playback on your Android device.

**Build External Assets Folder (manual copy)**

Under the “8i” menu in Unity, you can use the “Build External Assets Folder” to build the required “8i” folder (full of .hvr files) and then copy this folder directly to the devices external public storage yourself. You can do this by plugging your device into a computer, and accessing the device’s file system. The public directory should contain other folders such as “Movies”, “Media”, “Music”, “Download” and others.

**Build and Run (Assets Packed)**

Under the “Android” sub-menu of the “8i” menu in Unity, there is an option to “Build and Run (Assets Packed)”. This will create an APK that contains all of your data, and will add an “unpacking” scene to the project, which populates the “8i” external public folder as required whenever your application is opened. Please note that if your project uses a large amount of data, Unity may fail to build a packed APK.

It is suggested that you use “Build and Run (Assets Packed)” for the first build after you have added a new asset to a scene (or are distributing your APK). You should otherwise use Unity’s standard build system. Once an asset has been unpacked, it will remain unpacked and accessible during future runs and builds of the application. Uploading an APK with packed assets to a device will take significantly longer than uploading an APK produced by the standard Unity build system (as the asset packed APK will be much larger).

Performance on Android
----------------------

Android performs much slower than desktop systems. It is recommended that hvr frames with point counts of 600k or less are used, with the recommended point count being around 300k.

It is recommended to use the ‘Direct’ HvrRender render method on Android as it is the best performing renderer.

.. note::
    We are aware of the APK size limits imposed by the Google Play Store. Support for .obb files is likely to be added in the future.