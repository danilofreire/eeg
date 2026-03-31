# EEG with Python

From raw signal to metastability.

**Live site:** <https://danilofreire.github.io/eeg/>

## What this is

A learning site for EEG analysis in Python using [MNE-Python](https://mne.tools). The content follows the structure of the [EEGLAB tutorials](https://eeglab.org/tutorials/) but is written entirely in Python, with examples using simulated data so you can run everything without real patient recordings.

The site supports the master's project of Natalia Sayuri Melo (Neuroscience and Cognition, UFABC) on metastability of resting-state brain dynamics in Parkinson's disease.

## Modules

| Module | Topic | What it covers |
|:------:|:------|:---------------|
| 1 | Getting started | Installing MNE-Python, data structures (`Raw`, `Epochs`, `Evoked`), loading files, simulating data, montages |
| 2 | Preprocessing | Band-pass and notch filtering, re-referencing, resampling, bad channel detection, interpolation, epoching |
| 3 | Artifact rejection | Visual inspection, amplitude-based rejection, ICA (theory, practice, ICLabel), autoreject |
| 4 | Spectral analysis | PSD (Welch), frequency bands, topographic maps, time-frequency decomposition, ERPs, ERSP |
| 5 | Connectivity and metastability | Phase synchronisation, Hilbert transform, PLV, Kuramoto order parameter, dominant eigenvector, regional metastability, group statistics |

## Content

- **5 modules** with narrative explanations and code examples
- **41 topic pages** covering individual techniques in detail
- **100 exercises** (20 per module) with hints and complete solutions, all using simulated data

## Libraries used

- `mne` -- EEG processing: loading, filtering, ICA, spectra, connectivity
- `numpy` -- numerical operations, linear algebra
- `scipy` -- Hilbert transform, filters, statistics
- `matplotlib` -- signal visualisation, topographies, spectra
- `pandas` -- organising demographic and clinical data
- `pingouin` -- ANOVA, post-hoc tests, effect sizes

## Quick install

```bash
pip install mne numpy scipy matplotlib pandas pingouin
```

Or with conda:

```bash
conda install -c conda-forge mne numpy scipy matplotlib pandas
pip install pingouin
```

## Building the site locally

The site is built with [Quarto](https://quarto.org/). To render it:

```bash
quarto render
```

The output goes to `_site/`. To preview locally:

```bash
quarto preview
```

## Deploying

The site is deployed to GitHub Pages via the `gh-pages` branch:

```bash
quarto publish gh-pages
```

## Licence

This material is shared for educational purposes. Please cite the repository if you use it in your own teaching or research.
