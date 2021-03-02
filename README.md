# Salesforce Voxelhoxel

This is a Salesforce managed package containing a Tab with a Voxel game like [Voxelhoxel](https://voxelhoxel.glitch.me/).

## No way!

Currently (March 2021) the Lightning Locker Service prevents rendering image textures in WebGL.
Everything in the locker service is wrapped into a virtual DOM, so there is no native "Image" object which
the Texture object of THREEJS can use.

Even when you set the texture data directly with DataTexture, THREEJS uses an Image internally to render it onto the
WebGL context. And this does not work with the locker service!

So, THREEJS: YES but textures: NO! Damn it!