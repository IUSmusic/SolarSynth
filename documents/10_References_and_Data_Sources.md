# References and Data Sources

## Purpose

This document records the principal scientific and technical sources that support the concept and implementation direction of the Solar and Plasma Synthesiser.

## Scientific interpretation note

The project should describe itself carefully.

The instrument is based on measured solar and plasma phenomena that are audified, transposed, analysed, and resynthesised. It should not claim to present direct atmospheric audio capture of the Sun.

## Recommended data sources

### GONG

Global Oscillation Network Group provides long-running helioseismology observations and related products suitable for modal analysis and oscillation-derived synthesis work.

### SDO HMI and JSOC products

Helioseismology and Magnetic Imager data, along with related products from the Joint Science Operations Center, support solar oscillation and Doppler-based analysis.

### Solar Orbiter RPW

Radio and Plasma Waves data are well suited to event extraction, chirp behaviour, and signal-based source design.

### Solar Orbiter PHI

Polarimetric and Helioseismic Imager products can support future work involving Doppler and magnetic behaviour with different observational geometry.

### Parker Solar Probe FIELDS

FIELDS data support plasma, electric field, magnetic field, and wave-oriented source development.

### CDAWeb audification resources

These resources provide a practical reference point for turning selected scientific time series into audio.

## Recommended technical tools

### Python preparation stack

- SunPy
- SunPy SOAR plugin
- cdflib
- PySPEDAS
- NumPy
- SciPy
- pandas

### Browser demo stack

- HTML
- CSS
- JavaScript or TypeScript
- Web Audio API
- AudioWorklet
- Web MIDI API

### Fuller software stack

- native audio framework to be chosen during product planning
- Python preprocessing workflow
- formal asset pipeline

## Licensing and usage caution

Scientific data access policies and media usage terms should always be checked again before public release, especially for imagery, branding, and commercial use.

Repository documentation should make a distinction between:
- public scientific data
- processed project assets
- interface assets
- third-party brand or media material

## Review expectation

This references file should be updated whenever the project adopts a new mission source, software dependency, or public data pipeline.
