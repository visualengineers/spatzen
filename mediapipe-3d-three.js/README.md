## Goal
A hand-tracking AR application using Three.js and MediaPipe Hands. A 3D diagram follows the user's hand, adapting its position, rotation, and size in real time.
MediaPipe is used only to get a source for different 3D positions.

## How to test it
- Open index.html in a browser, accept camera access and move a hand in the camera view.

## Technology used
- uses getUserMedia() to access webcam and display live video in an HTML <video> element
- places transparent WebGL canvas over camera feed to render virtual 3D content
- uses MediaPipe Hands to detect hand landmarks from each processed video frame
- uses Three.js to create 3D scene with camera and textured plane (THREE.Mesh)
- loads diagram as texture using THREE.TextureLoader
- calculates daigram's position & rotation from selected handlandmarks; scale based on palm width
- continuously renders 3D scene over live camera image 

=> positioning and display of diagram done by canvas
