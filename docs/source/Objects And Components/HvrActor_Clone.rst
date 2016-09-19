HvrActor_Clone
===========

This component allows you to clone a specified HvrActor and render copies of it with a reduced performance cost. The performance savings are on the CPU and come from letting the clone share the source’s HvrAsset and reducing the total disk read and file decompression. Three clones are still just as expensive to render as three regular HvrActors.

How to Create
-------------
1. Right click in Unity Scene Hierarchy
2. Go to ‘8i/Create HVR Actor Clone’
3. Assign the ‘Source Actor’ by dragging an HvrActor into the slot, or searching the scene by clicking on the icon next to the slot.


Parameters
----------

**Source Actor**
Slot for assigning the HvrActor to clone.

**Actor Render Method**
Functionality matches HvrActor.

**Asset Render Method**
This functionality is disabled, as the source HvrActor defines this setting.

**Occlusion Culling**
Functionality matches HvrActor.