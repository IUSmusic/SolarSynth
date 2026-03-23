# User Interface and Interaction Specification

## Interface direction

The interface should preserve the official visual character that inspired this project while shifting the product away from a sequencer-first workflow. The layout should support performance, sound shaping, monitoring, and track management.

The instrument is better understood as a multi-track synthesiser with a rhythm layer than as a step sequencer.

## Primary layout

The recommended layout contains four principal areas.

### Top bar

The top bar should include:
- project title
- global status
- MIDI status
- scene controls
- global settings
- master output access

### Sidebar

The sidebar should include:
- preset browser
- scene browser
- source library
- imported data library
- project notes or metadata where useful

### Track area

The central area should contain track strips or track cards. Each track should be compact enough for overview use but rich enough to remain musically useful.

### Detail area

The detail area should show the currently selected track. This is where deeper editing, a larger touch surface, and an expanded monitor should appear.

## Track panel specification

Each synth track should contain the following sections.

### Header

- track name
- track colour
- mute
- solo
- arm
- preset name
- MIDI channel or source indicator

### Source section

- Helioseismology level
- Solar Radio level
- Plasma level
- optional Hybrid label where useful

### Macro section

Recommended default macros:
- Time Warp
- Activity
- Atmosphere
- Chaos

The project may later add further macros such as Drift, Brightness, Resonance, and Data Blend.

### Touch morph section

Each synth track should include a small touch morph panel.

This panel should support:
- position-based morphing
- node recall
- hold
- lock
- optional snap behaviour

Pressure should not be a default mapping.

### Effects section

Each synth track should include:
- delay
- reverb
- distortion
- equalisation or filter control

### Monitor section

Each track should display a small monitor.

This should support at least one switchable view:
- scope
- spectrum
- activity

### Output section

- track level
- pan
- send controls where applicable

## Selected-track detail view

When a track is selected, the detail view should show:

- large touch morph surface
- visible morph nodes
- larger monitor
- advanced source controls
- detailed macro assignments
- advanced effects controls
- save node
- recall node
- hold
- lock
- reset or home position

## Touch interaction behaviour

### Default behaviour

By default, the touch surface should be governed by X and Y position only.

This choice improves repeatability and makes patch recall more reliable.

### Optional behaviour

Additional gesture-derived behaviour may be enabled in advanced settings, but it should not be active by default.

### Morph states

The touch system should support:
- Free
- Hold
- Lock

Free allows immediate movement.

Hold retains the latest position after release.

Lock protects the current state from accidental change until the user unlocks it.

### Morph nodes

A morph node is a named sound point saved on the touch surface.

The instrument should support a small number of clearly visible nodes, enough for expressive movement without visual overload.

## Sequencer track interface

The sequencer track should have its own interface language.

It should support:
- pulse and rhythm drawing
- note or gate pattern editing
- scene trigger control
- interaction with synth tracks

The sequencer track should not dominate the visual design.

## Monitor language

The monitors should feel informative rather than decorative.

Suggested colour language:
- warm tones for Helioseismology
- electric blue for Solar Radio
- violet and bright neutral tones for Plasma

## Interaction principles

1. The user should be able to reach a meaningful sound quickly.
2. The user should be able to keep a sound stable once it is found.
3. The interface should reward exploration without becoming vague.
4. The selected-track view should always offer more control than the compact track strip.
