# GAMBIT JACKPOT

Schach gegen Bots mit Spielautomat, 18 Sammelfiguren, freien Decks und Spezialattacken. Dazu 1 gegen 1 auf einem Gerät.
Gebaut für Handys und Tablets (iOS und Android), installierbar als App. **Wie die Installation geht, steht in `ANLEITUNG.md`.**

## Spielmodi

| Modus | Beschreibung |
|---|---|
| Kampf | 5 Bots nacheinander. Den nächsten Bot schaltest du frei, indem du den vorherigen besiegst. Siege bringen EP. |
| 1 gegen 1 | Zwei Spieler auf einem Gerät. Alle 18 Figuren frei, Special-Stufe und Budget einstellbar, das Brett dreht sich zum Spieler am Zug. |
| Trainingsplatz | Aus dem Codex ("Ausprobieren") oder dem Deck-Editor. Beide Seiten spielbar, Specials unbegrenzt, Züge zurücknehmbar. |

## Bedienung

- Figur antippen, dann Zielfeld antippen (oder ziehen).
- Special: Karte unten antippen, dann Figur und Ziel antippen. Flächen-Specials mit "Los!" auslösen. Das X bricht ab.
- Pause-Knopf oben links: Remis anbieten, Aufgeben, Zugliste, Ton, Menü.
- Deck-Editor: Karte antippen, dann Feld antippen. Figuren auf dem Brett ziehen oder tauschen, aus dem Brett ziehen entfernt sie. Rechtsklick (Maus) leert ein Feld.

## Dateien

| Datei | Inhalt |
|---|---|
| `index.html` | Grundgerüst, App-Metadaten, lädt alle Skripte |
| `manifest.webmanifest`, `sw.js`, `icons/` | Installierbare App, Offline-Modus, App-Icons |
| `fonts/` | Erica One und National Park (SIL Open Font License, Lizenztexte liegen bei) |
| `css/style.css` | Komplettes Design |
| `js/config.js` | **Alle Balancing-Zahlen**: EP, Kosten, Automat-Chancen, Deck-Budget, Bots, Specials, 1-gegen-1-Optionen |
| `js/pieces.js` | Die 18 Figuren: Bewegung, Werte, Deck-Kosten, Specials, Grafik |
| `js/engine.js` | Schachregeln, Zuggenerator, Statuseffekte, Matt/Patt/Remis |
| `js/ai.js` | Bot (Alpha-Beta-Suche) |
| `js/icons.js` | Alle Icons als eigene Grafiken |
| `js/match.js` | Match-Ablauf, Specials-Auswahl, 1 gegen 1, EP-Abrechnung, Bot-Avatare |
| `js/ui-board.js` | Brett, Eingabe, Animationen aller Specials |
| `js/fx.js` | Partikel, Treffer-Sterne, Wackeln, Konfetti |
| `js/ui-screens.js` | Startscreen, Navigation, Codex, Optionen, 1-gegen-1-Setup, Anleitung |
| `js/deck.js`, `js/slot.js`, `js/training.js` | Deck-Editor, Spielautomat, Trainingsplatz |
| `js/save.js`, `js/audio.js`, `js/main.js` | Spielstand, Sounds, Start |

## Balancing ändern

Alles in `js/config.js`. Nach Änderungen an einer online gestellten Version in `sw.js` die `VERSION` hochzählen (siehe ANLEITUNG).

## Getestet

- Schachregeln mit Perft-Tests (Startstellung bis Tiefe 4, Kiwipete bis Tiefe 3) exakt.
- 300 Zufallspartien mit allen Figuren und Specials ohne Fehler.
- Layout auf iPhone SE, iPhone 13, iPhone 15 Pro Max, Pixel 7, Galaxy S9+, iPad hoch und quer, iPad Pro quer, Galaxy Tab: keine Überlappungen, kein seitliches Scrollen, Match passt ohne Scrollen auf den Bildschirm.
- Offline-Modus (Service Worker) über einen lokalen Server.
