# Discord Game Time Badge Spoofer · Deutsch / English

**🇩🇪 [Zur deutschen Anleitung](#deutsch)** · **🇬🇧 [Jump to English guide](#english)** · **[Original source / Originalquelle](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5)**

![MacBook showing an illustrative Discord interface](assets/images/macbook-discord-de.png)

> **Deutsch:** Unabhängige Dokumentation eines inoffiziellen Skripts von nvckai. Die Bilder sind illustrative Beispiele und keine echten Discord-Screenshots. Die Nutzung kann gegen die Discord-Nutzungsbedingungen verstoßen. Der Originalcode ist nicht enthalten.  
> **English:** Independent documentation for an unofficial script by nvckai. Illustrations are mockups, not real Discord screenshots. Use may violate Discord's terms. Original code is not bundled.

---

## Deutsch

[**🇩🇪 Deutsch**](README_DE.md) · [**🇬🇧 English**](README_EN.md) · [**↗ Original-Gist von nvckai**](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5)

![MacBook mit einer illustrativen Discord-Oberfläche](assets/images/macbook-discord-de.png)

> **Bildhinweis:** Dieses Foto ist ein **generiertes Konzeptbild**, kein echter Screenshot. Die abgebildete Game-Time-Kachel ist eine Illustration und **keine** durch das Skript bereitgestellte Benutzeroberfläche.

> [!WARNING]
> **Inoffizielles Community-Skript — auf eigenes Risiko.** Das Skript manipuliert künstlich erzeugte Spielaktivitäts- und Analyseereignisse. Der Originalautor warnt selbst vor einem möglichen Verstoß gegen die Discord-Nutzungsbedingungen. Die Nutzung kann dein Konto gefährden. Weder Funktion noch Abzeichen-Fortschritt sind garantiert. **Führe keinen fremden Konsolencode aus, den du nicht geprüft hast.**

## Inhalt

1. [Was ist das?](#was-ist-das)
2. [Voraussetzungen](#voraussetzungen)
3. [Schritt-für-Schritt-Anleitung](#schritt-für-schritt-anleitung)
4. [Einstellungen erklärt](#einstellungen-erklärt)
5. [Konsolenausgabe, Stoppen und Kontrolle](#konsolenausgabe-stoppen-und-kontrolle)
6. [Häufige Fragen & Fehler](#häufige-fragen--fehler)
7. [Quellen, Sicherheit und Lizenz](#quellen-sicherheit-und-lizenz)

## Was ist das?

Der [Original-Gist von **nvckai**](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5) enthält ein JavaScript-Snippet, das im **Discord-Desktop-Client** ausgeführt werden soll. Es greift auf interne Discord-Module zu und erstellt synthetische Aktivitätsereignisse für Spielstarts und Spielzeit.

- **Game Time / Spielzeit:** Discord wertet normalerweise die Zeit in erkannten Desktop-Spielen aus.
- **Game Variety / Spielvielfalt:** Discord wertet normalerweise die Anzahl verschiedener erkannter Spiele aus.
- **Nicht Bestandteil dieses Skripts:** Streaming-Abzeichen, Discord-Quests oder ein installierbares Programm mit eigener Oberfläche.

Das Skript ist **kein offizielles Discord-Feature**, keine macOS-App, kein Discord-Bot und keine Website. Es handelt sich um einmalig in der Entwicklerkonsole gestarteten Code. Das hier angebotene Repository enthält **Dokumentation und Bilder**, aber **keine Kopie des Originalskripts**.

## Voraussetzungen

| Benötigt | Details |
|---|---|
| Discord-Desktop-App | Die Browserversion und die Mobile-App werden vom Originalskript nicht unterstützt. |
| Zugang zur Entwicklerkonsole | Laut [Discord-Hilfe](https://support.discord.com/hc/en-us/articles/115001239472-Troubleshooting-Console-Log-Errors) sind **PTB oder Canary** für den Zugriff auf die Konsole vorgesehen. In der regulären App kann sie deaktiviert sein. |
| Eigene Prüfung des Quelltexts | Den JavaScript-Code vor jeder Ausführung lesen und verstehen; keine Zugangsdaten weitergeben. |
| Verständnis der Risiken | Interne Discord-Schnittstellen können sich ändern. Übertragene Daten und Abzeichen können abgelehnt, verzögert oder zurückgesetzt werden. |

**Tastenkombinationen für die Entwicklerwerkzeuge** (bei unterstütztem Desktop-Client):

- **Mac:** `⌥ Option + ⌘ Command + I`
- **Windows:** `Ctrl + Shift + I`

Auf dem Mac ist ausdrücklich **nicht** `Ctrl + Shift + I` gemeint. Die Tastenkombination stammt aus der offiziellen Discord-Anleitung für die Konsole. Wenn sich nichts öffnet, nutze die offiziellen Informationen zu PTB/Canary; versuche nicht, Schutzmechanismen einer regulären App mit unbekannten Hilfsprogrammen zu umgehen.

## Schritt-für-Schritt-Anleitung

### Schritt 1 — Originalcode öffnen und prüfen

1. Öffne den [Original-Gist](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5).
2. Suche den Abschnitt **Snippet** unter „How to use“.
3. Prüfe den vollständigen Code, insbesondere Zugriffe auf `/users/@me`, den Spielkatalog und das interne Analyseziel `/science`.
4. Kopiere **nicht** zufällige Varianten aus Kommentaren oder fremden Webseiten. Verwende, falls überhaupt, ausschließlich den selbst geprüften Originalcode.

**Wichtig:** Die Originaldatei heißt `gametime-badge.md`, obwohl darin ausführbares JavaScript steht. Dieses Dokument enthält das Skript absichtlich nicht, weil im Gist keine ausdrückliche Weiterverbreitungslizenz ersichtlich war.

### Schritt 2 — Discord auf dem Desktop öffnen

1. Starte Discord auf deinem **Mac** oder Windows-PC und melde dich im eigenen Konto an.
2. Öffne, falls dort verfügbar, die Entwicklerwerkzeuge mit der oben genannten Tastenkombination.
3. Wähle oben den Tab **Console** (Konsole).
4. Wenn die Entwicklerkonsole eine Warnung zum Einfügen zeigt: **Nicht blind fortfahren.** Die Aufforderung `allow pasting` ist bei manchen Konsolen eine explizite Freigabe für Einfügen; gib sie nur ein, wenn du die Warnung verstehst und den einzufügenden Code geprüft hast. Nicht jede Discord-Version zeigt diese Abfrage.

![Schematische Darstellung der Entwicklerkonsole](assets/images/01-open-console.png)

*Abbildung 1: Nachgebildete Console-Ansicht. Keine Originalaufnahme; Menüs und Anordnung können abweichen.*

### Schritt 3 — Erst den Testmodus vorbereiten

Im Originalskript befindet sich direkt am Anfang ein Block `const config = { ... }`. Ändere die Werte **im JavaScript-Snippet selbst**. Zum Verständnis eignet sich folgender **Beispielblock**:

```js
const config = {
  totalHours: 120,
  titles: 10,
  batchSize: 5,
  delay: 450,
  wobble: false,
  dryRun: true
};
```

Dieses Beispiel erzeugt **nur eine Testausgabe**, weil `dryRun: true` gesetzt ist. Bei dieser Einstellung soll der Code laut seiner aktuellen Implementierung **keine Aktivitätsereignisse an `/science` senden**. Er greift allerdings weiterhin auf interne Discord-Funktionen zu und ruft Benutzer- und Katalogdaten ab.

![Konfiguration mit eingeschaltetem Testmodus](assets/images/02-config-dry-run.png)

*Abbildung 2: Der Beispielblock zeigt die tatsächlich verwendeten Optionsnamen. Die beigelegte Datei `config.example.json` dient nur als Referenz; das Originalskript liest diese Datei **nicht** automatisch.*

### Schritt 4 — Snippet in der Konsole testen

1. Prüfe noch einmal, dass `dryRun: true` im **kopierten vollständigen Originalskript** steht.
2. Füge dieses vollständige, selbst geprüfte JavaScript-Snippet in die Console ein.
3. Drücke `Enter`, um den Testlauf zu starten.
4. Lies die Konsolenausgaben. Bei einem Testlauf solltest du Zeilen mit **`[dry-run]`** sehen.

> **Nicht verwechseln:** Das hier gezeigte `const config = { ... }` ist **nicht** das gesamte Skript und kann allein keine Funktion ausführen. Eine separate `config.example.json` verändert die Ausführung ebenfalls nicht.

### Schritt 5 — Ergebnis nur als Diagnose verstehen

Ein Testlauf zeigt, wie viele Spiele der Code auswählen und welche simulierten Stunden er berechnen würde. Er bestätigt **nicht**, dass Discord Spielstunden oder Abzeichen anerkennt. Das Originalskript sendet mit `dryRun: false` dagegen künstliche Analyseereignisse an Discord. Das kann gegen die Plattformregeln verstoßen. Diese Anleitung empfiehlt keine tatsächliche Manipulation.

![Schematische Konsolenausgabe im Testmodus](assets/images/03-example-console-output.png)

*Abbildung 3: Beispielwerte für `120` Stunden, `10` Spiele und `5` Spiele pro Batch. Es handelt sich nicht um die Ausgabe eines echten Kontos.*

## Einstellungen erklärt

| Einstellung | Im Original | Bedeutung |
|---|---:|---|
| `totalHours` | `6000` | Geplante **synthetische Ereignisstunden** über alle ausgewählten Spiele hinweg. **Nicht** der gewünschte Endstand des Abzeichens. |
| `titles` | `250` | Maximale Anzahl zufällig ausgewählter, im Katalog geeigneter Spiele. Tatsächlich können es weniger sein. |
| `batchSize` | `25` | Anzahl Spiele pro Übertragungs-/Testdurchlauf (Batch). |
| `delay` | `450` | Grundpause zwischen Batches in Millisekunden; der Code fügt eine kleine zufällige Abweichung hinzu. |
| `wobble` | `false` | Bei `true` werden simulierte Stunden pro Spiel leicht zufällig verändert. |
| `dryRun` | `false` | Bei `true` werden berechnete Batches nur protokolliert, **nicht** als Analyseereignisse verschickt. |

**Rechenbeispiel:** Bei `totalHours: 120` und `titles: 10` sind das ungefähr **12 Stunden je ausgewähltem Spiel**, falls mindestens zehn geeignete Einträge gefunden werden. Der Code wählt Spiele zufällig und benutzt dafür Einträge mit Windows-Executable-Metadaten (`win32`), auch wenn Discord auf einem Mac läuft. Ob Discord diese Ereignisse akzeptiert, ist nicht sichergestellt.

## Konsolenausgabe, Stoppen und Kontrolle

### Woran erkenne ich eine Testausgabe?

Mögliche Meldungen lauten (gekürztes, **fiktives** Beispiel):

```text
[spoofer] connected as demo-user | ... target: 120h across 10 games (~12.0h/game)
[spoofer] [dry-run] batch 1/2 (60.0h)
[spoofer] [dry-run] batch 2/2 (60.0h)
[spoofer] done: 10/10 games forged | total playtime: 120.0h
```

Der Begriff `forged` in der Abschlussmeldung wird vom Originalcode auch im **Testmodus** verwendet. Er ist **kein Nachweis** für eine erfolgreiche Aktualisierung der Discord-Statistik.

### Wie stoppe ich einen bereits gestarteten Lauf?

Solange das Skript in derselben Discord-Konsole aktiv ist, stellt es nach dem Start folgende Funktion bereit:

```js
window.__stopGameTimeForge()
```

Der Stopp wird an einer Batch-Grenze berücksichtigt. Er kann **bereits verschickte** Analyseereignisse **nicht zurücknehmen**. Ein Neustart des Clients macht übertragene Daten ebenfalls nicht rückgängig.

### Wie prüfe ich offizielle Badge-Informationen?

Discord beschreibt **Game Time** und **Game Variety** in seiner [offiziellen deutschsprachigen Hilfe](https://support.discord.com/hc/de/articles/44369363856663-Discord-Profilabzeichen-Was-jedes-Abzeichen-bedeutet). Der Fortschritt basiert auf erkannten Desktop-Spielen und kann verzögert angezeigt werden. Discord nennt außerdem die Einstellung **„Daten verwenden, um mein Discord-Erlebnis zu personalisieren“** als Voraussetzung für die Erfassung.

![Schematische Gegenüberstellung der Badge-Typen](assets/images/04-badge-expectations.png)

*Abbildung 4: Inhaltliche Einordnung, keine echte Profil- oder Abzeichenansicht.*

## Häufige Fragen & Fehler

**Kann ich das im Browser ausführen?**  
Nein. Das Original prüft auf interne Module des Discord-Desktop-Clients und bricht im Browser ab.

**Auf meinem Mac öffnet sich keine Konsole. Was nun?**  
Verwende die Tastenkombination `⌥ + ⌘ + I` und prüfe die [Discord-Hilfe zu PTB/Canary](https://support.discord.com/hc/en-us/articles/115001239472-Troubleshooting-Console-Log-Errors). In der Stable-Version steht die Entwicklerkonsole möglicherweise nicht zur Verfügung. Eine Funktionsgarantie auf macOS gibt es nicht.

**Ich sehe „failed to resolve rest module“ oder „failed to fetch analytics token“.**  
Der Code konnte eine interne Discord-Funktion oder notwendige Daten nicht finden. Solche undokumentierten Schnittstellen können sich ändern. **Keine Zugangstokens veröffentlichen**, keine Drittanbieter-„Fixes“ blind ausführen.

**Wozu dient `allow pasting`?**  
Das ist eine Schutzabfrage mancher Entwicklerkonsolen gegen das unüberlegte Einfügen von Code. Nur nach eigener Überprüfung fortfahren; es ist keine allgemeine Installationsanweisung.

**Mein Badge ändert sich nicht — ist das ein Fehler?**  
Nicht unbedingt. Testläufe senden keine synthetischen Ereignisse. Selbst bei einer Übertragung kann Discord Daten ablehnen oder verzögert verarbeiten. Es gibt keine garantierte Aktualisierungszeit und keinen Supportanspruch gegenüber Discord.

**Setzt `totalHours: 6000` meine gesamte Spielzeit exakt auf 6.000 Stunden?**  
Nein. Die Zahl steuert die Summe der **erzeugten Ereignisdauern**. Sie überschreibt keinen offiziellen Zähler. Mehrfaches Ausführen kann Ereignisse mehrfach erzeugen; die Verarbeitung liegt allein bei Discord.

**Hilft das bei Stream-Stunden oder Quests?**  
Nein. Das Originalskript erzeugt ausschließlich Spielstart- und Spielzeit-Ereignisse. Streaming und Discord-Quests folgen anderen Mechanismen.

**Ist `dryRun: true` vollkommen ungefährlich?**  
Nein. Der Code interagiert weiterhin mit dem eigenen Discord-Client und liest Informationen ab. Allerdings wird laut dem geprüften Quelltext im Testmodus kein künstlicher Event-Batch an den Analyse-Endpunkt gesendet. Sicherheitsprüfung bleibt notwendig.

## Quellen, Sicherheit und Lizenz

- **Autor des Originalskripts:** [nvckai — `gametime-badge.md`](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5)
- **Konsole auf Mac und Windows:** [Discord Support — Troubleshooting Console Log Errors](https://support.discord.com/hc/en-us/articles/115001239472-Troubleshooting-Console-Log-Errors)
- **Offizielle Beschreibung der Abzeichen:** [Discord Support — Profilabzeichen](https://support.discord.com/hc/de/articles/44369363856663-Discord-Profilabzeichen-Was-jedes-Abzeichen-bedeutet)
- **Quellcode:** Im Gist öffentlich einsehbar, hier **nicht enthalten**, weil keine explizite Lizenz zur Weiterverbreitung erkennbar war. Siehe [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md) und [`SOURCE.md`](SOURCE.md).
- **Bilder:** Eigenständig erstellte Illustrationen. Die MacBook-Fotos sind KI-generierte Konzeptbilder. Die Schrittbilder sind schematische, speziell für diese Dokumentation erstellte Darstellungen, **keine verifizierten Screenshots einer Discord-Version**.

Dieses Repository steht in keiner Verbindung zu Discord oder dem Originalautor und wird nicht von ihnen unterstützt.


---

## English

[**🇩🇪 Deutsch**](README_DE.md) · [**🇬🇧 English**](README_EN.md) · [**↗ Original Gist by nvckai**](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5)

![MacBook showing a conceptual Discord interface](assets/images/macbook-discord-en.png)

> **About the image:** This is a **generated concept photo**, not a real screenshot. The Game Time tile is illustrative and **not a user interface supplied by the script**.

> [!WARNING]
> **Unofficial community script — use at your own risk.** The original script fabricates game activity and analytics events. The author warns that this may violate Discord's Terms of Service and put your account at risk. Neither successful execution nor badge progress is guaranteed. **Never execute console code you haven't personally reviewed.**

## Contents

1. [What is this?](#what-is-this)
2. [Requirements](#requirements)
3. [Step-by-step guide](#step-by-step-guide)
4. [Configuration reference](#configuration-reference)
5. [Console output, stopping and checking](#console-output-stopping-and-checking)
6. [FAQ and troubleshooting](#faq-and-troubleshooting)
7. [Sources, safety and licensing](#sources-safety-and-licensing)

## What is this?

The [original Gist by **nvckai**](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5) contains a JavaScript snippet intended to run in the **Discord desktop client**. It accesses internal Discord modules and creates artificial game-launch and game-playtime telemetry events.

- **Game Time:** Discord normally measures total playtime across games detected by its desktop app.
- **Game Variety:** Discord normally measures the number of distinct games it recognizes.
- **Not included:** Streaming badges, Discord Quests, or an installable app with its own interface.

This is **not an official Discord feature**, a macOS app, a Discord bot, or a website. It is code launched from the client’s developer console. This repository provides **documentation and illustrations**, **not a redistributed copy of the original script**.

## Requirements

| Requirement | Details |
|---|---|
| Discord desktop client | The original script does not support the browser or mobile apps. |
| Access to Developer Tools | The [official Discord instructions](https://support.discord.com/hc/en-us/articles/115001239472-Troubleshooting-Console-Log-Errors) refer to **PTB or Canary** for accessing the console. It may be disabled in the stable client. |
| Personal source review | Read the JavaScript before running it. Never share account credentials or tokens. |
| Risk awareness | Discord's undocumented internals can change. Events and badge progress can be ignored, delayed, or reversed. |

**Developer Tools shortcuts** (when supported by the desktop build):

- **macOS:** `⌥ Option + ⌘ Command + I`
- **Windows:** `Ctrl + Shift + I`

On macOS, **do not use** the Windows shortcut. Discord documents these platform-specific shortcuts. If your stable client does not open Developer Tools, consult the official PTB/Canary information instead of installing unknown workarounds.

## Step-by-step guide

### Step 1 — Open and review the original source

1. Visit the [original Gist](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5).
2. Find the **Snippet** section under “How to use”.
3. Examine the complete code, especially its access to `/users/@me`, the game catalog and the internal `/science` analytics endpoint.
4. Avoid unreviewed versions copied from comments or third-party pages. If you proceed at all, use the original code only after checking it yourself.

**Note:** The original file is called `gametime-badge.md` even though it contains executable JavaScript. This repository intentionally does not reproduce that code: no explicit redistribution license was visible on the Gist.

### Step 2 — Open Discord desktop and its console

1. Launch Discord on your **Mac** or Windows PC and sign in to your own account.
2. If supported, open the Developer Tools using the appropriate shortcut above.
3. Select the **Console** tab.
4. Some consoles display a paste protection warning. **Do not ignore it.** The phrase `allow pasting` explicitly unlocks pasting in some consoles, and should only be entered if you understand the warning and have reviewed the script. It does not appear in every Discord build.

![Illustrative developer console mockup](assets/images/01-open-console.png)

*Figure 1: Schematic console layout, not a real screenshot. Labels and placement may differ.*

### Step 3 — Prepare a dry run first

Near the beginning of the original script, locate `const config = { ... }`. Values must be changed **inside the JavaScript snippet**. Here is an **illustrative example configuration**:

```js
const config = {
  totalHours: 120,
  titles: 10,
  batchSize: 5,
  delay: 450,
  wobble: false,
  dryRun: true
};
```

With `dryRun: true`, the current source code only **logs planned batches**, rather than posting fabricated events to `/science`. The code **still** accesses internal Discord modules and retrieves account/catalog information.

![Configuration example with dry run enabled](assets/images/02-config-dry-run.png)

*Figure 2: The option names match the original source. The included `config.example.json` is for reference only; the original code **does not automatically load it**.*

### Step 4 — Test the snippet in the console

1. Confirm that you set `dryRun: true` **inside the complete original script** you reviewed and copied.
2. Paste that complete JavaScript snippet into the Console tab.
3. Press `Enter` to start the dry run.
4. Inspect the logged lines. A test run should include **`[dry-run]`** entries.

> **Important:** The small `const config = { ... }` example shown above is **not a standalone program**. It will not run the original operation by itself. The separate `config.example.json` file also has no effect unless you manually copy the values into the actual script.

### Step 5 — Interpret the results cautiously

A dry run demonstrates how many games are selected and how much synthetic time the code would calculate. It does **not** establish that Discord has credited playtime or badges. Changing to `dryRun: false` makes the original script send fabricated analytics events to Discord, potentially violating the platform's rules. This guide does not recommend doing so.

![Illustrative dry run console output](assets/images/03-example-console-output.png)

*Figure 3: Example values for `120` hours, `10` games and `5` games per batch. This is not a log from a real account.*

## Configuration reference

| Setting | Original default | Meaning |
|---|---:|---|
| `totalHours` | `6000` | Aggregate **synthetic event duration** across selected games; **not** an official badge total to set. |
| `titles` | `250` | Maximum number of randomly selected eligible game entries. Fewer may be available. |
| `batchSize` | `25` | Number of games per request/test batch. |
| `delay` | `450` | Base delay between batches in milliseconds; the script also introduces some random jitter. |
| `wobble` | `false` | When `true`, varies synthetic hours slightly per game. |
| `dryRun` | `false` | When `true`, only logs calculated batches and does **not** post synthetic analytics events. |

**Example:** With `totalHours: 120` and `titles: 10`, the script plans roughly **12 hours per selected game**, provided at least ten suitable game entries exist. It chooses games randomly using catalog entries that include Windows (`win32`) executable information, even when running the client on macOS. Discord accepting any events is **not** guaranteed.

## Console output, stopping and checking

### What does a dry-run log look like?

Possible output (shortened **fictional** example):

```text
[spoofer] connected as demo-user | ... target: 120h across 10 games (~12.0h/game)
[spoofer] [dry-run] batch 1/2 (60.0h)
[spoofer] [dry-run] batch 2/2 (60.0h)
[spoofer] done: 10/10 games forged | total playtime: 120.0h
```

The word `forged` in the final line appears in the original code **even during a dry run**. It does **not** prove that Discord changed any statistics.

### How do I stop a running script?

Once it starts, the original script exposes this function in the **same active console session**:

```js
window.__stopGameTimeForge()
```

The stop flag is checked between batches. It **cannot undo** analytics events that have already been sent. Restarting Discord does not roll back transmitted events either.

### Where can I check official badge rules?

Discord documents **Game Time** and **Game Variety** in its [official profile badge guide](https://support.discord.com/hc/en-us/articles/44369363856663-Discord-Profile-Badges-What-Each-Badge-Means). These badges use desktop-detected game activity, and progress may take time to appear. Discord also requires the setting **“Use data to personalize my Discord experience”** for counting progress.

![Diagram comparing types of badges](assets/images/04-badge-expectations.png)

*Figure 4: Conceptual comparison, not a real profile or badge screenshot.*

## FAQ and troubleshooting

**Does this work in a web browser?**  
No. The original checks for internal modules only available in Discord's desktop client.

**My Mac doesn't open the console. What should I do?**  
Use `⌥ + ⌘ + I` and review the [official Discord PTB/Canary instructions](https://support.discord.com/hc/en-us/articles/115001239472-Troubleshooting-Console-Log-Errors). Developer Tools may not be available in stable. The original script is not guaranteed to work on macOS.

**I see “failed to resolve rest module” or “failed to fetch analytics token”.**  
The script could not locate an internal Discord function or required data. Discord can change undocumented APIs at any time. **Never publish account tokens** or blindly run third-party fixes.

**Why does the Gist mention `allow pasting`?**  
Some developer consoles use it as an anti-self-XSS safeguard. Proceed only after understanding the warning and reviewing the exact code; it is not a general installation step.

**My badge hasn't changed. Is something wrong?**  
Not necessarily. Dry runs send no synthetic events. Even otherwise, Discord may reject or delay processing. There is no guaranteed wait time or official support for this script.

**Will `totalHours: 6000` set my account total to exactly 6,000 hours?**  
No. It determines the total durations of **generated events**; it does not overwrite an official counter. Running the code repeatedly can create repeated events, and only Discord determines how to process them.

**Can I use this for streamed hours or Quests?**  
No. The original only creates game-launch and playtime events. Streaming and Quests are tracked differently.

**Is `dryRun: true` completely risk-free?**  
No. The code still interacts with your logged-in Discord client and retrieves information. But according to the reviewed source, dry-run batches are not posted to the analytics endpoint. Review all code regardless.

## Sources, safety and licensing

- **Original author:** [nvckai — `gametime-badge.md`](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5)
- **Developer Tools on macOS and Windows:** [Discord Support — Troubleshooting Console Log Errors](https://support.discord.com/hc/en-us/articles/115001239472-Troubleshooting-Console-Log-Errors)
- **Official badge descriptions:** [Discord Support — Discord Profile Badges](https://support.discord.com/hc/en-us/articles/44369363856663-Discord-Profile-Badges-What-Each-Badge-Means)
- **Source code:** Available at the original Gist, **not bundled** here because an explicit redistribution license was not visible. See [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md) and [`SOURCE.md`](SOURCE.md).
- **Images:** Original illustrations created for this guide. The MacBook photos are AI-generated concept imagery. The step diagrams are schematic recreations, **not verified screenshots of a specific Discord build**.

This repository is independent and is not affiliated with, endorsed by, or sponsored by Discord or the original script author.
