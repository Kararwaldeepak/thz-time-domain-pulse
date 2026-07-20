# THz Time-Domain Pulse Explorer

A self-contained, interactive introduction to the information contained in a terahertz time-domain pulse and its Fourier-transform spectrum.

## Live website

https://kararwaldeepak.github.io/thz-time-domain-pulse/

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
- Spectral bandwidth and peak frequency
- Time-window, sampling-step, Nyquist-frequency, and resolution concepts

## Repository structure

```text
thz-time-domain-pulse/
├── index.html
├── README.md
├── theory.md
├── time_and_frequency_domain_guide.txt
├── CITATION.cff
├── LICENSE
└── .nojekyll
```

`index.html` contains all HTML, CSS, and JavaScript required by the live simulation. No external library, build system, or separate JavaScript file is needed.

## Detailed guide

Read [`time_and_frequency_domain_guide.txt`](time_and_frequency_domain_guide.txt) for a detailed beginner-friendly explanation of the time and frequency domains, including ASCII visualizations, practical interpretation, common mistakes, and a glossary.

Read [`theory.md`](theory.md) for shorter theoretical notes.

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

## Important upload rule

Upload the extracted files themselves. Do not upload the ZIP file, and do not paste the contents of one file into another file.

The first line of `index.html` must be:

```html
<!DOCTYPE html>
```

## Author

**Deepak Kararwal**  
Research in terahertz photonics, THz time-domain spectroscopy, structured THz beams, polarization imaging, and waveguide propagation.

## License

MIT License.
