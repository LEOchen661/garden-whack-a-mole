# Garden Whack-a-Mole (Camera Two-Player Edition)

A camera-interactive whack-a-mole game built on MediaPipe Hands. Two players each raise one
hand; the index fingertip acts as the pointer. Tap a popping mole for +1 point; avoid the
bomb mole (-5 points). One round lasts 30 seconds, with a light background soundtrack and hit
/ explosion sound effects.

## Features

- Real-time hand tracking in the browser (MediaPipe Hands, on-device, no upload)
- Two-player mode: red cursor for hand 1, blue cursor for hand 2
- 9-hole grid; moles rise at random intervals, 30% chance to be a bomb
- Score +1 on mole, -5 on bomb; 30-second round with end-of-round score
- Background chords and hit/explosion sound (Tone.js)
- Mirrored camera preview at low opacity behind the board

## Tech stack

- HTML / CSS / vanilla JavaScript (single page, no build step)
- MediaPipe Hands (`@mediapipe/hands`, `camera_utils`)
- Tone.js for audio
- GitHub Pages deployment

## Run locally

Just open `index.html` in a browser (Chrome / Edge recommended) and click
**启动摄像头并开始**, then allow camera permission. On HTTPS or localhost the camera works
directly; opening via `file://` also works in Chrome / Edge.

## Deploy

Push to GitHub and enable **Settings → Pages → Deploy from branch → main / (root)**; the site
is served at `https://<username>.github.io/<repo>/`.

## Notes

- Camera video is processed locally in the browser; nothing is recorded or sent to a server.
- If the camera is occupied by another app (Zoom, OBS, another tab), close it and retry.
