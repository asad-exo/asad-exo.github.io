# asad-exo.github.io

My personal portfolio. View it here:
**https://asad-exo.github.io**

I'm Asad Shahab, a grad student in computer engineering at NYU Tandon. The site covers what I work on (AI agent security, game theory and deep learning), my main projects, my experience and how to reach me.

## How it's built

One static page, no framework and no build step. Everything is in `index.html`: the markup, the styles and a small script.

The look borrows from banknote printing: guilloché line patterns, serial numbers, stamps and perforated edges between sections. Most of it is drawn in code:

- **The line patterns** are hypotrochoids (spirograph curves) computed in JavaScript when the page loads and drawn as SVG.
- **The spirograph in the hero** is a canvas that draws a new pattern every few seconds. Moving your cursor over it nudges the pen.
- **The project demos** (the decoy monitor, the Sequence board, the knight, the waveform) are plain HTML and CSS animations.
- **The MNIST demo** steps through real denoising frames from my [MNIST Denoising](https://github.com/asad-exo/MNIST-Denoising) project.

The intro counter plays once per visit. Anyone who has reduced motion turned on in their system settings gets a still version of the page.

## Files

```
index.html               the whole site
assets/
  Asad-Shahab-CV.pdf     my CV, linked from the Download CV buttons
  favicon.svg            browser tab icon
  og.jpg                 preview image for links shared on LinkedIn, Slack, etc.
  mnist-steps.png        frames for the MNIST demo
  style-transfer.jpg     image for the Live Style Transfer card
.nojekyll                tells GitHub Pages to serve the files as they are
```

## Editing

- **Text:** everything is written directly in `index.html`. Search for the line you want to change.
- **Colors:** the page uses the Prussian scheme. To switch, change `s-prussian` in `<div class="vt s-prussian">` to `s-vault`, `s-petrol` or `s-midnight`. The schemes are defined at the top of the `<style>` block.
- **CV:** replace `assets/Asad-Shahab-CV.pdf` with a file of the same name.
- **Link preview:** if you change the hero, retake `assets/og.jpg` at 1200 × 630.

To preview locally, open `index.html` in a browser. Or run `python -m http.server` in this folder and go to http://localhost:8000.

## Publishing

GitHub Pages serves the site from the `main` branch, root folder (Settings → Pages → Build and deployment). Pushing to `main` updates the live site, usually within a few minutes.

## Credits

Set in [Hubot Sans](https://github.com/github/hubot-sans) by GitHub, loaded from Google Fonts.
