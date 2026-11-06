# A Song for Someone Who Matters and a Model Lesson

A single-page, self-contained teaching page that helps a smart friend who is **not** in this
course tell three AI model families apart: **LLMs**, **multimodal models**, and **diffusion
models**. It also carries a short, honest appendix on how the accompanying song was made.

Open `index.html` in any modern desktop browser. There is no build step, no framework, no
server and no external request — one file, fully offline.

---

## Opening notes

**What the page is for.** The core question it answers is: *given a task, which family is the
core of what you need, and which are helpers?* Each family gets a concrete mechanism
explanation (tokenisation and next-token prediction; patching and projection for other
modalities; forward noising and reverse denoising) rather than a product tour.

**Two modes.** The page is built for both required situations:

- **Self-paced** — read and click straight through. Each demo works on its own.
- **Teach mode** (button, top right) — reveals short blue presenter cues: when to stop, what
  to ask, what a good answer sounds like. Useful when you are sitting next to the learner.

**Interactions.** Four clickable elements plus a quiz:

1. **Next-token loop** (LLM) — click candidates and watch a sentence grow one token at a time.
2. **Image → patches → vectors** (multimodal) — a slider changes the patch grid; the chips
   show each patch reduced to numbers.
3. **Denoising step slider** (diffusion) — drag from pure noise to a clean image, or press
   *Run sampling* to animate it.
4. **Three-question quiz** with a written explanation after every answer.

**Honesty about the demos.** The next-token percentages are hand-set, and the denoising
animation is a simulation — neither is a measurement of a real model. Both say so on the page.
The patch demo is real image data but collapses each patch to an average colour, which is
labelled too.

**AI disclosure.** The page states in its footer that the text and code were written with AI
assistance and that the cover art and music are AI-generated.

---

## Known limitations

1. **The demos illustrate, they do not measure.** No real model is running in the browser.
   The probabilities and the denoising steps are constructed to show the *shape* of the
   process. A learner who reads the labels carefully cannot mistake them for measurements,
   but a learner who skips the captions could.
2. **The patch demo loses almost everything.** Reducing a patch to its average colour throws
   away the texture and edges that a real vision encoder keeps. It shows the *step*
   (picture → grid of vectors) clearly and the *content* of the vectors badly. This is
   labelled, but it is the weakest of the three demos conceptually.
3. **Depth is traded for breadth.** Three families in one page means each gets roughly a page
   of text. Diffusion sampling maths is described qualitatively, not derived; the guidance
   mechanism is one paragraph.
4. **English with Chinese summaries.** The main text is English; each section ends with a
   short Chinese summary for readers who are more comfortable in Chinese. The Chinese
   summaries are condensed and are not a full translation.
5. **Desktop-first.** It works on a phone, but the two canvas demos are designed around a
   laptop screen and a mouse. The quiz and the reading flow are fine on mobile.
6. **Not every product works this way.** The page says this explicitly. The three families are
   mainstream recipes, and named commercial products often mix or hide them.
