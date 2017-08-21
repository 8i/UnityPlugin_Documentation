HvrActor3DMask
===============

This components allows you to mask sections of an HvrActor in 3D space.

**Instructions**
  1. Attach a HvrActor3DMask component to the HvrActor you wish to mask.
  2. Create a new GameObject.
  3. Attach a HvrActor3DMaskObject to the new GameObject.
  4. Position and scale the HvrActor3DMaskObject as desired.
  5. The HvrActor will now no longer be visible within the volume of the HrvActor3DMaskObject.

Limitations
  - This effect is essentially done in 2D. This means masking a hand in front of a face will remove the hand, but the face will. See the example scene for a demonstration of this.
