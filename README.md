# MDK Debrief Generator
Create your own pre/post-game debriefings from MDK.

Renders text the way MDK does it — actual bitmap fonts pulled from the game data, actual mission backgrounds, actual teletype sound. Type something, watch it clack out letter by letter, export it as a GIF or PNG. Optional CRT Scanline effect(does not save with image). All 25 original briefing and debriefing texts are in the preset dropdown, including the cut debriefings.

## Running it
Double click "run_me.bat" to start a local server and load the app in your default browser. Be sure to close the console window when finished.
OR
Host it anywhere that serves static files — GitHub Pages, Netlify, Cloudflare Pages, or just `python3 -m http.server` locally, then go to `http://localhost:8000` in your browser. You need a local server because of how browsers handle GIF encoding — it won't work opened directly as a file.

## What's in here

```
index.html          — the whole app
assets/
  L1_MAP.png        — mission backgrounds (L1–L5)
  FONTBIG_sheet.png — spritesheet for the main display font
  FONTSML_sheet.png — spritesheet for the sidebar labels
  TELETYPE.wav      — typing sound
  SND_PUSH.wav      — button click
  gif.js            — GIF encoder
  gif.worker.js     — GIF encoder background thread
```

## Credits

Assets extracted from **MDK** (1997, Shiny Entertainment / Playmates Interactive). Fan project, not affiliated. Font decoding informed by [BuXXe's MDKTools](https://github.com/BuXXe/MDKTools), [brandonhare/mdk-parse](https://github.com/brandonhare/mdk-parse), and [Calinou's Godot reimplementation](https://github.com/Calinou/mdk).
