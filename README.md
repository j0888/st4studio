# ST4 Studio

Webapp zum Erstellen von [Stage Traxx 4](https://stagetraxx.com) Song-Archiven (`.st4s`) —
komplett im Browser, ohne Build und ohne Backend.

**Workflow:** Spotify/YouTube-Link → Titel & Artist · MP3 reinziehen (Track 1 „Original") ·
BPM per TAP oder Auto-Schätzung · Lyrics automatisch via [lrclib.net](https://lrclib.net)
(oft mit LRC-Timecodes) · Band-Songs: Pitch −1, generierter Einzähler-Click (Track 2,
Mutegroup 2, ohne Transposition), MIDI-Zeile aus dem
[MIDI-Helper](https://github.com/j0888/midihelper), Regionen im Waveform markieren ·
Export als `.st4s` → Import in Stage Traxx über *More Options → Import ST4 Files*.

## Benutzung

`index.html` im Browser öffnen — oder via GitHub Pages aufrufen.
Internet wird benötigt (CDN: JSZip, wavesurfer.js; APIs: oEmbed, lrclib).

## Format

Das `.st4s`-Format wurde aus Exporten von Stage Traxx 4.0.17 reverse-engineered
(ZIP mit `share_data.json` + Asset-Ordnern). Es ist proprietär und kann sich mit
App-Updates ändern — keine Gewähr.
