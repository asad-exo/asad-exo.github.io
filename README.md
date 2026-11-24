# asad-exo.github.io

My personal site: **https://asad-exo.github.io**

I'm Asad Shahab, a grad student in computer engineering at NYU Tandon. I work mostly on machine learning (AI agent security, game theory and deep learning) and I'm open to ML and software engineering roles. The site covers what I work on, my main projects, my experience and how to reach me.

## The idea

My current project, [Dye Packs for AI](https://github.com/asad-exo/Dye-Packs-for-AI), plants decoys in an AI agent's workspace to catch it when it's been hijacked. It's named after the dye packs banks hide in stacks of cash. The site takes its look from the same place: banknote printing.

That means fine guilloché line patterns, serial numbers, rubber stamps for results, notes with double-ruled borders, and perforated edges where the dark and off-white sections meet, like the edge of a postage stamp. The colors are Prussian blue and a vermilion red, borrowed from old engraved stamps. Everything is set in one typeface, Hubot Sans, mostly at its widest setting.

## What's on the page

- **An intro** that counts up to 100, then slides away to reveal the page.
- **A hero** with my name printed slightly out of register in red, as if from a second printing plate. Beside it, a spirograph draws a pattern with its turning gears in view. Click or tap it and it clears and starts over with a new, randomly picked pair of gears.
- **About**, with a line pattern of its own for each of the four things I work on: AI agent security, game theory, deep learning and software engineering.
- **Selected work**: Dye Packs for AI, Sequence, Kestrel and Soundstage. Each comes with a small animation of what the project does, plus its key results stamped underneath.
- **Other projects**: Finish the Lyric, MNIST Denoising, Live Style Transfer and Prim's vs. Kruskal's, each on a small card with its own demo.
- **Record**: my experience and education.
- **Contact**: email, LinkedIn, GitHub and my CV.

## How it's built

It's a single static page with no framework and no build step: plain HTML, CSS and a little JavaScript.

- **The line patterns are math, not images.** Every rosette and wavy band is a hypotrochoid, the curve a spirograph draws. The page computes them in JavaScript when it loads and draws them as SVG paths, so they stay sharp at any size.
- **The hero spirograph** runs on a canvas. It simulates a small circle rolling inside a larger one, with a pen fixed to the small circle. The curve is drawn a little at a time, and the gears are drawn on a second canvas on top. It always opens on the same pattern. After that, each new one picks a random gear ratio in lowest terms, so every curve closes into a clean figure. The drawing pauses whenever the hero is off screen.
- **The project demos are CSS animations.** These are the decoy monitor replaying a real hijack from my experiments, chips completing a sequence on a game board, a knight moving through a game, and a waveform split between narrator and character voices.
- **The MNIST demo** steps through real denoising frames from my [MNIST Denoising](https://github.com/asad-exo/MNIST-Denoising) project. They're tinted to match the page with CSS blend modes.
- **Colors are CSS variables.** Each scheme is one class, which made it easy to try eight palettes before settling on Prussian.
- **The perforated edges** are a repeating radial gradient: a row of dark circles cut into the top and bottom of each light section.
- **Project cards are dealt in** like playing cards as you scroll to them. The intro only plays once per visit.
- **It respects reduced motion.** If your system asks for less motion, the animations stop and the spirograph shows one finished pattern, and clicking it swaps in another.

## Credits

Set in [Hubot Sans](https://github.com/github/hubot-sans) by GitHub, loaded from Google Fonts. Hosted on GitHub Pages.
