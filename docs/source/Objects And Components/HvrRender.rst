HvrRender
===========

In order to render HvrActors a HvrRender component must be attached to a Camera.

There are three different render modes that the HvrRender component can be set to. While Standard is the default and recommended mode, there are two others which each have different properties and performance costs.

How to Create
-------------
1. Select the main rendering camera in the scene
2. In the Inspector click 'Add Component'
3. Type in HvrRender into the search box
4. Click 'HvrRender' in the results to add it to the camera


Rendering Modes
---------------

Standard
^^^^^^^^

**How it renders**

Renders the scene in multiple passes, where it renders each actor that is visible one by one.

This allows for a lot of customization as each HvrActor can have unique shaders and be color-graded individually.


Direct
^^^^^^^^

**How it renders**

Rendering the scene in a single pass by rendering directly into the framebuffer.
