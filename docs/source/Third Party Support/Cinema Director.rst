Cinema Director
===============

Cinema Director is a third party plugin for Unity. It is a powerful tool for creating cutscenes within Unity.
It is available on the Unity Asset Store for purchase.

Links
`Website <http://cinema-suite.com/>`_.
`Unity Store <https://www.assetstore.unity3d.com/en/#!/content/19779>`_.

**Download**

8iUnityPlugin 0.4.2f1
* CinemaDirector 1.4.5.2 `Download <https://drive.google.com/open?id=0B2RPRDuZy4rIejdFRURrRDhETm8>`_

**Installation**

Extract the ‘CinemaDirector’ folder from the zip into your project located under '8i/Integrations'

**Usage**

1. Open the ‘Creator’ window for Cinema Director by going to ‘Window/Cinema Suite/Cinema Director/Create Cutscene’
2. Set the Actor Track Groups to ‘1’
3. Drag the GameObject that has a HvrActor component attached into the ‘Actor 1’ slot
4. Press ‘Create Cutscene’
5. If it is not visible already, open the Director window by going to ‘Window/Cinema Suite/Cinema Director/Director’
6. In the Director window click the ‘+’ icon next to ‘Actor 1 Group’ and add a ‘Actor Track’
7. Click the ‘+’ button next to the ‘Actor Track’ and select ‘8i/Play Hvr’
8. Click the play symbol in the Director window to preview the cutscene.


**How to use HVR Actor Fade**

1. Open the ‘Creator’ window for Cinema Director by going to ‘Window/Cinema Suite/Cinema Director/Create Cutscene’
2. Set the Actor Track Groups to ‘1’
3. Drag the GameObject that has a HvrActor component attached into the ‘Actor 1’ slot
4. Press ‘Create Cutscene’
5. If it is not visible already, open the Director window by going to ‘Window/Cinema Suite/Cinema Director/Director’
6. In the Director window click the ‘+’ icon next to ‘Actor 1 Group’ and add a ‘Actor Track’
7. Click the ‘+’ button next to the ‘Actor Track’ and select ‘8i/HVR Actor Fade’
8. In the hierarchy click the "Cutscene/HvrActorGroup/ActorTack/HVRActorFade" and you could moldify the start color/end color/firsttime/duration.
9. If you wish to do the alpha fade, please make sure "Rendering Mode" of your HVR Actor shader is set to "AlphaBlend"