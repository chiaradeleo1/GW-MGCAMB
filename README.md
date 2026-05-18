# GW-MGCAMB

`GW-MGCAMB` is an extension of [**MGCAMB**](https://github.com/sfu-cosmo/MGCAMB) in which we implemented source terms for Gravitational Wave (GW) observables.  
These features are planned to be included in the main MGCAMB repository in future releases.

## Implemented GW Source Terms

In addition to the source terms already available in MGCAMB, this extension includes:

- **Gravitational Wave Number Counts (GWNC)**  
  `source_type = gwcounts`

- **Gravitational Wave Weak Lensing (GW-WL)**  
  `source_type = gwamp`

Both observables include the full set of relativistic corrections described in Appendix A of:

> De Leo et al., *[Illuminating the dark sector: understanding modified gravity signatures with cross-correlations of Gravitational Waves and Large-Scale Strucuture]*, JCAP 05 (2026) 038  
> https://iopscience.iop.org/article/10.1088/1475-7516/2026/05/038

The relativistic contributions can be enabled or disabled through the standard `pars.SourceTerms` options in CAMB.

---

# Relativistic Contributions

## GW Number Counts (`gwcounts`)

The following contributions are implemented:

| Contribution | Flag |
|---|---|
| Density (main term) | `gwcounts_density` |
| Gravitational potential | `gwcounts_potential` |
| Gradient of the potential | `gwcounts_gradpotential` |
| Time delay | `gwcounts_timedelay` |
| Doppler effect | `gwcounts_velocity` |
| Integrated Sachs–Wolfe effect | `gwcounts_ISW` |
| Luminosity-space distortions | `gwcounts_lsd` |
| Lensing contribution | `gwcounts_lensing` |

---

## GW Weak Lensing (`gwamp`)

The following contributions are implemented:

| Contribution | Flag |
|---|---|
| Convergence (main term) | `gwlens_lensing` |
| Volume distortion | `gwlens_volume` |
| Time delay | `gwlens_TD` |
| Doppler effect | `gwlens_velocity` |
| Sachs–Wolfe effect | `gwlens_sw` |
| Integrated Sachs–Wolfe effect | `gwlens_ISW` |

---

# Citation

If you use this code in your work, please cite:

```bibtex
@article{De Leo_2026,
doi = {10.1088/1475-7516/2026/05/038},
url = {https://doi.org/10.1088/1475-7516/2026/05/038},
year = {2026},
month = {may},
publisher = {IOP Publishing},
volume = {2026},
number = {05},
pages = {038},
author = {De Leo, C. and Cañas-Herrera, G. and Balaudo, A. and Martinelli, M. and Silvestri, A. and Baker, T.},
title = {Illuminating the dark sector: understanding modified gravity signatures with cross-correlations of Gravitational Waves and Large-Scale Structure},
journal = {Journal of Cosmology and Astroparticle Physics},
}

```

and the original [**MGCAMB**](https://github.com/sfu-cosmo/MGCAMB) code.
