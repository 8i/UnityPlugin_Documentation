Quick Start
===========

Using Unity
-----------
If you’re brand new to Unity then there are some excellent tutorials for learning the interface and it’s features here 
https://unity3d.com/learn/tutorials

For VR development, there are some great tutorials here
https://unity3d.com/learn/tutorials/topics/virtual-reality

Creating a scene with the 8i Unity Plugin
-----------------------------------------
1. Create a new Unity Project.
2. Install the 8i Unity Plugin into your Unity Project.
3. Create a new folder within your Unity Project.
4. Copy the hvr frames you wish to use into the folder.
5. Right click in the Unity Hierachy and select '8i/Create HvrActor'
6. From the Unity Hierachy, drag the folder that was created earlier into the 'data' slot on the HvrActor. The data you chose will now be visible in the Unity Editor Scene View.
7. In the Unity Hierachy, select the 'Main Camera' object.
8. At the bottom of the inspector click 'Add Component' and search for "HvrRender". Select it and press enter.
9. Position the 'Main Camera' in front of the HvrActor.
10. Press the 'Play' button in the UnityEditor.

The HvrActor should now be visible in the Unity Editor Game View.

If the HvrActor or HvrRender components do not appear in the Unity Menus, please double check the installation instructions or the Troubleshooting section of this documentation. 

Creating a Build with the 8i Unity Plugin
-----------------------------------------
1. Follow the 'Creating a scene' steps above.
2. Save your scene.
3. Open Build Settings window under 'File/Build Settings...'.
4. Click the 'Add Open Scenes' button on the right of the window.
5. Click the 'Build and Run' and follow the onscreen prompts and select your build location.
 
Unity will now compile the project and create an exe. If it does not, please check the Troubleshooting section of this documentation. 
