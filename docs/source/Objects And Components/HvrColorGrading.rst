HvrColorGrading
===============

This component allows the user to apply color grading to the rendering of HvrActors.

To color grade a single HvrActor, just add a HvrColorGrading component to the same GameObject and set its render method to ‘Standard’. Keep in mind that if the rendering camera’s HvrRender’s render method is not set to ‘Standard’ this component will be ignored.

To color grade all the HvrActors in the scene, add a HvrRender and HvrColorGrading component to a Camera and set the HvrRender render mode to ‘Composite’.