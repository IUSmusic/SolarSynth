# Audio and Data Engine Specification

## Purpose

This document defines the synthesis logic and data strategy for the Solar and Plasma Synthesiser.

The instrument should remain scientifically informed, but it must also behave as a musical tool. The engine therefore combines real or derived scientific material with controlled synthesis and resynthesis.

## Scientific basis

The product is based on three source families.

### Helioseismology

Helioseismology provides measured oscillation behaviour of the Sun. In practice, this material supports tonal, resonant, slowly moving sound structures. The synthesis engine should preserve the impression of a large resonant body rather than a conventional bright oscillator.

### Solar Radio

Solar radio behaviour supports event-driven, chirped, sweeping, signal-like motion. This family is appropriate for bursts, glides, and spectrally animated gestures.

### Plasma

Plasma-derived material supports unstable, electrical, noisy, and turbulent behaviour. This family is appropriate for granulation, crackle, dense motion, and energetic transformation.

## Engine design principles

1. Real data should inform the identity of the sound.
2. Real data does not have to remain raw at performance time.
3. The engine should support repeatability.
4. The source families should remain perceptually distinct.
5. Hybrid use should sound intentional rather than muddy.

## Helioseismology engine

Recommended techniques:
- additive synthesis
- modal synthesis
- resonator networks
- slow phase drift
- controlled beating
- long envelope structures

The Helioseismology engine should favour:
- stable low-noise partials
- slowly evolving amplitude relationships
- a sense of inner pressure and scale

## Solar Radio engine

Recommended techniques:
- chirp synthesis
- swept oscillators
- event generators
- burst envelopes
- band-limited noise accents
- spectral scanning

The Solar Radio engine should favour:
- fast gestures
- descending or rising event trajectories
- signal clarity
- focused band energy

## Plasma engine

Recommended techniques:
- filtered noise
- granular resynthesis
- ring modulation
- frequency modulation
- chaotic modulation sources
- resonant filtering

The Plasma engine should favour:
- irregular activity
- flicker
- energy variation
- unstable but bounded motion

## Hybrid engine

Hybrid behaviour may be implemented in one of two ways.

### Layered hybrid

The three engines run simultaneously and are blended.

### Directed hybrid

A higher-level hybrid macro controls the relative contribution and movement of the engines.

The layered approach is often simpler at first. The directed approach becomes more valuable as the instrument matures.

## Data strategy

### Public demo strategy

The browser demo should use preprocessed scientific assets rather than heavy live acquisition.

Derived assets may include:
- modal tables
- compact wavetables
- event maps
- reduced time series
- short audio grains
- metadata files

### Fuller product strategy

The fuller product may support richer ingestion, including:
- additional datasets
- larger analysis windows
- user import workflow
- more complete metadata presentation

## Offline preparation pipeline

The recommended offline pipeline is:

1. acquire source files
2. read mission or archive format
3. clean and normalise the data
4. identify relevant structures
5. reduce the result into compact musical assets
6. export the asset with metadata and source references

## Monitoring taps

The engine should expose monitoring taps for:
- pre-effects output
- post-effects output
- source family activity
- macro modulation summary

These taps support both track monitors and debugging.

## State logic

The engine should distinguish clearly between:
- live performance state
- saved preset state
- saved node state
- scene state

This separation is essential for trust and repeatability.

## Default control philosophy

By default, the engine should respond to:
- position
- track macros
- MIDI note and expression
- sequencer track events where routed

Pressure-based touch response should remain optional and disabled by default.

## Reliability note

The engine should never rely on hidden randomness for core behaviour. If random or chaotic behaviour is present, it should be user-visible and bounded by named controls.
