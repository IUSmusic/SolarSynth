# GitHub Documentation and Release Guide

## Purpose

This guide explains how the documentation should be presented in the public repository.

## Repository documentation structure

The repository should include:
- a root `README.md`
- a `documents` folder
- a `media` folder for screenshots and approved visuals
- a `demo` folder if the browser build is separated
- a `tools` or `scripts` folder for preprocessing utilities where needed

## Root readme guidance

The root readme should contain:
- project title
- short mission statement
- key features
- screenshots
- quick start
- scientific basis summary
- documentation links
- contribution note
- licensing note

## Documents folder guidance

The `documents` folder should contain the formal files included in this package.

These documents should not be treated as throwaway notes. They should be versioned, reviewed, and updated as the product evolves.

## Tone and wording

The repository should use:
- formal language
- concise sentences
- plain technical clarity
- consistent naming

Avoid exaggerated claims.

Avoid presenting artistic interpretation as raw physical audio capture.

## Release guidance for the demo

Before the public demo is released, confirm the following:
- the application runs in the intended browser targets
- touch morph lock behaves reliably
- presets load correctly
- monitor views work
- MIDI fallback is explained clearly
- the scientific basis section is present
- the licensing note is accurate

## Contribution guidance

If public contribution is allowed, the repository should include:
- contribution instructions
- coding style guidance
- issue templates
- discussion boundaries for scientific claims versus creative interpretation

## Versioning guidance

Use clear semantic versioning once the demo reaches public release maturity.

Suggested early path:
- 0.1.0 for first internal demo
- 0.2.0 for feature-complete public demo
- 0.3.0 and onward for refinement before product transition

## Review guidance

The documentation should be reviewed whenever:
- the interaction model changes
- the source families change
- the data strategy changes
- the product scope changes
