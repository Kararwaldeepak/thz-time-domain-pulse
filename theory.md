# Understanding a Time-Domain THz Pulse

> For a longer beginner-friendly version with ASCII diagrams, sampling rules, practical interpretation examples, and a glossary, see [`time_and_frequency_domain_guide.txt`](time_and_frequency_domain_guide.txt).


## 1. What is measured?

In coherent THz time-domain spectroscopy, the measured waveform is proportional to the transient electric field:

\[
E(t).
\]

The horizontal axis is the relative delay between the THz pulse and the optical gate pulse. The vertical axis is the detected electric-field amplitude.

Unlike an intensity measurement, the electric-field trace can be positive or negative. The sign indicates the instantaneous direction of the electric field along the detected polarization axis.

## 2. Why does the pulse have positive and negative lobes?

A propagating electromagnetic transient cannot generally remain as a purely unipolar field in free space. Broadband THz emitters therefore commonly produce single-cycle or few-cycle waveforms. The field changes direction during the transient, producing positive and negative lobes.

The detailed waveform depends on:

- THz generation mechanism
- emitter thickness and conductivity
- detector response
- propagation and focusing optics
- water-vapor absorption
- sample or waveguide response
- reflections from parallel interfaces

## 3. Time-domain information

A measured waveform can reveal:

### Arrival time

A shift in the pulse position indicates a propagation delay. For a sample, this delay is connected to refractive index and thickness. In a waveguide, it can reflect modal group delay and dispersion.

### Peak and peak-to-peak field

The peak absolute field is

\[
E_{\mathrm{peak}} = \max_t |E(t)|.
\]

The peak-to-peak value is

\[
E_{\mathrm{pp}} = E_{\max} - E_{\min}.
\]

These are common relative measures of signal strength.

### Temporal width

The full width at half maximum is often evaluated from the intensity-like quantity

\[
I(t) \propto E^2(t),
\]

or from an analytic-signal envelope. The exact definition should always be stated.

### Echoes

A second pulse at a later time can be caused by an internal reflection. For a round trip through a material of thickness \(d\) and refractive index \(n\), the approximate delay is

\[
\Delta t \approx \frac{2nd}{c}.
\]

### Ringing

Oscillations after the main pulse may arise from resonances, narrow absorption features, etalon reflections, waveguide-mode interference, or detector response.

## 4. Frequency-domain information

The complex spectrum is obtained through a Fourier transform:

\[
E(\omega) = \int_{-\infty}^{\infty} E(t)e^{-i\omega t}\,dt.
\]

Because \(E(\omega)\) is complex, it contains both amplitude and phase:

\[
E(\omega) = |E(\omega)|e^{i\phi(\omega)}.
\]

A short pulse generally supports a broad spectrum. A longer oscillatory waveform generally produces a narrower spectrum.

## 5. How THz-TDS reconstructs the waveform

A conventional THz-TDS experiment does not record the complete picosecond transient with an ordinary electronic oscilloscope. Instead, an ultrashort optical gate samples the THz field at a controlled relative delay.

The basic sequence is:

1. Generate a THz pulse.
2. Split or synchronize an optical gate pulse.
3. Change the optical delay.
4. Measure one electric-field sample.
5. Repeat across the delay range.
6. Assemble the samples into \(E(t)\).
7. Apply a Fourier transform to obtain \(E(\omega)\).

## 6. Why phase matters

Two signals can have similar spectral amplitudes but different spectral phases. Their time-domain waveforms can therefore be very different. Coherent THz-TDS is powerful because it preserves this phase information.

## 7. Educational model used in this repository

The web simulation includes:

- a derivative-of-Gaussian-like single-cycle pulse,
- a Gaussian-envelope carrier model,
- optional quadratic temporal phase (chirp),
- a delayed scaled copy representing a reflection,
- deterministic artificial noise,
- a numerical discrete Fourier transform.

The model is intended for conceptual visualization and is not a substitute for a calibrated emitter, detector, or complete propagation transfer function.
