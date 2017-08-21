Quick Start
===========

Create
------

    If you are brand new to Unity then there are some excellent tutorials for learning the interface and it’s features here 
    https://unity3d.com/learn/tutorials

    1. Create a new Unity Project.
    2. Add the 8i Unity Plugin into your Unity Project.
    3. Create a new folder within your Unity Project.
    4. Copy the hvr frames you wish to use into the folder.
    5. Create a `HvrActor` by right clicking in the Hierachy and select '8i/Create HvrActor'
    6. Drag the folder that was created earlier into the 'data' slot on the `HvrActor`.
    7. Select the `Main Camera` object from the Hierachy
    8. At the bottom of the inspector click 'Add Component' and search for "HvrRender". Click it to add it to the `Main Camera`.
    9. Position the `Main Camera` in front of the HvrActor.

    The HvrActor should now be visible in the Unity Editor Game View.

    If the HvrActor or HvrRender components do not appear in the Unity Menus, double check the installation instructions or the Troubleshooting section of this documentation. 

Build
-----
    1. Follow the 'Creating a scene' steps above.
    2. Save the scene.
    3. Open Build Settings window under 'File/Build Settings...'.
    4. Click the 'Add Open Scenes' button on the right of the window, or drag the scene from the 'Project' window of the Unity Editor.
    5. Click the 'Build and Run' and follow the onscreen prompts and select your build location.
 
    Unity will now compile the project and create an exe. If it does not, check the Troubleshooting section of this documentation. 


VR
--
    The 8i Unity Plugin fully supports VR rendering.

    To enable VR for your Unity Project
        1. Open the 'Player Settings' window from 'Edit/Project Settings/Player'.
        2. Tick the 'Virtual Reality Supported' checkbox.
        3. From the new list, make sure the target headset you wish to use is listed. If it isn't, add it by clicking the + icon.

    If you are new to VR development in Unity, there are some great tutorials here:
    https://unity3d.com/learn/tutorials/topics/virtual-reality

    If you encounter any issues getting VR working in your Unity Project, please consult the Unity Manual
    https://docs.unity3d.com/Manual/VROverview.html

