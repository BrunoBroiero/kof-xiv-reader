# KOF XIV Reader

[English](README.md) · [Español](README.es.md) · **Deutsch** · [Français](README.fr.md) ·
[Italiano](README.it.md) · [Português](README.pt.md) · [日本語](README.ja.md) ·
[한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

> Diese Übersetzung wurde nicht von einer deutschsprachigen Person geprüft. Korrekturen
> sind willkommen.

Eine Screenreader-Mod für **THE KING OF FIGHTERS XIV** (Steam, PC). Sie liest die Menüs,
die Geschichte, die Listen und den Text auf dem Bildschirm mit dem Screenreader vor, den du
schon benutzt — NVDA, JAWS und die anderen —, damit das Spiel ohne Sehen spielbar ist.

Sie spricht **in der Sprache, in der das Spiel läuft**, welche der elf es auch ist, denn
fast alles, was sie sagt, ist der Text des Spiels selbst und nicht der der Mod.

## Was sie liest

- **Menüs und Optionen**: der Bildschirm, den du betreten hast, der Eintrag mit dem Fokus
  und seine Beschreibung; der Name einer Einstellung, worauf sie steht und was eine
  Änderung bewirkt hat.
- **Story-Modus**: jede Dialogzeile und jedes Ende — in diesem Spiel ohne Sprachausgabe und
  daher ohne die Mod nicht zugänglich.
- **Kommandolisten**: wie ein Move ausgeführt wird, in fünf Schreibweisen (F10 wechselt):
  die Worte des Spiels, Arcade, Arcade vereinfacht, FGC, FGC vereinfacht.
- **Trials und Tutorial**: die geforderte Combo, Schritt für Schritt, und der Text jeder
  Lektion mit den Eingaben im Satz.
- **Charakterauswahl**: die Kämpfer, das Anpassungsfenster (Farbe und Kostüm) und der
  Reihenfolge-Bildschirm, samt Gegner und den Bossstufen drei gegen eins.
- **Spielerdaten**: Aufzeichnungen, Ranglisten, dein Profil und deine Karte,
  Charakteraufzeichnungen und -daten.
- **Galerie**: Illustrationen, Gegenstände, Filme und Klänge, und was noch gesperrt ist.
- **Der Kampf selbst, auf Anfrage**: Lebensbalken, Powerbalken und die Uhr des
  Zeitangriffs, aus dem HUD des Spiels gelesen (siehe Tasten unten).
- **Online**: das Menü, der Ranglistenkampf mit seiner ersten Frage und seinen
  Sucheinstellungen, die Kampfliste, die Wiederholungen samt der Teams, die sie gespielt
  haben, und das Online-Profil.
- **Hinweise, Bestätigungen und Systemmeldungen**, wo sie auch erscheinen.

Tastenhinweise, Layout-Füllungen und Seitenzähler werden **absichtlich nicht** gesprochen.

## Was noch fehlt

- **Online-Räume**: die Lobbys für freie Kämpfe und Online-Training — Spielerliste,
  Warteschlange und Wartebildschirme.
- **Die Bildschirme um einen Online-Kampf**: der gefundene Gegner und die Online-Ergebnisse
  mit Rangpunkten. Beide brauchen eine zweite Person, also ist keines davon getestet.
- **Eine Wiederholung ansehen**: die Steuerung der Wiedergabe.

## Voraussetzungen

- Die Steam-PC-Version von KOF XIV.
- Ein laufender Screenreader (NVDA, JAWS, ...). Die Mod spricht über
  [PRISM](https://github.com/ethindp/prism), das den gerade aktiven benutzt.
- Windows x64.

## Installation

Kopiere drei Dateien in den Spielordner, neben `kofxiv.exe`:

```
winmm.dll     die Mod
prism.dll     PRISM
tolk.dll      die NVDA/JAWS-Anbindung von PRISM
```

Sonst ändert sich nichts, und keine Spieldatei wird geändert oder umbenannt. Zum
Deinstallieren lösche diese drei Dateien.

Die Mod wird geladen, weil das Spiel `winmm.dll` benutzt; die Kopie im Spielordner leitet
jede Funktion dieser Bibliothek an die echte in `System32` weiter, sodass nichts anderes im
Prozess etwas davon merkt.

## Tasten

| Taste | Was sie tut |
|-------|-------------|
| Oben / Unten | Durch das gehen, was ein Bildschirm bereithält — eine Kommandoliste, eine Punktetabelle, den Abspann. Bei offenem Dialog bewegen sie dessen Auswahl |
| F1 | Alles sagen, was der Bildschirm bereithält. Bei offenem Dialog: die Meldung, was sie zeigt (Spieler, Datum und Modus einer Wiederholung) und die Option mit Fokus |
| F2 | Einen Schritt zurück. Bei offenem Dialog: die Meldung und die Option mit Fokus |
| F3 | Einen Schritt vor. Bei offenem Dialog: was sie über die Sache zeigt, nach der sie fragt |
| Rechter Stick, im Kampf | Nach Seiten, wie die Balken auf dem Bildschirm liegen: links das Leben von Spieler 1, rechts das von Spieler 2; oben die Powerbalken von Spieler 1, unten die von Spieler 2 |
| Klick des rechten Sticks, im Kampf | Beide Spieler zusammen: "PLAYER 1, 62%, POWER 2, PLAYER 2, 40%, POWER 1". Im Zeitangriff die bisher gebrauchte Zeit |
| Rechter Stick, sonst | F1 bis F3 für das Gamepad: oben ist F2, unten ist F3, links und rechts sind F1, der Klick wechselt die Schreibweise wie F10. In einem Trial oder einer Lektion bleibt es so, auch der Klick: dort gehören die Richtungen dem Kämpfer, und die Eingaben zählen mehr als die Balken |
| F10 | Wechselt die Schreibweise der Eingaben, durch die fünf Varianten |
| F4 | Menülesen ein- oder ausschalten |
| F7 | Aufhören zu sprechen |
| F8 | Sagt, welchen Screenreader die Mod gefunden hat — überhaupt etwas zu hören heißt, die Mod läuft |
| F9 | Markiert diesen Moment im Protokoll, stumm: "hier ist das Problem" |
| F5 | Diagnose: die nächsten Übersetzungen ausgeben und den Film nach dem fragen, was die Mod nicht lesen kann |
| F6 | Das Diagnoseprotokoll ein- oder ausschalten (standardmäßig ein) |

In einem **Survival**-Lauf sagen F1 bis F3 und die Richtungen des Sticks das verbleibende
Leben in Prozent; in einem **Zeitangriff** die bisher gebrauchte Zeit, im Format der
Ergebnisse.

Was ein Bildschirm bereithält, endet an seinen Enden und beginnt nicht von vorn: über das
letzte Stück hinaus sagt nichts, und vor das erste zurück auch nicht. Diese Stille ist der
Anfang und das Ende — die Schritte einer Combo, die Sätze einer Lektion, die Zeilen einer
Tabelle. Was als ein einziges Stück gehalten wird, hat keine Enden und wird jedes Mal ganz
gesagt.

**Die Mod hat keine eigenen Worte.** Alles, was sie sagt, ist Text des Spiels, in der
Sprache des Spiels, oder ein Name. Wo sie etwas Eigenes sagen müsste — eine Lesetaste ohne
etwas zu lesen, eine Markierung im Protokoll —, sagt sie nichts, und die Stille ist die
Antwort. Schalter antworten mit den Worten des Spiels für ein und aus.

## Was die Mod schreibt

`KofXIVReader.learned`, neben dem Protokoll, hält das Wenige, das das Spiel nur einmal
zeigt: welche Kämpfer eine Kostümzeile im Anpassungsfenster haben. Das Spiel zeichnet diese
Zeile beim ersten Mal und erwähnt sie danach nie wieder, also ist Sehen der einzige Weg, es
zu erfahren. Es aufzuschreiben heißt, dass die Mod einmal hinterherhinkt statt bei jedem
Start. Lösche die Datei, und sie lernt alles neu.

## Ein Problem melden

Drücke im Spiel **F6**, um das Protokoll einzuschalten, **F9** in dem Moment, in dem etwas
falsch vorgelesen wird, und beende dann normal. Das Protokoll ist `KofXIVReader.log` im
Spielordner, die vorige Sitzung liegt daneben als `KofXIVReader.prev.log`. Es verzeichnet,
was das Spiel angezeigt hat, in welchem Feld, von welchem Bildschirm und was die Mod dazu
gesagt hat — genug, um zu sehen, was sie hätte sagen sollen. Du musst nicht aufschreiben,
was du gehört hast: im Protokoll steht der genaue Wortlaut.

## Quellcode

Der Quellcode ist noch nicht öffentlich. Er wird es, sobald die Mod im Gebrauch angekommen
ist; das ist eine Phase, keine Grundsatzentscheidung. Was hier erscheint, darf frei
heruntergeladen und benutzt werden.

Die Mod bringt zwei fremde Dateien mit, `prism.dll` und `tolk.dll`, beide von
[PRISM](https://github.com/ethindp/prism) unter der Mozilla Public License 2.0 — siehe
[THIRD-PARTY.md](THIRD-PARTY.md).

## Übersetzungen

Dieses README gibt es in allen Sprachen, die das Spiel unterstützt. Nur die englische und
die spanische Fassung wurden von Sprechern geprüft; die übrigen nicht, und Korrekturen sind
willkommen: ein unbeholfener Satz lässt sich verbessern, eine fehlende Sprache lässt ihren
Spielern nichts zu verbessern.
