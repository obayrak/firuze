# Firuze

**A nuclear-reaction code that runs in your browser.**

*Author: Orhan Bayrak*  ·  Licence: [GPL-3.0](LICENSE)

Firuze calculates direct and compound nuclear reactions (elastic scattering, inelastic excitation, transfer, breakup, capture, resonances and compound-nucleus decay) and plots the results right away. The whole program is one HTML file. You don't install anything, need no server and don't compile anything: open the page, choose a case and press **▶ Run**.

▶ **Open the app:** https://obayrak.github.io/firuze/
📱 **Phone version:** https://obayrak.github.io/firuze/mobile.html

---

## What it calculates

| Tab | What it does |
|---|---|
| **Optical model** | Elastic scattering: dσ/dΩ, σ_R, σ_T, S-matrix, phase shifts; global potentials (Koning–Delaroche, Avrigeanu α, …) |
| **Coupled channels** · **Spin-½ CC** | Inelastic excitation of rotational and vibrational states, with and without projectile spin |
| **Coulomb excitation** | Coulomb and projectile excitation |
| **Sub-barrier CC** · **Mutual excitation** | Fusion-region coupled channels that stay stable at the lowest energies; projectile and target both excited |
| **Transfer (DWBA)** · **CCBA** · **CRC** | Zero- and finite-range transfer, post and prior form, (d,p), (t,p), pickup; transfer with coupled-channel waves and coupled reaction channels |
| **CDCC breakup** | Breakup through continuum bins and pseudo-states |
| **Semiclassical** | Classical trajectories, rainbows, glory, diffraction |
| **Radiative capture** | E1 direct capture and the astrophysical S-factor |
| **R-matrix fit (AZURE-like)** | Multi-level, multi-channel R-matrix fits of resonances |
| **Reaction rates** | Thermonuclear rates N_A⟨σv⟩(T₉) from S-factors and narrow resonances, with Gamow windows |
| **Compound nucleus (HF)** | Hauser–Feshbach decay with width fluctuations (HRTW), direct inelastic, exciton pre-equilibrium, (n,2n)/(n,np), isomers and angular distributions |
| **Exfor** · **Fitting** | Import experimental data (EXFOR X4, C4, tables), kinematics; robust and global fits |
| **Emulator (OM / CC)** | Fast emulators (eigenvector continuation, reduced basis) for Bayesian uncertainty quantification |
| **FRESCO comparison** | Benchmarks against FRESCO |
| **How Firuze works** | Animated diagrams of how the code runs, with a live solver, pop-up definitions, an Argand diagram, solver comparison and a 2D wave picture |
| **Theory** | 41 sections of the physics and the numerical methods behind every tab, with formulas, symbols, algorithms and limitations |

Every tab comes with ready-made **cases** (each tab has a selection of them), several plot views, a CSV/PNG/SVG export and a **model summary** you can copy into an input file for a cross-check with standard codes (FRESCO, TALYS).

## Numerical methods

The radial equation can be solved with Numerov, RK4, Numerov with integral matching and Richardson extrapolation, the Lagrange–Legendre R-matrix, R-matrix propagation, Ixaru's piecewise perturbation method (CPM), and a Chebyshev spectral integral-equation method. Heavy jobs run in parallel Web Workers, with WebAssembly inner loops. A built-in **verify numerics** panel runs over 100 regression checks (flux conservation, unitarity, symmetries, benchmarks) in the browser.

## Use

- **Online:** open the link above.
- **Offline:** download `index.html` and open it in a recent Chrome, Edge, Firefox or Safari.
- **Internet:** the formulas (MathJax) and plots (Plotly) are loaded from cdnjs, so the first opening needs a connection.

Quick start:
1. Choose a tab, for example **Optical model**.
2. Choose a case from the list.
3. Press **▶ Run**.
4. Switch between views and export the results.
5. Open **Theory** for the physics, or **How Firuze works** to watch what the code is doing.

## Files

| File | |
|---|---|
| `index.html` | Firuze (desktop layout) |
| `mobile.html` | Firuze (phone layout) |
| `README.md` | this page |
| `LICENSE` | GNU General Public License, version 3 |
| `.nojekyll` | lets GitHub Pages serve the files as they are |

## Accuracy and limits

Firuze is an educational and research tool. Each Theory section lists what is approximated and what is not included. For example, compound-nucleus level densities and γ strengths come from systematics, so (n,γ) and multiple-emission cross sections can be off by large factors unless they are normalised to data. Check important numbers against established codes and measured data before you publish them.

## Citation

If you use Firuze in teaching or research, please cite this repository:

```
O. Bayrak, Firuze: a browser-based nuclear-reaction workbench (2026),
https://github.com/obayrak/firuze
```

## Licence

Copyright © 2026 Orhan Bayrak

Firuze is free software: you can redistribute it and/or modify it under the terms of the **GNU General Public License** as published by the Free Software Foundation, either **version 3** of the License, or (at your option) any later version.

Firuze is distributed in the hope that it will be useful, but **without any warranty**; without even the implied warranty of merchantability or fitness for a particular purpose. See the [GNU General Public License](LICENSE) for more details.
