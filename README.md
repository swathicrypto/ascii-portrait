# ASCII Portrait — *Swathi Prakash*

An interactive, scroll-driven graduation portrait. It begins as raw `010101`
binary "typing" itself onto the screen, then evolves — through Python source,
the vocabulary of AI governance, and my own name — until it finally dissolves
into the real graduation photograph.

The characters that draw the portrait aren't random. They're pulled from the
things that made up the degree: the code, the research language, the name on
the diploma.

> **Live demo:** https://swathicrypto.github.io/ascii-portrait/

<!-- Optional: add a screen recording or screenshot here -->
<!-- ![preview](preview.gif) -->

---

## The layers

As you scroll, the same portrait is redrawn from a different alphabet:

1. **Raw binary** — `010101…` the machine underneath
2. **Source code** — Python, how the models are built
3. **AI governance** — fairness, explainability, robustness, accountability, audit
4. **Name & degree** — `SWATHI PRAKASH · UPENN · PENN ENGINEERING · COMPUTER SCIENCE`
5. **Graduation** — the ASCII dissolves into the real photograph

## Interactions

- **Scroll** — moves through the five layers
- **Move the mouse** — left/right changes character density (chunky ↔ fine)
- **Click the portrait** — reveals / hides the real photo
- **Upload** or **drag-drop** an image — swap in any photo live
- **Color** — toggle image-tinted vs. terminal green
- **Invert** — flip between full-figure (dark = dense) and glowing-subject (bright = dense)
- **Replay** — restart the typing intro
- **Record video** — auto-plays a ~20s cinematic run and saves it as a video
- **Save frame** — export the current frame as a PNG

## Posting it on LinkedIn

LinkedIn can't embed a live page, so post the **video** and link to the live
demo in the caption:

1. Open the page (locally or the live link) with your `portrait.jpg` in place.
2. Click **● record video** — it plays the full sequence and downloads a
   square 1080×1080 clip (`.mp4` in recent Chrome/Edge — ideal for the feed).
3. Create a LinkedIn post, attach the video, and drop the live-demo link in the
   caption so people can try it themselves.

> Tip: if your browser saves a `.webm` instead of `.mp4`, either record with the
> latest Chrome/Edge, or use Windows **Game Bar** (`Win + Alt + R`) to screen-
> record the run — that produces an `.mp4` directly.

## Run it locally

It's a single file with no build step. Just open `index.html` in a browser.
For image loading to work reliably, serve it over a local server:

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000
```

## Use your own photo

Drop a file named **`portrait.jpg`** next to `index.html` and it loads
automatically. (If it's missing, a placeholder portrait is shown.)

## Make it yours

Everything worth editing lives at the top of `index.html`:

- **`CONFIG`** — your name, image path, density ramp, and **`focus`** (zoom /
  crop center) plus **`autoContrast`** / **`gamma`** for tuning dark photos
- **`LAYERS`** — the text each layer is drawn from. Paste in snippets of your
  résumé, thesis, or actual code and they'll form the image.

> **Framing tip:** if your face sits off-center or too far away, nudge
> `CONFIG.focus` — raise `zoom` to crop in tighter, and shift `x` / `y`
> (0–1) to re-center on your face.

## Tech

Plain HTML5 Canvas + vanilla JavaScript. No dependencies, no framework.

---

*Built to mark graduating from the University of Pennsylvania.* 🎓
