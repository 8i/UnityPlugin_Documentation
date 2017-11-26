HvrLight
========

HvrLight enables Light component to light HvrActors.

There's no options can be adjusted in HvrLight. All the parameters from Light component should reflect on HvrActors once HvrLight is attached, with a few limitations.

.. note::
	HvrLight only works when HvrRender's rendering mode is set to 'Standard'. In 'Direct' rendering mode, the HvrActors will always be fully lit no matter lights or HvrLights are applied or not.

How to Create
-------------
1. Select the light object of interest
2. In the Inspector click 'Add Component'
3. Type in HvrLight into the search box
4. Click 'HvrLight' in the results to add it to the light

Limitations
-----------
* HvrLights under directional light will not be able to cast shadows
* HvrLights under point light will have shadow artifacts prior to Unity 5.6
* Some mobile devices will have limited shadow casting abilities
* HvrActors receive shadows from other objects will not have soft-edged shadows