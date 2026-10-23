# Mach–Zehnder Interferometers (MZIs)

**Focus:** wavelength-dependent interference and passive circuit layouts.

## Original repository artifacts

- [Combined KLayout layout](layout/MZI_all_layout_klayout.png) and [PDF export](layout/MZI_all_layout_klayout.pdf)
- [Single MZI simulation](simulations/MZI_single.png)
- [Double MZI simulation](simulations/MZI_double_transmission_spectrum.png)
- [Equal-arm MZI simulation](simulations/MZI_same_length.png)
- [Original design notes](notes/MZI_notes.txt)

![MZI designs](layout/MZI_all_layout_klayout.png)

**Simulation results — original files preserved:**

![Simulated MZI response](simulations/MZI_double_transmission_spectrum.png)

## Design and characterization

The original design note specifies **1550 nm** and a **500 nm waveguide width**, with layout in **KLayout** and optical simulation in **Ansys Lumerical FDTD**. The project contains multiple MZI layout configurations, including equal-arm and unequal-arm variants.

The author reports university-led fabrication/characterization and **approximately 1.5 nm measured FSR**. This is a preliminary value from experimental spectra, **not** an independently recomputed CSV result in this repository.

A reproducible design–measurement comparison would require measured transmission CSVs, the associated arm-length difference, and simulated spectra for the matching device ID. Do not infer insertion loss or extinction ratio from a layout image.

See [characterization notes](../docs/CHARACTERIZATION_AND_VERIFICATION.md).
