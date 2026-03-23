# Project Charter

## Project title

Solar and Plasma Synthesiser

## Project purpose

The purpose of this project is to design and build a software instrument that translates the behaviour of the Sun and related plasma phenomena into a playable musical system.

The instrument will not present itself as a literal recorder of sound in a gaseous atmosphere. Instead, it will use measured solar oscillation data, plasma wave behaviour, radio events, and related scientific inputs as the foundation for audification, transposition, resynthesis, and controlled performance.

The project has two principal outputs.

The first output is a public demonstration version that can be published on GitHub and experienced in the browser.

The second output is a fuller software version designed as a serious instrument with deeper synthesis control, stronger data integration, and a more mature production workflow.

## Vision statement

The Solar and Plasma Synthesiser should feel like an instrument, not a novelty. It should invite performance, composition, and research-minded experimentation. It should carry a clear scientific character while remaining musically expressive, stable, and enjoyable to use.

## Strategic objectives

1. Create a recognisable synthesis identity built from helioseismology, solar radio behaviour, and plasma motion.
2. Preserve a formal visual language inspired by the existing DMS framework while moving away from a sequencer-first interface.
3. Support deliberate sound design through touch morphing, MIDI performance, lockable states, and repeatable presets.
4. Deliver a browser-based demo that is technically credible and publicly shareable.
5. Deliver a software product specification that can guide later development into a standalone application and plug-in format.

## Scope

### In scope

- Multi-track instrument model
- Helioseismology source layer
- Solar radio source layer
- Plasma source layer
- Hybrid source behaviour
- Per-track touch morph control
- Morph hold and morph lock
- Per-track monitoring, including oscilloscope and spectrum style views
- DMS-inspired effects workflow
- One optional sequencer track for rhythm and structure
- Presets, scenes, and saved morph states
- Public documentation suitable for GitHub

### Out of scope for the first public demo

- Full real-time ingestion of all live spacecraft data
- Full digital audio workstation integration
- Commercial licensing workflow
- Expanded collaboration features
- Large-scale user import of every mission format without preprocessing

## Primary users

### Creative user

A musician, composer, producer, or sound artist who wants a distinctive instrument that can move between ambient, cinematic, experimental, and structured musical work.

### Technical user

A developer, researcher, or educator who wants to explore solar and plasma data through a well-designed audio interface.

### Demonstration user

A public GitHub visitor who wants a clear, immediate, browser-based experience that communicates the idea and the technical credibility of the project.

## Success criteria

The project will be considered successful when the following conditions are met:

- The instrument produces a recognisable sound identity that differs from conventional subtractive or wavetable synthesis.
- The user can intentionally shape and recall sound states without relying on uncontrolled randomness.
- The public demo is simple enough to run in the browser and strong enough to demonstrate the concept clearly.
- The full product specification is detailed enough to guide implementation without major redesign.
- The documentation is clear, formal, and credible for public presentation.
