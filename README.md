# THz Time-Domain Pulse Explorer

A self-contained, interactive introduction to the information contained in a terahertz time-domain pulse and its Fourier-transform spectrum.

## Live website

https://kararwaldeepak.github.io/thz-time-domain-pulse/

## Read the complete guide online

The full beginner-friendly guide is available as a normal webpage:

https://kararwaldeepak.github.io/thz-time-domain-pulse/guide.html

No file download is required. Readers can move through the table of contents and view all equations and text visualizations directly in their browser.

The same guide is also available as GitHub-rendered Markdown: [`time_and_frequency_domain_guide.md`](time_and_frequency_domain_guide.md).

## What readers can explore

- The measured THz electric field, `E(t)`
- Positive and negative field polarity
- Arrival time, peak field, peak-to-peak amplitude, and temporal width
- Difference between electric field `E(t)` and intensity `E²(t)`
- Single-cycle and carrier-envelope pulses
- Chirp and temporal distortion
- Reflections and delayed echoes
- Noise and signal quality
- Point-by-point sampling in THz time-domain spectroscopy
- Fourier-transform amplitude spectrum
- Spectral bandwidth, phase, and group delay
- Time window, sampling step, Nyquist frequency, and spectral resolution

## Repository structure

```text
thz-time-domain-pulse/
├── index.html
├── guide.html
├── time_and_frequency_domain_guide.md
├── README.md
├── theory.md
├── CITATION.cff
├── LICENSE
└── .nojekyll
```

`index.html` contains the interactive simulation. `guide.html` contains the complete readable online chapter. No external library or build system is needed.

## Run locally

Open `index.html` directly in a modern browser, or run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## GitHub Pages configuration

In this repository, open **Settings → Pages** and use:

```text
Source: Deploy from a branch
Branch: main
Folder: / (root)
```

## Author

**Deepak Kararwal**  
Research in terahertz photonics, THz time-domain spectroscopy, structured THz beams, polarization imaging, and waveguide propagation.

## License

MIT License.
