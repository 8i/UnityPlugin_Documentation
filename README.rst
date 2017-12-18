8i Unity Plugin
===============

The 8i Unity Plugin is a plugin for the Unity game engine.
It adds the ability to render and interact with hvr content.

Dev portal
==========

This repository is pulled and built as part of the dev portal section of 8i.com.

See the https://github.com/8i/8i-com/ repo for more about that.

To test this flow, you will need pip(https://github.com/pypa/pip) to install the build dependencies.

pip install -r requirements

Once you have these installed you can build the docs using sphinx.

The current build approach requires that this repo is checked in within the root folder of the 8i-com repo.
It depends on templating and stylesheets from that repo.
This was a quick solution, and it really should be thought through about how to do this better.
8i-com/
  - UnityPlugin_Documentation
  - UnrealPlugin_Documentation
  - argo-android
  - argo-ios

In order to test the generated docs, you should build and run the 8i-com repo.
See the README in https://github.com/8i/8i-com/ for instructions

Unfortunately running the 8i-com repo depends on having all of the documentation repo's available.
You will need to checkout all of the unity, unreal, android and ios repo's
See .buildkite/build.sh in the 8i-com repo to see how all of the repos are checked out for release builds.

There is most definitely a more efficient/better way to do this, but deadlines won ¯\_(ツ)_/¯.

TODO should be able to docker-compose the latest docker image from quay?
And then update the documentation repos as required???
