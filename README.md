# Face As Numbers

Watch a face become a wall of numbers in real time.

**Live:** https://kanishk-saini-007.github.io/Face-As-Numbers/

## What it does

- Left panel: live webcam feed with face detection drawn on top (bounding box + all 68 facial landmarks).
- Right panel: the same frame re-rendered live as a dense wall of digits - each cell of the frame becomes a number, weighted by brightness, so the face emerges out of pure numerals.
- Bottom: the 128-dimensional face descriptor (the embedding vector the network computes for the detected face), ticking in real time.

Everything runs 100% in the browser. No server, no uploads - the video never leaves your device.

## How

- [face-api.js](https://github.com/justadudewhohacks/face-api.js) (vendored, MIT)
- SSD MobileNet v1 for detection, 68-point landmark net, ResNet-34 recognition net for the 128-D embedding
- Model weights vendored in `/models`, served straight from GitHub Pages
- Canvas for both the overlay and the numbers wall

## Run it

Open the live site, press **START CAMERA**, and allow camera access. No camera? Press **DEMO IMAGE** to run the whole pipeline on a bundled sample face instead.

## Credits

Built by [Kanishk Saini](https://github.com/Kanishk-Saini-007) - a computer-vision learning experiment. Demo face image is a test asset from the face-api.js repository (MIT).
