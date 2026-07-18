# ST4 Studio

Webapp zum Erstellen von [Stage Traxx 4](https://stagetraxx.com) Song-Archiven (`.st4s`) —
komplett im Browser, ohne Build und ohne Backend.

**Workflow:** Spotify/YouTube-Link → Titel & Artist · MP3 reinziehen (Track 1 „Original") ·
BPM per TAP oder Auto-Schätzung · Lyrics automatisch via [lrclib.net](https://lrclib.net)
(oft mit LRC-Timecodes) · Band-Songs: Pitch −1, generierter Einzähler-Click (Track 2,
Mutegroup 2, ohne Transposition), MIDI-Zeile aus dem
[MIDI-Helper](https://github.com/j0888/midihelper), Regionen im Waveform markieren ·
Export als `.st4s` → Import in Stage Traxx über *More Options → Import ST4 Files*.

**Einzähler-Click:** Taktarten 2/4 · 3/4 · 4/4 · 5/4 · 6/8 · 7/8 · 9/8 · 12/8 mit korrekten
Betonungen (bei Achtel-Taktarten beziehen sich die BPM auf die punktierte Viertel bzw. bei
7/8 auf die Viertel). Optional **Cue-Ansage**: Der letzte Takt wird mit gesprochener Stimme
angezählt („1, 2, 3, 4" — Deutsch oder Englisch, eingebettete Sprach-Samples, die Beeps
treten dabei in den Hintergrund).

**Optimieren-Modus:** Eine bestehende `.st4s`-Datei laden (auch mit mehreren Songs) —
die App zeigt pro Song eine Diagnose (Lyrics fehlen / ohne Timecodes, BPM fehlt) und kann
automatisch nachbessern: Lyrics-Suche via lrclib.net (vorhandene Lyrics werden nie ungefragt
überschrieben, Vorschläge müssen bestätigt werden), BPM-Schätzung aus dem Archiv-Audio,
Metadaten-Putzen („(Official Video)", „- Topic" …). Beim Export bleiben alle Audio-Dateien
unverändert, nur `share_data.json` wird aktualisiert.

## Benutzung

`index.html` im Browser öffnen — oder via GitHub Pages aufrufen.
Internet wird benötigt (CDN: JSZip, wavesurfer.js; APIs: oEmbed, lrclib).

## Format

Das `.st4s`-Format wurde aus Exporten von Stage Traxx 4.0.17 reverse-engineered
(ZIP mit `share_data.json` + Asset-Ordnern). Es ist proprietär und kann sich mit
App-Updates ändern — keine Gewähr.
