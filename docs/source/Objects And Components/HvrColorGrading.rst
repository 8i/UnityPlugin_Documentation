HvrColorGrading
===============

This component allows the color grading to be applied to the rendering of HvrActors.

How to Create
-------------
1. Select your HVRActor from the Hierachy panel
2. Below the HVRActor component click the 'Add Component' and search for 'HVRColorGrading'
3. Add it by highlighting it in the 'Add Component' window and pressing Enter, or clicking it.

Usage
-----

Adjusting the values and sliders of the this component will affect the look of the HvrActor it is attached to.

.. note::
    The 'Direct' render mode available on HvrRender and HvrActor are not compatible with this component.

.. note::
    When using HvrRender's 'Composite' mode. The HvrColorGrading component can be attached to the Camera GameObject and used to grade the look of the HvrActors rendered by that camera.
