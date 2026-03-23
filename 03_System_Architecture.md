# System Architecture

## Architectural summary

The Solar and Plasma Synthesiser should be built as a layered system. The visual interface, synthesis engine, data preparation workflow, performance control, and storage model should remain distinct so that the demo and the fuller software version can share concepts without forcing a single codebase forever.

## Core layers

### Presentation layer

The presentation layer is responsible for:
- track panels
- touch surfaces
- monitor displays
- preset browser
- mixer controls
- master controls
- selected-track detail view

The presentation layer should preserve the formal style inspired by the DMS interface while moving away from a sequencer-first layout.

### Control layer

The control layer is responsible for:
- MIDI handling
- touch gesture handling
- morph node selection
- macro movement
- automation capture
- lock and hold state logic
- sequencer track triggering

### Audio engine layer

The audio engine layer is responsible for:
- source generation
- source blending
- modulation
- effect processing
- monitoring taps
- output routing

### Data layer

The data layer is responsible for:
- preset storage
- scene storage
- morph node storage
- source metadata
- imported and preprocessed scientific assets
- browser-ready derived assets for the demo

### Preparation pipeline

The preparation pipeline is responsible for converting external scientific files into assets appropriate for the instrument. This work is expected to be done offline in Python for both reliability and clarity.

## Recommended track architecture

### Synth track

A synth track contains:
- identity metadata
- source family levels
- macro values
- touch state
- morph node definitions
- lock state
- effect state
- monitor selection
- MIDI settings
- output routing

### Sequencer track

A sequencer track contains:
- pattern data
- timing and pulse logic
- note or gate output data
- modulation lane data
- scene trigger assignments
- playback state

### Master bus

The master bus contains:
- global output controls
- global effects
- scene recall
- transport behaviour where needed
- application-wide settings

## Signal flow

The recommended signal flow for a synth track is:

Source layers  
to source mixer  
to modulation stage  
to per-track effects  
to monitor tap  
to track output  
to master bus  
to master effects  
to audio destination

The recommended signal flow for the sequencer track is:

Pattern engine  
to event generation  
to target track routing  
to synth parameter or note output

## Source layer model

Each synth track should host up to three active source layers.

### Helioseismology layer

The Helioseismology layer is the tonal and resonant body.

### Solar Radio layer

The Solar Radio layer is the event-based and signal-like component.

### Plasma layer

The Plasma layer is the electrical, noisy, and unstable component.

These layers may be blended directly, or wrapped in a higher-level Hybrid presentation.

## Data preparation model

External data should not be read raw in the browser during the demo except in carefully controlled cases.

The recommended workflow is:
1. obtain source data
2. analyse and reduce it offline
3. produce a compact derived asset
4. store metadata with the asset
5. load the asset into the demo or software product

This approach reduces complexity and improves reliability.

## Storage model

The project should separate:
- application state
- track state
- preset state
- scene state
- imported source metadata

This prevents accidental coupling between temporary performance behaviour and saved reusable content.

## Recommended implementation split

### GitHub demo

- browser application
- Web Audio engine
- AudioWorklet processing where appropriate
- Web MIDI support
- preprocessed assets
- static hosting compatibility

### Fuller software version

- native application and plug-in
- stronger routing
- expanded data import
- deeper monitoring
- richer preset and scene system
- improved performance headroom

## Architectural priorities

1. Predictable state management
2. Clear separation between interface and engine
3. Offline data preparation
4. Stable touch behaviour
5. Extensible source and effects system
