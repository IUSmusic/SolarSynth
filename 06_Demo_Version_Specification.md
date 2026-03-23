# Demo Version Specification

## Purpose

The demo version is the public proof of concept. It should show the core identity of the instrument clearly, work in the browser, and be simple enough to host from a public repository.

The demo is not required to expose every future feature. It is required to feel coherent, playable, and credible.

## Platform

The demo should target:
- modern desktop browser use
- GitHub repository distribution
- static hosting compatibility where possible

## Primary goals

1. Demonstrate the three source families clearly.
2. Demonstrate per-track blending.
3. Demonstrate the touch morph system.
4. Demonstrate morph hold and morph lock.
5. Demonstrate DMS-inspired effects and monitor views.
6. Demonstrate one sequencer track for rhythm or song support.

## Recommended feature set

### Included in the demo

- 4 synth tracks
- 1 sequencer track
- Helioseismology, Solar Radio, and Plasma layers
- Hybrid behaviour through blending
- small per-track touch pads
- selected-track large touch pad
- hold and lock
- preset loading
- scene recall
- per-track monitor
- basic DMS-style effects
- MIDI input
- keyboard fallback for users without MIDI hardware

### Excluded from the first demo

- large-scale live data download
- user import of raw scientific archives
- advanced automation editing
- plug-in deployment
- complex account or cloud features

## Recommended technical stack

- HTML
- CSS
- JavaScript or TypeScript
- Web Audio API
- AudioWorklet where needed
- Web MIDI where available
- offline Python preprocessing for scientific assets

## Asset strategy

The demo should ship with a small, curated set of source assets.

Suggested content:
- a small Helioseismology asset set
- a small Solar Radio asset set
- a small Plasma asset set
- a handful of presets and scenes

The aim is quality and identity, not volume.

## User experience expectations

The demo should:
- open quickly
- make sound quickly
- explain its main controls clearly
- show a reliable morph system
- feel polished enough for public viewing

## Demonstration scenarios

The demo should support at least the following scenarios:

### Scenario 1

A user opens the demo, loads a preset, touches the morph panel, locks a sound, and plays from the computer keyboard.

### Scenario 2

A user connects a MIDI keyboard, uses one synth track for a sustained Helioseismology layer, adds Radio detail, and uses the sequencer track for rhythmic structure.

### Scenario 3

A user explores monitor views and track effects, then recalls a saved scene.

## Repository expectations

The demo repository should include:
- clear setup instructions
- a short explanation of the scientific basis
- a concise licensing section
- screenshots or interface images produced by the project
- a development roadmap
