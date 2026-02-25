# Knowledge Graphs are Implicit Reward Models

**Path-Derived Signals Enable Compositional Reasoning**

[Yuval Kansal](https://yuvalkansal.me/) · [Niraj K. Jha](https://ece.princeton.edu/people/niraj-jha)  
Princeton University · arXiv preprint, January 2026

[![arXiv](https://img.shields.io/badge/arXiv-2601.15160-b31b1b.svg)](https://arxiv.org/abs/2601.15160)
[![License](https://img.shields.io/badge/License-Princeton--Academic-orange.svg)](LICENSE)

---

## Overview

This repository contains the source code for the project webpage of our paper:

> **Knowledge Graphs are Implicit Reward Models: Path-Derived Signals Enable Compositional Reasoning**  
> Yuval Kansal and Niraj K. Jha  
> arXiv:2601.15160 · January 2026  
> [https://arxiv.org/abs/2601.15160](https://arxiv.org/abs/2601.15160)

We propose a post-training pipeline in which **knowledge graphs act as implicit reward models**. By deriving reward signals from KG paths, we provide verifiable, scalable, and grounded process supervision that encourages models to compose intermediate axioms — rather than only optimizing final answers — during reinforcement learning. Trained on 1–3 hop paths and evaluated zero-shot on unseen 4–5 hop queries, our 14B model outperforms GPT-5.2, Gemini 3 Pro, and a 32B expert-distilled model on the most difficult medical reasoning tasks.

## Project Page

The live site is deployed at:

```
https://kg-implicit-reward-model.github.io/
```

## Repository Structure

```
.
├── src/
│   ├── paper.mdx          # Main page content (edit this)
│   ├── pages/
│   │   └── index.astro    # Page layout and HTML shell
│   ├── components/        # Astro UI components
│   └── styles/
│       └── global.css     # Global styles and theme
├── public/
│   └── figures/           # Paper figures (PNG)
├── bibliography.bib        # BibTeX references
├── astro.config.ts         # Astro + plugin configuration
└── .github/
    └── workflows/
        └── astro.yml      # GitHub Actions deployment workflow
```

## Local Development

**Requirements:** Node.js 20+, npm

```bash
# Install dependencies
npm install

# Start dev server
npm run dev
```

Open [http://localhost:4321](http://localhost:4321) in your browser.

Other useful commands:

```bash
npm run build      # Build for production (outputs to dist/)
npm run preview    # Preview the production build locally
npm run check      # Type-check the project
```

## Editing the Page

All page content lives in **`src/paper.mdx`**. It supports:

- Markdown prose, headings, and lists
- LaTeX math via KaTeX (`$...$` inline, `$$...$$` block)
- Astro components (`<Figure>`, `<TwoColumns>`, `<HighlightedSection>`, etc.)
- Citations via `bibliography.bib`

Figures are stored as PNGs in `public/figures/` and referenced as `/figures/<name>.png`.

## Deployment to GitHub Pages

The repository includes a pre-configured GitHub Actions workflow (`.github/workflows/astro.yml`) that automatically builds and deploys the site on every push to `main`.

**To enable:**

1. Push this repository to a GitHub org or user account named `kg-implicit-reward-model`, with the repo named `kg-implicit-reward-model.github.io`.
2. In the repository on GitHub, go to **Settings → Pages**.
3. Set **Source** to **GitHub Actions**.
4. Push to `main` — the Actions tab will show the build progress.

The site will be live at `https://kg-implicit-reward-model.github.io/` within ~2 minutes of a successful build.

## Citation

If you find this work useful, please cite:

```bibtex
@misc{kansal2026kgs,
  title         = {Knowledge Graphs are Implicit Reward Models:
                   Path-Derived Signals Enable Compositional Reasoning},
  author        = {Kansal, Yuval and Jha, Niraj K.},
  year          = {2026},
  eprint        = {2601.15160},
  archiveprefix = {arXiv},
  primaryclass  = {cs.AI},
  url           = {https://arxiv.org/abs/2601.15160}
}
```

## Acknowledgements

The experiments reported in the paper were performed on computational resources managed and supported by Princeton Research Computing, Princeton AI Lab, and the Princeton Language and Intelligence Initiative at Princeton University.

The project page is built with [Roman Hauksson-Neill's academic project page template](https://github.com/RomanHauksson/academic-project-astro-template).

## License

This project is licensed for academic and research use only. See [LICENSE](LICENSE) for full terms. Commercial use is not permitted.

Copyright © 2026 Princeton University. All rights reserved.
