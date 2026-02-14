# Collatz Harmonics

Collatz Harmonics is an autonomous synthesis-based sound generator developed in Max/MSP.  
It uses the Collatz conjecture as a deterministic algorithm for generating pitch material, which is then mapped to musical parameters to create an evolving ambient soundscape.

show CollatzHarmonics/media/Collatz_Harmonics_main_patch.png

## How it works (high level)

- A Collatz step is applied repeatedly to an integer sequence:
  - if n is even → n / 2  
  - if n is odd → 3n + 1
- The resulting numbers are mapped to pitch ranges using modulo operations and MIDI offsets.
- Multiple independent synthesis layers (bass, lead, chord textures) are driven by separate clocks, producing slowly shifting harmonic structures.
- Stochastic modulation is used for parameters such as panning and timbral variation.

## Requirements

- Cycling ’74 Max (tested with Max 9.x)
- BEAP package (used for the Gigaverb reverb module)

If BEAP is not installed, the patch will still run, but the reverb module may be missing.

## Running the patch

1. Open `Collatz_Harmonics.maxpat` in Max.
2. Turn DSP on.
3. Start the generator layers using the main toggles.

## Demo

- YouTube: https://youtu.be/Z08BplgWCKc

## Author

Jussi Suonikko  

## Acknowledgements

The Collatz step implementation used in this project was based on an educational Max/MSP tutorial by Umut Eldem.  
All other parts of the system (pitch mapping, synthesis layers, modulation, mixing, panning, and overall architecture) were designed and implemented by the author.

Tutorial by Umut Eldem: https://youtu.be/boYDBkAlnEI?si=s1YnI2pBEGbk3ttF
