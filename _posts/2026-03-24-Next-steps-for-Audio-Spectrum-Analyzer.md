---
layout: post
title: "Next steps for Audio Spectrum Analyzer"
---

Just a few quick notes about next steps for the [Audio Spectrum Analyzer]({% link _posts/2026-03-22-Spectrum-analyzer-tutorial.md %}) effort, as it evolves into a fully-featured instrument tuner:

1. Provide hints on how sharp or flat the current tone is with regard to the closest musical note.
1. Provide concept of instrument-specific target notes (EADGBE for guitar, for example) to aid with tuning. Understand that a novice may be an entire octave off, and we want to help prevent them from harming their instrument.
1. Allow for multiple instruments (guitar and violin initially, but viola/cello/bass and bass guitar are easy additions). Consider ability for multiple tunings in the future as we consider our user experience.
1. Ultimately we want at multiple user experiences:
    - A phone-native one, optimized for tuning instruments with a smartphone. Efficient provider of expert-level information.
    - A retro analog needle UI, simliar to the [Boss TU12](https://spectrum.ieee.org/the-consumer-electronics-hall-of-fame-boss-tu12-guitar-tuner).
    - An instrument-specific UI, optimized for the strings of the instrument. Ideally this is the most beginner-friendly, as it can show graphic representation of which string is being tuned, and even guide on rough vs. fine tuner use.
1. Incorporate tone generation as a part of the different experiences, as this aids in beginners learning to tune their instrument by ear. Start with artificial tone generation.

Some of these features will make interesting tutorials by themselves. For example, the analog needle UI feature will likely be a nice Swift component exercise, and some of the pitch suggestion may require deeper audio signal analysis.

I'm having fun developing this from the perspective of what makes the best learning experience.