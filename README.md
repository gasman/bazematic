# bazematic

A browser-based ZX Spectrum live-coding environment

https://bazematic.demozoo.org/

## Background

At the NOVA 2023 demoparty, there was a live-coding jam organised on the premise of "if you can broadcast your screen, you can code in whatever tools you like". So, because I'm an awkward bugger, I decided to try my hand at live-coding for the Spectrum in Z80 assembler. Unfortunately, since no-one has made a dedicated live-coding environment for that, it involved a whole lot of switching between the emulator, text editor, and command line for the assembler.

bazematic is my attempt at addressing this obvious gap in the live-coding ecosystem. It brings together my [JSSpeccy](https://github.com/gasman/jsspeccy3) emulator, roudoudou's [rasm](https://github.com/EdouardBERGE/rasm) assembler (cross-compiled to WebAssembly with [Emscripten](https://emscripten.org/)), and the [Ace](https://ace.c9.io/) code editor into a single coder-friendly package.

Following the precedent of [Bonzomatic](https://github.com/Gargaj/Bonzomatic) being named after Bonzaj / Plastic who spearheaded live shader coding, bazematic is named after legendary Spectrum coder Baze / 3SC.

## Compilation notes

There isn't a proper build script right now - compiled assets from jsspeccy, rasm and ace are included directly into the repo.

* jsspeccy is built from [commit 429daf15](https://github.com/gasman/jsspeccy3/commit/429daf159d620340c5e54939dfa761dd9f405e0f) with `npm run build` - the contents of `dist` are copied into `jsspeccy`
* rasm is built from [commit af8013ed of my fork](https://github.com/gasman/rasm/commit/af8013edbcf573a31c17b5dfbdbfe03344adb3be), using `emmake make` with an emscripten environment active. The resulting `rasm.js` and `rasm.wasm` are copied into `rasm`
* ace is the `src-min` subtree of [commit d065fe88](https://github.com/ajaxorg/ace-builds/commit/d065fe88b942824db5e8820b8e9693df3499a2cb)
