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
**Performance**

Bronze

**How it renders**

Renders the scene in multiple passes, where it renders each actor that is visible one by one. This allows for a lot of customization as each HvrActor can have unique shaders and be color-graded individually.

**HvrColorGrading support**

Allows individual color grading of HvrActors if the HvrActor ‘Unity Render Method’ is set to ‘Standard’.


Composite
^^^^^^^^
**Performance**

Silver

**How it renders**

Renders the scene in a single pass by compositing into the scene by using a fullscreen shader.

**HvrColorGrading support**

Supports color grading if the HvrColorGrading component is attached to same camera as the HvrRender component. Invididual HvrColorGrading components on HvrActors are ignored.


Direct
^^^^^^^^
**Performance**

Gold

**How it renders**

Rendering the scene in a single pass by rendering directly into the framebuffer.

**HvrColorGrading support**

Does not support color grading.