# Contributing

Thanks for helping! This project is meant to stay simple: one HTML file, no dependencies, no build step, no tracking.

## Ground rules

- **Keep it a single self-contained file.** No external libraries, fonts, images or audio files. Everything is drawn with SVG/CSS and the sound is generated with Web Audio. That keeps it working offline and on locked-down school networks.
- **Touch first.** Every control needs to work with a finger on a phone (big targets, no hover-only features).
- **No data collection.** Don't add analytics, accounts or network calls. The only storage is `localStorage` for best scores and volume.
- **Calm tone.** Gentle feedback, no harsh fail screens, no flashing. Respect `prefers-reduced-motion`.
- **Keep the facts accurate.** Any health or tea-science statement should be something a teacher would be comfortable repeating. Use "may help" for claims that aren't settled.
- **Match the surrounding code:** same naming, same comment density, same style.

## How to contribute

1. Fork the repo and create a branch.
2. Make your change in `index.html`.
3. Test it: open the file in a browser, and check at a phone width (about 375px wide). Play a full round on each level. Use `?speed=8` to skip the wait while steeping.
4. Open a pull request. Say what changed and why, and include a screenshot if it changes how things look.

## Reporting bugs and suggesting ideas

Open an issue using one of the templates. For bugs, include your device, browser, and the level you were playing.
