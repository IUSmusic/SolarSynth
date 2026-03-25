## Demo Version v0.1a
#### Standalone App
- [Windows 64-bit](./SolarSynth%20for%20Window.exe)
- [Linux 64-bit AppImage](./SolarSynth%20for%20Linux.AppImage)

#### Plugin
VST3
- [Windows 64-bit](./SolarSynth%20VST3%20for%20Windows.vst3.zip)
- [Linux 64-bit](./SolarSynth%20VST3%20for%20Linux.vst3.zip)

![0Preview](solarsynthpreview01.png)
![0Preview](solarsynthsettingpreview.png)

# SolarSynth

SolarSynth is a JUCE-based instrument that combines a playable three-layer synth engine, internal rhythmic trigger lanes, live performance controls, and audio capture into one desktop application and VST3 plug-in.

**SolarSynth** is built around three complementary signal engines, each derived from a different physical aspect of solar and plasma behaviour. Rather than imitating traditional subtractive or keyboard synthesis, the instrument models three families of motion: solar oscillation, radio-burst activity, and plasma turbulence. These become the Helio, Radio, and Plasma engines.
- **Helio**
Helio is the resonant engine.
It is based on helioseismology, the study of pressure waves and oscillations moving through the Sun. NASA describes the Sun as a body filled with waves that travel, bounce, and reveal internal motion, and notes that solar oscillations include well-known five-minute surface motions as well as larger-scale wave behaviour. In the instrument, that science is translated into a harmonic field built from slow-moving resonances, modal clusters, and continuously shifting energy rather than a fixed note-on, note-off voice. The result is the body of the sound: tonal, structural, and spatially stable.
A concise professional sentence: Helio models the Sun’s oscillatory interior as a living resonant field, giving the instrument its harmonic body, weight, and long-form motion.

- **Radio**
Radio is the event and signal engine.
It is based on solar radio emissions, especially burst activity produced when energetic electrons accelerated by solar flares move through surrounding plasma and emit radio waves. ESA’s Solar Orbiter material describes these events as radio bursts whose frequency drops as the electrons travel away from the Sun, creating the distinctive falling “hockey stick” structure seen in real data and heard in sonifications as descending tones. In the instrument, that becomes a layer of chirps, sweeps, bursts, and transient signal behaviour. Radio adds articulation, edge, and communicative movement to the sound.
A concise professional sentence: Radio models solar burst behaviour as a dynamic signal layer, introducing chirps, sweeps, and transient activity that express the Sun’s more communicative and energetic side.

- **Plasma**
Plasma is the turbulence engine.
It is based on the behaviour of charged particles and plasma waves in heliophysical environments. NASA describes plasma-wave data as producing audible whistles, crunches, whooshes, and chorus-like structures when audified, reflecting the interaction of particles, magnetic fields, and wave motion. In the instrument, that science becomes a textural engine built around instability, turbulence, modulation density, and charged motion. Plasma is what gives the sound its electric surface, roughness, and sense of living disturbance.
A concise professional sentence: Plasma models charged-wave turbulence as an unstable textural field, adding friction, motion, and electrical complexity to the instrument.

- The three engines are not separate presets. They are parallel layers of one instrument.
- Helio provides structure and resonance.
- Radio provides signal events and transient motion.
- Plasma provides turbulence and texture.
*Together they form a composite sonic system that behaves more like a field than a conventional synth voice. MIDI and performance controls do not simply trigger a fixed patch. They excite, bias, and shape the relationship between these three engines in real time.

## What the app does

SolarSynth is designed as a performance-first instrument rather than a traditional menu-driven editor. The synth can be played from external MIDI, the built-in on-screen keyboard, or the computer keyboard. Its output can then be captured into loopable playback lanes, creating a layered workflow that sits somewhere between a synthesizer, a sketchpad looper, and a rhythm-driven performance tool.

The repository builds both:

- a **standalone desktop app**
- a **VST3 plug-in**

## Main features

### 1. Three-layer synth engine

The sound engine blends three continuously variable layers:

- **Helio** for the main tonal body
- **Radio** for unstable, burst-like upper energy
- **Plasma** for noisy, animated texture

These layers are shaped by a dedicated performance state that includes:

- Morph X / Morph Y control
- Morph Lock
- Density
- Drift
- Excitation
- Brightness
- Field Gain

### 2. Performance morphing

A dedicated **Morph Pad** lets the instrument move across different tonal positions in real time. This is intended as a central performance surface rather than a static modulation source.

