# Gliss

A live-playable synth for gliding chords, by Superrated. Currently an experimental beta.

Six chord pads, and every note of the chord slides to the next chord as its own line. You can add arps, a counter line, a reese bass and a beat, play a lead on top, loop it, and build it into a track.

Gliss is one HTML file with no build step and nothing to install. It runs in any modern browser on a phone, tablet or computer.

## Run it

- **As an app (recommended):** open **https://superrated.github.io/Gliss/** on your phone or tablet.
  - Android (Chrome): menu ⋮ → **Install app** (or "Add to Home screen").
  - iPhone / iPad (Safari): Share → **Add to Home Screen**.
  - Or tap **⬇ Install Gliss as an app** at the top of the Start a jam screen (also in Help). On iPhone it shows the steps.
  - It then opens full screen from its own icon, works offline, and updates itself when a new version is online.
- **In a browser:** open the same link, or download `index.html` and open it in Chrome, Edge, Safari or Firefox.

To publish it yourself: Settings → Pages → deploy from the `main` branch, root folder.

On iPhone, switch the silent switch off, or web audio may stay muted.

## How to play

**Jam page**
- **Chord pads:** tap a pad and the notes glide to it on the next bar (or every 2 bars: the **1 bar / 2 bars** button under the pads). The waiting pad fills up from the bottom; when it is full the chord lands, with a short flash. A tap just after the line still counts as on time.
- **Two chords in a bar:** tap a second pad while the first is still waiting. The first lands on the bar, the second (marked ½) halfway through the chord length (half a bar, or one bar with 2 bars). Tap a waiting pad again to take it back.
- **Brighter / darker:** swipe a pad up for its brighter version, down for its darker one.
- **Chord set (▾ left of the loop bar):** 14 sets of six chords, the key, and ✎ My set 1–4 to build your own (including 6/9, sus2, m7♭5, quartal and maj7♯5 chords).
- **Lead strip:** slide across it to play notes that always fit the chord. Notes snap gently to the beat, and the chords make room for the lead. While the lead or a hook plays, the arp, counter and sparkle keep to their own ranges.
- **Hook:** tap Hook and play a phrase on the strip; two bars are kept and repeat over every chord change, with a different ending every second time. Hold Hook for a suggested hook. Tap again to let it go.
- **Add / Hold / Vary:** tap to switch on and leave on, hold to use only while held. Hold and Vary share one row: tap the small HOLD / VARY tabs to switch (a tab lights up when something on it is on).
  - Add: Arp, Counter, Reese, Beat (tap to cycle full → light → off; light is a soft kick on the 1 with quiet hats), Echo and Wash (hold to throw the chords into a long dub echo or a big reverb that rings on after you let go), Spark (bells)
  - Hold: Freeze, Octave up, Smear, Darken, Stab, Softer, No chords
  - Vary: Low only, Swell, Pulse top, One by one, Shimmer, Pedal (the bass holds its note while the chords move), Breathe (each push spreads the notes apart or pulls them together)
- **Lead** moves the strip an octave, **Lift ↑** moves the whole jam up a step at the next bar (hold for down), **Stab** sets the stab style: plucked rhythms or a filter that pumps, wobbles, gates or sweeps. A small dot on a button means holding it does something extra.
- **Filter pad:** left–right sets the cutoff, up–down the resonance.
- **Play / Stop:** Stop fades out gently. Hold it to switch every locked button off at once.

**Loops**
- Tap **Loop** to record 2, 4, 8 or 16 bars (tap the bars chip to change it). The loop keeps chords, the lead, the buttons you lock or hold, and filter pad, Space and Drive moves.
- While it plays, tap a pad to swap the chord in that spot. **Loop A ▾** opens the loop menu:
  - **Overdub:** add buttons, lead and knob moves; tapping a button switches that layer on or off in the loop from that point.
  - **Undo**, **Record / go to loop B**, **Chain** (A A B A, A B A B and more, played by itself), **Edit loop**, **Clear loop** (tap twice).
- **Edit loop** (or tap the loop bar): each block is half a bar. The Chords tab picks its chord, ▼ darker or ▲ brighter variation, Keep last, or Break (the end of the block goes quiet). The Layers tab switches layers on or off per block and removes the lead from a block. At the bottom: Clear lead, Clear moves, Double loop.
- Each loop keeps its own sound, so B can sound different from A.
- With **Loop repeats** set to vary a little (Shape › Chords), loops of 2 bars or more sometimes get a chord in their last half bar that pulls back to the start (a turnaround).

**Shape page**
- **Chord sounds** include laid-back ones: Rhodes and Wurli (electric-piano tones that are struck and ring out, with tremolo), Mellow analog, Dusk pad (both swell gently into each chord) and Deep stab. Laid-back presets: Rhodes lounge, Late night Wurli, Mellow drive, Sunday dusk and Deep dub (dark offbeat stabs, long echoes, deep bass). There is also a hypnotic **Deep** chord set.
- **Phone load:** Auto (default) switches to Eco on weaker phones: up to 3 voices per note, the Clean filter, lighter distortion and a shorter reverb, so it does not crackle. You can also choose Eco or Full quality yourself.
- **Filter:** Clean, or Ladder (a warm analog-style filter whose resonance sings when you sweep the filter pad; used by the warm and laid-back presets).
- **Your own presets:** in the Sound preset list, save the sound you have now as My preset 1–4.
- **Sound:** Sound preset (sets everything in one go; Mirage, Lift, Full and Wild also set motion, space and some buttons), chord sound, lead sound, lead plays, ensemble, tape, voicing and stack.
- **Chords:** Arrive (how notes travel to each chord), when chords start and glide, how lines move, before-chord moves, stab style, loop repeats.
- **Arp & bass:** arp sound, shape (including 3, 5 and 7-step patterns that drift across the beat), speed, range, reese pattern, counter.
- Faders: Motion, Space, Detune, Bloom, Glide spread, Stab length, Lines one by one, Drive and Volume.
- **Save:** four slots that keep the whole song (loops A and B, chain, hook, sounds, mixer). **Mixer:** a level for each layer. **Export:** record a WAV, save the loop as MIDI, or save / open the whole song as a `.gliss` file (safe outside the browser and movable to another device). **Help.**

**Drums page**
- Beat on/off, tap tempo, drum kit (Classic, 808, 909, Lo-fi, Brush) and fills.
- A 16-step grid for kick, snare, hats and clap, with pattern presets.
- Tempo, Swing and Pump.

**Rec** records what you hear and saves it as a WAV file.

On tablets in landscape, the Jam page stays on the left with Shape or Drums on the right.

While playing, Gliss keeps the screen awake and gives a short buzz on pad taps where the browser allows it.

A short tour runs the first time you open Gliss. You can see it again under Help on the Shape page.

## Tech

Pure Web Audio API and plain JavaScript in a single file, with no libraries. Settings and saves are stored in the browser's localStorage.

## License

Copyright © 2026 Superrated. Gliss is licensed under the [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0): free to use, change and share for noncommercial purposes. See [LICENSE.md](LICENSE.md). Music you make with Gliss is yours.
