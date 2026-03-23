# Product Requirements Document

## Executive summary

The Solar and Plasma Synthesiser is a multi-track software instrument inspired by scientific observations of the Sun and plasma phenomena. It is intended to combine formal visual design, expressive interaction, real or derived scientific data, and a reliable synthesis architecture.

The product is not a generic space sound generator. It is a controlled instrument with a clear design philosophy: measured behaviour, artistic interpretation, precise performance control, and repeatable results.

## Product goals

### Goal 1

Create a synthesiser whose sound identity is rooted in helioseismology, solar radio activity, and plasma behaviour.

### Goal 2

Make the instrument playable through MIDI, touch interaction, and track-based mixing.

### Goal 3

Allow the user to blend one source family, several source families, or all source families together on each track.

### Goal 4

Prevent loss of repeatability by making morph states lockable and by keeping pressure-based control optional rather than default.

### Goal 5

Provide a credible public demo and a clear path to a fuller product.

## Product principles

1. The instrument should feel intentional.
2. Scientific inspiration should be visible in both sound and language.
3. Touch interaction should be expressive but controlled.
4. A pleasing result should be easy to reach.
5. A precise result should be possible to repeat.
6. The interface should respect the official DMS design language where appropriate.

## Functional requirements

### Track model

The system shall support multiple tracks.

Each track shall be either:
- a synth track, or
- a sequencer track

Each synth track shall support:
- source blending
- macro control
- per-track effects
- monitor views
- touch morph interaction
- morph hold
- morph lock
- preset selection
- MIDI routing

The sequencer track shall support:
- rhythm generation
- note or gate pattern generation
- modulation pattern generation
- scene launching
- song structure support

### Source system

Each synth track shall support the following source families:
- Helioseismology
- Solar Radio
- Plasma

Each synth track shall also support a hybrid behaviour through either:
- explicit Hybrid mode, or
- simultaneous blending of Helioseismology, Solar Radio, and Plasma layers

### Touch interaction

Each synth track shall provide:
- a small touch morph panel for quick control
- a larger selected-track touch panel for detailed performance

By default, the touch panel shall use position-based control only.

Pressure, touch size, or similar input shall not be active by default.

The system shall allow:
- free morph mode
- hold mode
- lock mode

The system shall allow morph nodes or saved sound points.

### Monitoring

Each synth track shall include a small monitor capable of showing at least one of the following:
- oscilloscope
- spectrum
- source activity
- output envelope

The selected track view shall provide an expanded monitor.

### Effects

Each track shall support DMS-style effects, including at minimum:
- delay
- reverb
- distortion
- equalisation or filter control

The system should also be designed so that additional effects can be added later, including resonator, shimmer, spectral blur, and grain delay.

### Performance control

The instrument shall support:
- MIDI note input
- velocity
- pitch bend
- mod wheel
- aftertouch where available
- MIDI learn or assignable mapping in the fuller product

### Presets and scenes

The system shall support:
- patch presets
- saved morph states
- multi-track scenes
- a clear distinction between temporary track state and saved reusable state

## Non-functional requirements

### Stability

The system should behave predictably and should avoid hidden state changes.

### Latency

The demo should remain responsive in a modern browser.

The fuller product should target performance-appropriate latency in a native environment.

### Clarity

The interface should preserve a formal and coherent language.

### Extensibility

The architecture should support future data import, stronger routing, and commercial packaging.

## User stories

- As a musician, I want to blend solar and plasma source layers on one track so I can create a richer sound.
- As a performer, I want to lock the morph state so I can return to the same sound reliably.
- As a composer, I want one sequencer track so I can establish rhythm and song structure.
- As a researcher, I want the product language to remain scientifically grounded.
- As a GitHub visitor, I want the demo to open quickly and explain itself clearly.

## Acceptance criteria

A minimum acceptable version shall demonstrate the following:
- at least three working source families
- per-track blending
- working touch morph
- morph hold and morph lock
- at least one monitor per track
- a functioning effects path
- one sequencer track
- preset recall
- clear project documentation
