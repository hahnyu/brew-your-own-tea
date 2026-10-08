# Brew Your Own Tea

A calm, browser-based green tea brewing game for middle and high school classes. Players brew a cup (leaves, water heat, pour, steep), then use their senses to work out the tea's main flavors. It's a single HTML file with no libraries, no build step, and no data collection.

**Play it:** https://hahnyu.github.io/brew-your-own-tea/

## How it plays

1. **Brew:** measure the leaves, heat the water, pour, and steep. Heat, time, amount of leaves and amount of water all change the tea.
2. **Use your senses:** smell, look, feel, then taste. Brewing mistakes change every clue. Over-steeping makes the tea bitter and dry. A weak brew makes it pale and faint.
3. **Guess:** pick the tea's main flavors from the ten-note tasting wheel (nutty, herbal, grassy, floral, berry, sweet, refreshing, spicy, umami, bitter).
4. **Reflect:** see your score, whether it came out "delicious", and a "How do you feel?" check-in.

Three levels: Gentle (1 main flavor, guides shown), Mindful (2, tips only), Master (3, no guides).

## Run it locally

No install needed. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000. Add `?speed=8` to the URL to make the steeping step run 8x faster while testing.

## How the code is organized

Everything lives in [`index.html`](index.html), in this order:

| Section | What it does |
|---|---|
| CSS | Layout, theme colors (CSS variables at the top), touch-friendly buttons |
| HTML screens | `title`, `game` (the SVG scene and control panel), `observe`, `guess`, `result` |
| Data | The tasting wheel notes (`NOTES`, `WHEEL`), the ideal brewing ranges (`IDEAL`), and the facts and messages |
| Sound | Web Audio only, with no audio files. Includes the volume slider and mute |
| Brew model | `brewLook` turns heat, leaves, water and time into strength, bitterness and color. `tasteOf` turns that into the wheel |
| Game flow | Steps, the hold-button input, the scene drawing loop, scoring and results |

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). Good first ideas:

- A second-infusion bonus round (shorter steep, slightly hotter water)
- More mystery tea profiles or a class mode with a shared code
- Accessibility improvements (screen reader labels, high-contrast mode)
- Translations
- Tuning the difficulty and the scoring

## Credits

The tasting wheel and the farm and health facts come from the Green Tea education presentation by Wild Orchard. The wheel is based on their tea tasting card.
