# Microring Resonator

**Focus:** resonant wavelength response and passive ring–bus waveguide coupling.

## Original repository artifacts

- [KLayout ring layout](layout/Ring_resonator_layout_klayout.png)
- [Ring layout PDF](layout/Ring_resonator_layout_klayout.pdf) and [zoomed PDF](layout/Ring_resonator_zoom_layout_klayout.pdf)
- [Original simulated optical response](simulations/ring_response.png)

![Ring resonator layout](layout/Ring_resonator_layout_klayout.png)

**Simulation result — original file preserved:**

![Simulated ring spectral response](simulations/ring_response.png)

## Experimental status

The author reports university-led fabrication and characterization, with an **approximate measured FSR of 4.5 nm**.

Previously reviewed experimental spectra showed closely spaced / split-looking resonance minima. Possible explanations include counterpropagating-mode coupling, multiple mode families, or measurement-path artifacts. **No cause is asserted and no loaded/intrinsic Q factor is claimed.**

For Q, examine the raw CSV and measurement resolution, correct the baseline in linear power, and use a physically suitable resonance/doublet fit. Spacing between split minima is **not** the resonance linewidth.

See [characterization notes](../docs/CHARACTERIZATION_AND_VERIFICATION.md).
