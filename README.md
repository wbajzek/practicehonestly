# Practice Honestly

A one-page recorder for practising musicians: record, listen back, go practise, repeat.

Everything is in `index.html`. There is no build step, no dependencies and no server-side code. Recordings live only in memory and are replaced by the next take.

## Use

- **Record button**: start or stop a take. Starting a new take discards the previous one.
- **Play button**: listen back. Tap or drag the waveform to jump around.
- **Share button**: opens the system share sheet on iOS, Android and Safari; downloads the file elsewhere.
- **Keyboard**: `R` records or stops, `Space` stops, plays or pauses, arrow keys seek on the waveform.

Recordings are AAC in an `.m4a` file where the browser supports it (Safari, recent Chrome), otherwise WebM or Ogg. Echo cancellation, noise suppression and automatic gain are switched off so instruments sound like themselves.

On computers the page asks for the microphone as soon as it loads and keeps it open while the tab is visible, because a freshly opened mic takes a few seconds to reach its real level. On phones and tablets the mic is opened per take so playback stays at full quality.

Add `?debug` to the URL to see which microphone and audio settings the browser is actually using.

## Run locally

Browsers only allow microphone access over HTTPS or on `localhost`:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Put it on your phone

Host the folder on any static HTTPS host. With GitHub Pages: push this repo, then enable Pages for the `main` branch under Settings → Pages. Open the URL on the phone and use "Add to Home Screen" for a full-screen app.

## License

© 2026 William Bajzek. Licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0). See `LICENSE` for the full text.