Additional performance switches include:

- Sustain
- Field Hold
- Arpeggiator On/Off
- Arp Latch
- Room Input enable

### 3. Arpeggiator

SolarSynth includes an internal arpeggiator with the following controls:

- Arp Rate
- Arp Mode
- Octaves
- Arp Gate
- Latch
- Live-page Tap Tempo

The Live page mirrors the most important arp functions so timing changes can be made during performance without switching views.

### 4. Bass, filter, EQ, and spatial processing

The synth voice can be shaped further with:

- **Bass section**: Bass Amount, Bass Focus, Sub Enhance, Low Width
- **Filter section**: Filter Cutoff, Resonance, Mode, Drive
- **EQ section**: EQ Low, EQ Mid, EQ High
- **Delay section**: Delay Time, Delay Feedback, Delay Mix, Delay Tone
- **Reverb section**: Reverb Size, Reverb Damping, Reverb Mix
- **Stereo section**: Stereo Width, Stereo Motion, Stereo Depth

### 5. Live performance page

The **Live** page is the performance surface of the app. It includes:

- system gauges for engine and input activity
- a master waveform panel
- transport controls
- recording controls
- three playback/capture lanes
- an on-screen keyboard
- mirrored live toggles for Sustain, Arp, Tap Tempo, and Room Input
- room input status and arp tempo readout

The master section supports:

- Arm
- Play
- Pause
- Loop
- Stop / Panic
- Record master capture
- Stop recording
- Export captured audio to WAV

### 6. Master capture and lane playback

SolarSynth can record the master output and reuse it inside the Live page workflow.

Tracks **1–3** act as playback lanes that can:

- arm for capture
- store recorded clips
- play from the start
- pause playback
- loop clips
- clear existing clips

This makes it possible to perform the synth live, print results into lanes, and build layered playback beneath the master output.

### 7. Internal rhythm engine and lane routing
(will update soon)


### 8. External input modulation

SolarSynth includes an external input analysis path that can react to incoming audio.

Available controls include:

- Room Input
- Input Mix
- Input Gain
- Input Gate
- Input to Helio
- Input to Radio
- Input to Plasma
- File Blend

This allows live input energy to be analyzed and used as a modulation source for the synth engine while also supporting blended input-based behaviour inside the signal flow.

### 9. Presets and target-based editing

The **Settings** page is built around editable targets. You can choose whether you are editing:

- Master
- Lane 1
- Lane 2
- Lane 3

Each target keeps its own synth state, which makes it possible to prepare different variations of the instrument across the master and lane contexts.

Preset workflow includes:

- preset naming
- save preset to `.solarpreset`
- load preset from `.solarpreset`
- reset the currently selected target
- plug-in state save/restore through JUCE state serialization

## Interface overview

### Welcome screen

On launch, SolarSynth opens with a welcome overlay and bundled license view before entering the main interface.

### Live page

The Live page is focused on immediate interaction:

- performance monitoring
- waveform feedback
- transport
- recording
- playback lane control
- keyboard input
- fast performance toggles

### Settings page

The Settings page organizes the deeper editor into functional groups:

- Core tone
- Arp and bass
- Filter and EQ
- Delay and reverb
- Stereo and routing
- External input

It also includes the Morph Pad, target selector, preset controls, and output monitor.

## Input methods

SolarSynth can be played using:

- external MIDI input
- the built-in on-screen keyboard
- the computer keyboard

The computer keyboard is mapped as a playable note surface, making it possible to sketch and perform without an external controller.

## Technical overview

- **Framework:** JUCE
- **Language:** C++17
- **Formats:** Standalone, VST3
- **Audio I/O:** mono or stereo input, mono or stereo output
- **Graphics:** native JUCE UI with custom background rendering and OpenGL support enabled in the project


## Current workflow in practice

A typical session looks like this:

1. Play the synth from MIDI, the on-screen keyboard, or the computer keyboard.
2. Shape the sound on the Settings page using the morph surface and grouped controls.
3. Use the Live page to arm the master, perform, and monitor the waveform.
4. Capture material, then move that output into loopable playback lanes.
5. Layer lane playback under new live synth parts.
6. Save the current state as a preset or export the recorded result as WAV.

## License

This repository is provided under the **I/US SolarSynth Demo Personal Use License 1.1**.

It is a personal-use demo license rather than an open-source license. See `LICENSE.txt` for the full license text and usage terms.
