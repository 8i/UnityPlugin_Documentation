iOS
===

Building for iOS
----------------
When building for iOS, there are a few things to be noted.

* Use a Mac to generate the iOS build
* Switch the build target to iOS in 'Build Settings' dialogue
* In 'Player Settings' dialogue, uncheck 'Auto Graphics API', move and make sure 'OpenGL ES3' is on the top of Graphics API list. We don't support Metal at the moment specifically.

Performance
-----------

Performance Tips
	- Point Count
		As Android performs much slower than desktop systems it is recommended that hvr frames with point counts of 600k or less are used, with the recommended point count being around 300k.

	- Rendering Settings
		It is recommended to use the ‘Direct’ HvrRender render method on Android as it is the best performing renderer.

	- Render Method
		It is recommended to use the 'Point Sprite' render method in all cases. It is the best performing render method provided.
		The current alternative, 'Point Blend' does not work on some older devices, and is around twice as expensive to render.
