# bazematic

A browser-based ZX Spectrum live-coding environment

https://bazematic.demozoo.org/

## Background

At the NOVA 2023 demoparty, there was a live-coding jam organised on the premise of "if you can broadcast your screen, you can code in whatever tools you like". So, because I'm an awkward bugger, I decided to try my hand at live-coding for the Spectrum in Z80 assembler. Unfortunately, since no-one has made a dedicated live-coding environment for that, it involved a whole lot of switching between the emulator, text editor, and command line for the assembler.

bazematic is my attempt at addressing this obvious gap in the live-coding ecosystem. It brings together my [JSSpeccy](https://github.com/gasman/jsspeccy3) emulator, roudoudou's [rasm](https://github.com/EdouardBERGE/rasm) assembler (cross-compiled to WebAssembly with [Emscripten](https://emscripten.org/)), and the [Ace](https://ace.c9.io/) code editor into a single coder-friendly package.

Following the precedent of [Bonzomatic](https://github.com/Gargaj/Bonzomatic) being named after Bonzaj / Plastic who spearheaded live shader coding, bazematic is named after legendary Spectrum coder Baze / 3SC.
