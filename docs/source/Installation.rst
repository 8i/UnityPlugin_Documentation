Installation
=========

Download
--------------------------
All the files you need to access, including the plugin, example content and documentation can be found in the dropbox folder that was shared with you.

Adding the 8i Unity Plugin
--------------------------

1. Ensure you have Unity 5.4.0 or greater installed
2. Create a new Unity Project
3. Extract the ‘8i’ folder from the plugin zip file into your project

  
Updating the 8i Unity Plugin
--------------------

1. Close the Unity Editor.
2. Completely remove the previous version by deleting the ‘8i’ folder from your project.
3. Extract the ‘8i’ folder from the plugin zip file into your project

It is very important to close the Unity Editor before updating the plugin. This is required as the Unity Editor will lock the native dlls from being overwritten or deleted while they are in use. This can cause issues where the plugin can get into a state where the native dll does not get updated and the plugin will be in an unstable state.
