# The Loudest WER! · A little room, a little band

**Local MVP · Desktop-first · HTML/CSS/JavaScript · Web Audio API**

The Loudest WER! is a pixel-pet music playground. Adopt a tiny Halloween band or create a pet from a photo, then arrange a song together. The website runs without a build step or account.

## Run locally · 本地运行

1. Open this folder in Terminal.
2. Run `python3 -m http.server 8000`.
3. Open `http://localhost:8000/`.
4. Click **Play together** once to enable browser audio.

## Pages · 页面

- `index.html` — interactive pixel pet home, automatic local-time mood, Sunset/Night selection, and a pull-cord theme switch.
- `pets.html` — create a pet from a photo, record/upload a voice, preview the pixel effect, and adopt the Pumpkin Band.
- `studio.html` — choose pets and scenes, arrange rhythms, adjust sound, play/pause, and save a session.
- `collection.html` — reopen, share a local session link, or remove saved sessions.
- `gallery.html` — standalone character and sound gallery.

## Current MVP behavior · 初版功能

- The room follows local time: Sunset 06:00–18:59 and Night 19:00–05:59. Pulling the cord switches directly between Sunset and Night; hovering or focusing it reveals a warm glow. Mystery Cat, Orange Cat, and White Cat use matching transparent sprites from `assets/pets/` for each theme, aligned over the cats in the wallpaper. Click a cat to enlarge it slightly in place and hear its call; click again to return it to normal size. Use Arrange / 调整位置 to drag the three cats; positions save separately for Sunset and Night in this browser, and Reset / 恢复默认 resets the current theme. The monitor stays as part of each wallpaper, without a separate overlay; use Start Playing / 开始一起演奏 to open Music Studio. The top navigation stays visible while scrolling.
- The three starter characters are Pumpkin Cat, Ghost Cat, and Bat Cat. The adoption shelf also includes the other built-in pets.
- Photo uploads are turned into a small pixelated preview in the browser. This is a visual pixel effect, not AI cutout or background removal.
- Pet voices can be recorded for up to 8 seconds or uploaded as a short clip. Studio applies browser audio filters and pitch changes to make an electronic tone.
- Music sessions, adopted pets, and custom pet details are saved in this browser's local storage. They do not sync across devices. Clear browser data and local saves may be lost.
- Share copies a local studio URL. It does not publish the song or upload it to a server.

## Replaceable assets · 可替换素材

For the concise bilingual workflow and asset map, see the [Team Guide / 团队协作与素材替换说明](docs/团队协作与素材替换说明.md).

- Pet PNGs: `assets/pets/` (`cat.png`, `dog.png`, `bird.png`, `bunny.png`, `frog.png`, `fox.png`). Use transparent PNGs where possible.
- Music samples: `assets/sounds/` (short WAV examples).
- Studio stage background: `assets/backgrounds/`; if no image is present, the pixel scene is drawn by `app.js`.
- Home uses `assets/backgrounds/home-night.png` and `assets/backgrounds/home-sunset.png` as full-page desktop wallpapers. The background artwork includes the room computer; separate computer PNG overlays are not used. Local time or the pull cord switches wallpaper, logo, navigation accent, action buttons, and cat sprites together. Replace each theme's three cat sprites in `assets/pets/`, keeping transparent margins and matching the painted cats' scale and position. Replace the two wallpaper files in `assets/backgrounds/`; replace the matching `logo_*` files in `assets/wer-christmas-ui/`. The six displayed `button_*_uniform.png` files use a 300 × 100 source canvas; keep that size when replacing them. On narrow screens, the room returns to an in-flow scene panel so the whole illustration and its pet hotspots remain usable.

## Main code · 主要文件

| File | Purpose |
|---|---|
| `index.html`, `home.js` | Home room and light/time interaction |
| `pets.html`, `pets.js` | Pet photo/voice input, adoption, local pet shelf |
| `studio.html`, `app.js` | Music editor and playback |
| `collection.html`, `collection.js` | Saved sessions |
| `store.js` | Browser-local pets, settings, and music data |
| `theme.js` | Shared automatic Sunset/Night mode |
| `style.css`, `pixel-ui.css`, `experience.css` | Layout, pixel components, and page styling |

This is a browser-local prototype; it has no account system, cloud sync, AI image generation, public music hosting, or server-side storage.

The current product direction is recorded in [`SPEC.md`](SPEC.md).
