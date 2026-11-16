# WebXR AR Diagram

## *Goal*

This project demonstrates markerless augmented reality using WebXR, Three.js, and WebGL. An SVG diagram is placed approximately 70 cm in front of the user when the AR session starts and remains at a fixed position in 3D space.

Standard iOS browsers do not support immersive WebXR AR directly. Therefore, **Needle Go** is used as an iOS App Clip that connects WebXR to Apple's ARKit. (Probably not necessary for Android devices)

## *How to test it for local development (iPhone)*

1. Start a local web server in the project directory:
   ```bash
   python3 -m http.server 8080
   ```
2. Open a second terminal and start an HTTPS tunnel:
   ```bash
   /Users/selina/Downloads/cloudflared tunnel --protocol http2 --url http://localhost:8080
   ```
3. Copy the generated `https://...trycloudflare.com` URL.
4. On an iPhone, open the following URL in Safari:
   ```
   https://appclip.needle.tools/ar?url=YOUR_HTTPS_URL/index.html
   ```
5. Launch Needle Go by scanning the QR Code, select "Web XR", start the AR session, and move the phone to observe the diagram.

Keep both terminal processes running while testing. The temporary tunnel URL may change when restarted.

## *How to test it (iPhone)*

1. On an iPhone, open the following URL in Safari: https://appclip.needle.tools/ar?url=https://visual-engineers.org/spatzen (replace 2nd url with updated url from github pages if necessary)
2. Launch Needle Go by scanning the QR Code, select "Web XR", start the AR session, and move the phone to observe the diagram.

Keep both terminal processes running while testing. The temporary tunnel URL may change when restarted.

## *Technology used*

- **WebXR Device API:** AR session and device pose tracking.
- **Needle Go / ARKit:** Enables the WebXR experience on iOS through an App Clip.
- **Three.js:** Creates and positions the virtual diagram.
- **WebGL:** Renders the SVG as a texture on a 3D plane.
- **Cloudflare Tunnel:** Makes the local development server accessible over HTTPS without deploying to GitHub. (necessary to test any local development on the phone)

The real-world camera view is provided by the AR session rather than being rendered manually as a video background.

## example url:
https://appclip.needle.tools/ar?url=https://continually-anderson-retrieve-metres.trycloudflare.com%2Findex.html&utm_source=chatgpt.com