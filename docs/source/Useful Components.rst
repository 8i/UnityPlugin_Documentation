Useful Components
=================

PlayHvrActor
------------

Assigning an HvrActor to this component will trigger it to begin playing as soon as the scene loads.

TriggerHvrActor
---------------

By attaching this component to a GameObject that has a Collider and assigning a HvrActor, the HvrActor will begin playing when the Collider is hit by any collidable object.

HvrActorProjectorShadow
-----------------------

Can be used in conjunction with a Projector component to project a texture onto a surface based on the bounds of an HvrActor. This is useful for creating blob shadows.

HvrActorAudioSourceSync
-----------------------

This component has two slots, one for an Animation and one for an HvrActor. Filling both these slots will cause the AudioSource's playback to match the HvrActor.

Create by

1. Select (or create) a Unity GameObject
2. Click on ‘Add Component’ in the inspector
3. Go to ‘8i/HvrActor Audiosource sync’
4. Slot the HvrActor and Audiosource into the component. From now on the audio source will match the playback time of the HvrActor.

.. note::
	The HvrActorAudioSourceSync does not take an audio clip itself as a value. It expects the audiosource to have an audioclip assigned. Once you have assigned a Audiosource and HvrActor, you will not need to manage this component - If the actor is playing, the audio source will be playing. If the AudioClip assigned to the AudioSource is shorter than the HvrAsset’s duration it will play as long as it can, if it is longer it will stop once the HvrActor stops playing.

HvrActorAnimationSync
-----------------------

This component has two slots, one for an Animation and one for an HvrActor. Filling both these slots will cause the Animation's playback to match the HvrActor.

Create by

1. Select (or create) a Unity GameObject
2. Click on ‘Add Component’ in the inspector
3. Go to ‘8i/HvrActor Animation sync’
4. Slot the HvrActor and Animation into the component. From now on the animation will match the playback time of the HvrActor.