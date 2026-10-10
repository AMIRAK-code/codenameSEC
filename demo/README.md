# Overseer technical demo

- `overseer-demo.mp4`: 45-second, 1920×1080, 30 fps motion-graphics demo (H.264, silent).
- `index.html`: the same demo as a live player in the browser (play/pause, scrub, space bar). Every frame is a pure function of time, so the video is rendered from this page.
- `VOICEOVER.md`: optional narration timed to each scene.

## Re-render the video

Open `index.html#render`. It exposes `window.renderAt(t)` and sets `window.DEMO_READY` once the fonts have loaded. Capture a 1920×1080 screenshot for every `t = frame / 30` from 0 to 45, for example with Playwright, then encode the frames:

```sh
ffmpeg -framerate 30 -i frames/f%05d.jpg -c:v libx264 -crf 20 -pix_fmt yuv420p -movflags +faststart overseer-demo.mp4
```

Fonts (Bricolage Grotesque, IBM Plex Sans, JetBrains Mono) are under the SIL Open Font License. Three.js r128 is under the MIT license.
