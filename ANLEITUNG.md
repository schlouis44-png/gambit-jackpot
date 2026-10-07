# Gambit Jackpot als App installieren

Gambit Jackpot ist eine **installierbare Web-App (PWA)**. Nach der Installation liegt sie mit eigenem Icon auf dem Homescreen, startet im Vollbild ohne Browser-Leisten und läuft auch ohne Internet.

Damit das klappt, muss der Spielordner **einmal online liegen** (über `https://`). Das ist kostenlos und dauert ungefähr 10 Minuten. Danach installierst du die App auf jedem Gerät mit zwei Fingertipps.

> Warum nicht einfach eine Datei aufs Handy kopieren?
> iPhones und iPads installieren grundsätzlich keine App-Dateien außerhalb des App Stores. Dafür bräuchtest du einen Mac und ein Apple-Entwicklerkonto (99 € pro Jahr). Der Weg über den Homescreen funktioniert dagegen auf **allen** Geräten. Für Android gibt es zusätzlich den Weg zur echten APK-Datei (Schritt 4).

---

## Schritt 1: Spiel online stellen (einmalig)

### Weg A: GitHub Pages (empfohlen, dauerhaft kostenlos)

1. Auf [github.com](https://github.com) ein kostenloses Konto anlegen.
2. Oben rechts auf **+** und dann **New repository** tippen.
3. Name: `gambit-jackpot`, auf **Public** lassen, **Create repository**.
4. Auf der neuen Seite **uploading an existing file** anklicken.
5. Den **Inhalt** des Ordners `gambit-jackpot` hineinziehen (also `index.html`, `sw.js`, `manifest.webmanifest` und die Ordner `css`, `js`, `fonts`, `icons`). Unten auf **Commit changes**.
6. Im Repository auf **Settings**, links **Pages**. Bei **Branch** `main` und `/ (root)` wählen, **Save**.
7. Nach 1 bis 2 Minuten steht oben deine Adresse, zum Beispiel
   `https://DEINNAME.github.io/gambit-jackpot/`

### Weg B: Netlify (ganz schnell zum Testen)

1. [app.netlify.com/drop](https://app.netlify.com/drop) öffnen.
2. Den ganzen Ordner `gambit-jackpot` in das Feld ziehen.
3. Du bekommst sofort eine Adresse. Damit sie dauerhaft bleibt, ein kostenloses Konto anlegen und die Seite übernehmen ("claim").

---

## Schritt 2: Auf iPhone oder iPad installieren

1. Die Adresse in **Safari** öffnen (wichtig: Safari, nicht Chrome).
2. Unten (iPad: oben) auf **Teilen** tippen, das Quadrat mit dem Pfeil nach oben.
3. Runterscrollen, **Zum Home-Bildschirm** tippen, dann **Hinzufügen**.
4. Fertig. Gambit Jackpot liegt jetzt mit eigenem Icon auf dem Homescreen und startet im Vollbild.

## Schritt 3: Auf Android installieren (Handy und Tablet)

1. Die Adresse in **Chrome** öffnen.
2. Oben rechts auf die **drei Punkte** tippen, dann **App installieren** (manchmal heißt es "Zum Startbildschirm hinzufügen"). Oft erscheint auch direkt ein Hinweis unten.
3. **Installieren** bestätigen.
4. Chrome erstellt daraus eine echte installierte App. Sie taucht in der App-Übersicht auf wie jede andere App.

## Schritt 4 (optional): Echte APK-Datei für Android

Wenn du eine `.apk`-Datei willst, die du weitergeben oder später in den Play Store bringen kannst:

1. [pwabuilder.com](https://www.pwabuilder.com) öffnen.
2. Deine Adresse aus Schritt 1 eingeben, **Start**.
3. **Package for stores**, dann bei **Android** auf **Generate Package**.
4. Die ZIP-Datei herunterladen und entpacken. Darin liegt eine APK zum Testen.
5. Die APK aufs Android-Gerät kopieren und öffnen. Android fragt einmal, ob Installationen aus dieser Quelle erlaubt sind.

Die APK lädt das Spiel von deiner Adresse aus Schritt 1, die Seite muss also online bleiben.

---

## Ohne Installation am PC spielen

Einfach `index.html` doppelklicken. Das Spiel läuft dann im Browser, nur der Offline-Modus ist so nicht aktiv (der braucht `https://`).

## Updates veröffentlichen

1. Geänderte Dateien hochladen (bei GitHub einfach erneut hochladen und überschreiben).
2. In `sw.js` oben die Zeile `const VERSION = 'gambit-jackpot-v2.0.0';` hochzählen, zum Beispiel auf `v2.0.1`.
   Ohne diesen Schritt behalten bereits installierte Apps die alten Dateien.
3. Die App auf dem Gerät einmal schließen und neu öffnen, dann lädt sie die neue Version.

## Spielstand

- Der Spielstand liegt auf dem jeweiligen Gerät. Jedes Gerät hat seinen eigenen.
- Unter **Optionen > Spielstand > Exportieren** kannst du ihn sichern und auf einem anderen Gerät mit **Importieren** laden.
- Wird die App gelöscht, ist auch der Spielstand weg. Vorher exportieren.
