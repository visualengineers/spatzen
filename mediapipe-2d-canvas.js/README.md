## Goal
A 2D hand-tracking application using MediaPipe Hands and HTML Canvas. A diagram follows the index fingertip and scales dynamically based on the hand's estimated distance from the camera.
MediaPipe is used only to get a source for different 3D positions.

## How to test it
- Open index.html in a browser, accept camera access and move a hand in the camera view.

## Technology used
- uses getUserMedia() to access webcam & display live video in HTML <video>
- places transparent HTML <canvas> over video using CSS positioning 
- uses MediaPipe hands to detect handlandmarks
- uess Canvas 2D API (getContext('2d')) to draw diagram on canvas

=> positioning and display of diagram done by canvas