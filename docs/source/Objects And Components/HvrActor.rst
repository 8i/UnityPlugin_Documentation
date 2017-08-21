HvrActor
===========

This component acts most like Unity’s built in Mesh Filter component. Where instead of a mesh, it takes as input a folder from the Unity Project which contains .hvr frames.

How to Create
-------------
1. Right click in Unity Scene Hierarchy
2. Select ‘8i/Create HVR Actor’


Parameters
----------

**Data**

Slot which a folder containing .hvr frames can be dragged to from the Project.


**Actor Render Method**

The rendering method the actor will use to draw into the scene.

Options
    - Standard
        - Supports per-actor colour grading
        - Supports custom shaders
    - Direct
        - Faster than 'Standard'
        - Does not support colour grading
        - Does not support custom shaders
    
.. note::
    This setting will be overridden if the rendering camera’s HvrRender component is not set to ‘Standard’


**Asset Render Method**

The rendering method the HvrActor’s HvrAsset will render with.

Options
    - Point Blend
        - Renders the actor with smooth points which soften the look of the actor
    - Point Sprite
        - Renders the actor with hard edges.
        - Renders faster than PointBlend


**Occlusion Culling**

Whether when rendering the HvrActor the HvrRender should use Unity’s Occlusion Culling system to check whether the object is visible. A wireframe sphere will be drawn in the Editor SceneView to show the size and location of the bounding sphere which is used to check the visibility of the HvrActor.

Options
    - Occlusion Radius Offset
        - Allows you to offset the size of the bounding sphere radius.