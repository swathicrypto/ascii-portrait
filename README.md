# ASCII Portrait — *Swathi Prakash*

An interactive, scroll-driven graduation portrait. It begins as raw `010101`
binary "typing" itself onto the screen, then evolves (through Python source,
the vocabulary of AI governance, and my own name) until it finally dissolves
into the real graduation photograph.

The characters that draw the portrait are pulled from the
things that made up the degree: the code, the research language, the name on
the diploma.

> **Live demo:** https://swathicrypto.github.io/ascii-portrait/

![preview](ascii-boomerang.gif)

---

## The layers

As you scroll, the same portrait is redrawn from a different alphabet:

1. **Raw binary** : `010101…` the machine underneath
2. **Source code** : Python, how the models are built
3. **AI governance** : fairness, explainability, robustness, accountability, audit
4. **Name & degree** : `SWATHI PRAKASH · UPENN · PENN ENGINEERING · COMPUTER SCIENCE`
5. **Graduation** : the ASCII dissolves into the real photograph

## Interactions

- **Scroll** : moves through the five layers
- **Move the mouse** : left/right changes character density (chunky ↔ fine)
- **Click the portrait** : reveals / hides the real photo
- **Photo** : toggle between the three graduation portraits
- **Color** : switch between full color and black & white
- **Replay** : restart the typing intro
- **Save frame** : snapshot the current view as a PNG

## Run it locally

It's a single file with no build step. Just open `index.html` in a browser.
For image loading to work reliably, serve it over a local server:

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000
```

## The photos

Three portraits live in the repo as **`portrait1.png`**, **`portrait2.png`**,
and **`portrait3.png`** — the **◇ photo** button toggles between them, each shown
whole in its original orientation. Swap in your own by replacing those files.

## Make it yours

Everything worth editing lives at the top of `index.html`:

- **`PHOTOS`** — the three image files
- **`CONFIG`** — your name, the density ramp, and the tone controls
  (`gamma`, `saturate`, `cellFill`) for how the portrait reads
- **`LAYERS`** — the text each layer is drawn from. Paste in snippets of your
  résumé, thesis, or actual code and they'll form the image.

## Tech

Plain HTML5 Canvas + vanilla JavaScript. No dependencies, no framework.

---

*Built to mark graduating from the University of Pennsylvania.* 🎓
