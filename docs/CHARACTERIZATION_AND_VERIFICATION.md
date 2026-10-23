# Fabrication, verification, and optical characterization

This document separates **repository artifacts**, **author-reported project history**, and **measurements still awaiting upload/independent processing**.

## 1. Verification and fabrication provenance

The author reports that the passive PIC designs were submitted through a **university-led design/tapeout workflow**, passed **DRC and LVS**, were fabricated, and subsequently underwent optical characterization.

**Not yet included in this repository:** DRC/LVS reports, verification-tool versions, PDK version, foundry submission receipts, fabrication process details, source GDSII files, and raw measurement CSV files. Therefore the repository does **not** independently substantiate those milestones with original reports yet. When those files are available and distributable, attach them under documented device-specific directories rather than replacing the simulation plots.

## 2. Reported experimental observations

| Device | Author-reported observation | Status of quantitative processing |
| --- | --- | --- |
| MZI | Approximate FSR **1.5 nm** from measured transmission fringes | Estimate awaiting reproducible CSV extraction and spectral-resolution confirmation |
| Ring resonator | Approximate FSR **4.5 nm** from measured resonance groups | Estimate awaiting reproducible CSV extraction; reported split/asymmetric dips mean **Q is not claimed** |
| Bragg reflector | Experimental characterization performed | No verified stopband width/rejection/reflectivity archived |
| Ultra-broadband splitter | Experimental characterization performed | No calibrated splitting ratio/excess-loss/bandwidth archived |

**Important:** FSR describes spectral periodicity, not necessarily reduced loss, improved performance, or optimized fabrication. No measured-to-simulated agreement percentage is claimed from the current repository assets.

## 3. Recommended raw-data archive layout (future)

```text
MZI/measurements/
  README.md                  # device ID, setup, units, polarization, dates
  transmission_measured.csv  # wavelength vs detector/output power
Ring-Resonator/measurements/
  README.md
  transmission_measured.csv
Bragg-Grating/measurements/
  README.md
  transmission_measured.csv
Ultra-broadband-splitter/measurements/
  README.md
  port1_measured.csv
  port2_measured.csv
verification/
  README.md                  # PDK version, DRC/LVS summary, attribution
```

These are **proposed paths only**; no raw CSVs or verification reports have been uploaded as part of this documentation update.

## 4. Minimum measurement metadata

For each spectrum, record the device identifier, layout revision, tested port, operating polarization, wavelength units and step size, instrument spectral resolution, power units, fiber/grating-coupler reference measurement, and any normalization or smoothing. Preserve raw data separately from processed data.

## 5. Extraction guidance

- **FSR:** wavelength spacing between *consecutive* fringes or resonance **groups** of the same mode family; report mean/median and variability after checking for missed orders.
- **MZI extinction ratio:** local peak-to-trough power difference in dB; ensure troughs are above the detector noise floor.
- **Ring Q:** Q = resonance wavelength / fitted FWHM. For a through-port dip, use the **half-depth in linear power** after baseline correction. If dips split or overlap, fit a suitable coupled-mode model; **do not confuse doublet separation with FWHM**.
- **Insertion/excess loss:** requires a valid optical reference and calibration; raw received dBm is not automatically intrinsic device loss.
- **Bragg stopband/splitter bandwidth:** requires a stated threshold and measured port response.

## 6. Attribution and publication

Only upload experimental traces, university course material, fabrication data, and PDK files when their redistribution is permitted. Clearly distinguish designs and analysis performed by the author from fabrication and measurement performed through the university workflow.
