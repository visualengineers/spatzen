# A-Frame
This folder is a very simple test for the A-Frame 3D-Web-Framework (https://github.com/aframevr/aframe#builds)

## Goal
A marker-based augmented reality application using A-Frame and AR.js. A virtual diagram is displayed on a Hiro marker and follows its position and orientation.

## How to test it
- Open index.html in a browser, accept camera access and find a hiro marker to display information on top. 

## Technology used
- Uses A-Frame to create and render a virtual 3D scene in the browser
- uses AR.js to access the webcam and detect a Hiro marker in the camera view
- displays live camera feed behind virtual 3D scene
- uses <a-marker> entity (a-frame) to anchor virtual objects to detected marker
- uses <a-image> entity to display SVG diagram as textured plane
- positions and rotates diagram so it lies flat on the marker's surface
- AR.js continuosly updates marker's position and orientation to keep diagram aligned

=> positioning and display of diagram done by AR.js => virtual scene is aligned by marker