# KOF XIV Reader

**English** · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md) ·
[Italiano](README.it.md) · [Português](README.pt.md) · [日本語](README.ja.md) ·
[한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

A screen-reader mod for **THE KING OF FIGHTERS XIV** (Steam, PC). It speaks the game's
menus, story, lists and on-screen text through whatever screen reader you already use —
NVDA, JAWS, and the rest — so the game can be played without sight.

It speaks in **the language the game is running in**, whichever of the eleven that is,
because almost everything it says is the game's own text rather than the mod's.

## What it reads

- **Menus and options**: the screen you entered, the entry that has focus and its
  description; a setting's name, what it is set to, and what changing it did.
- **Controls**: the controls screen, from the options and from the pause menu — which
  device each player uses, what every action is bound to, and the binding itself: the
  key or button taken and any it displaced. Keyboard keys are read as the game writes
  them. A pad's buttons are not read yet — the bindings the game hands its screen are
  still being decoded — so a pad's rows name the action alone.
- **Story mode**: every line of dialogue and every ending — unvoiced in this game, and so
  unreadable without this.
- **Command lists**: how a move is performed, in five notations (F10 switches between
  them): the game's own words, arcade, arcade simplified, FGC, FGC simplified.
- **Trials and the tutorial**: the combo being asked for, step by step, and each lesson's
  text with its inputs set into the prose.
- **Character select**: fighters, the customise panel (colour and costume), and the order
  screen, including who the fight is against and the three-against-one boss stages.
- **Player data**: records, rankings, your profile and card, character records and data.
- **Gallery**: illustrations, items, movies and sounds, with what is still locked.
- **The fight itself, on request**: life, power bars and a time attack's clock, read off
  the game's own HUD (see the keys below).
- **Online**: the menu, ranked match with its first-time question and its search settings,
  the battle list, replays with the teams that fought them, and the online profile.
- **Notices, confirmations and system messages**, wherever they appear.

Button hints, layout padding and page counters are deliberately **not** spoken.

## Not covered yet

- **Online rooms**: free match and online training lobbies — the player list, the queue
  and the waiting screens.
- **The screens around an online match**: the opponent found, and the online results with
  rank points. Both need another person to reach, so neither has been tested.
- **Watching a replay**: the playback controls.

## Requirements

- The Steam PC release of KOF XIV.
- A running screen reader (NVDA, JAWS, ...). The mod speaks through
  [PRISM](https://github.com/ethindp/prism), which uses whichever one is active.
- Windows x64.

## Download

The latest build is under [Releases](../../releases): a zip with the three files below and
this README. Nothing to install beyond copying them.

## Installing

Copy three files into the game folder, next to `kofxiv.exe`:

```
winmm.dll     the mod
prism.dll     PRISM
tolk.dll      PRISM's NVDA/JAWS backend
```

Nothing else changes, and no game file is modified or renamed. To uninstall, delete those
three files.

The mod loads because the game imports `winmm.dll`; the copy in the game folder forwards
every one of that library's functions to the real one in `System32`, so nothing else in
the process notices it is there.

## Keys

| Key | What it does |
|-----|--------------|
| Up / Down | Walk through what a screen is holding — a command list, a score table, the credits. With a dialog open, they move its cursor |
| F1 | Say the whole of what the screen is holding. With a dialog open: its message, what it shows (a replay's players, date and mode) and the option with focus |
| F2 | A step back through what is held. With a dialog open: its message and the option with focus |
| F3 | A step forward. With a dialog open: what it shows about the thing it asks about |
| Right stick, in a fight | By side, as the bars sit on screen: left is player 1's life, right player 2's; up is player 1's power bars, down player 2's |
| Right stick click, in a fight | Both players whole: "PLAYER 1, 62%, POWER 2, PLAYER 2, 40%, POWER 1". In a time attack run, the time taken so far |
| Right stick, elsewhere | F1 to F3 for a pad: up is F2, down is F3, left and right are F1, the click changes notation as F10 does. In a trial or a lesson being played it stays this way, click included: there the arrows belong to the fighter, and the inputs matter more than the bars |
| F10 | Change how a move's input is said, through the five notations |
| F11, or both stick clicks on a pad | Turn the whole reader off, and on again. Off it says nothing at all; these two still answer, and every run starts with it on |
| F7 | Stop talking |
| F8 | Say which screen reader the mod found — hearing it at all means the mod is alive |
| F9 | Mark this moment in the log, silently: "the problem is here" |
| F5 | Diagnostics: dump the next translations, and ask the movie for what the mod cannot read |
| F6 | Turn the diagnostic log on or off (on by default) |

During a **survival** run, F1 to F3 and the stick's directions say the life left as a
percentage; during a **time attack** run, the time taken so far, as the results write it.

What a screen holds stops at its ends rather than coming round again: pushing past the last
piece says nothing, and neither does pushing back past the first. That silence is where it
begins and where it finishes — a combo's steps, a lesson's sentences, the rows of a table.
Something held as a single piece has no ends to be at, and says itself every time it is
asked for.

**The mod has no voice of its own.** Everything it says is the game's text, borrowed in the
language the game is running in, or a name. Where it would otherwise have to say something
of its own — a reading key pressed with nothing to read, a mark dropped in the log — it says
nothing, and silence is the answer. Toggles answer with the game's own words for on and off.

## What the mod writes

`KofXIVReader.learned`, beside the log, holds the few things the game only ever shows once
— which fighters have a costume row on the customise panel. The screen draws that row the
first time it has to appear and never mentions it again, so being shown is the only way to
find out. Recording it means the mod is a step behind once rather than every time it
starts. Delete the file to have it all learnt again.

`KofXIVReader.settings`, beside it, holds what you chose rather than what the game showed:
for now, the notation commands are read in. Being turned off is deliberately not kept — a
mod that remembered that would start a silent game with nothing to say why.

## Reporting a problem

Press **F6** in game to turn the log on, press **F9** at the moment something reads wrong,
then quit normally. The log is `KofXIVReader.log` in the game folder, and the previous
session is kept alongside it as `KofXIVReader.prev.log`. It records what the game
displayed, which widget it went to, which screen it came from, and what the mod said about
it — enough to see what it should have said instead. There is no need to write down what
you heard: the log already has the exact wording.

## How it works

KOF XIV's interface is Scaleform GFx with ActionScript 3, and it localises text the
Scaleform way: ActionScript hands the game a key like `$MAINMENU_STORY`, and the game
looks it up. Every title, entry, description and message in the game passes through that
one call, which is where the mod listens — one hook covering every screen, present and
future, rather than code written per screen.

Each string arrives named after the widget receiving it, and it is the *widget* that is
classified, never the screen, so a screen nobody has looked at yet is already readable.

The fight's own numbers are not text at all: the game draws its HUD itself. Those are read
from the HUD's own state, reached through the game's RTTI and the code that builds it, and
a time attack's clock is unscrambled the same way the game unscrambles it to draw it.

Nothing is hardcoded to an address: the mod finds the game's Scaleform entry points by the
shape of its own code, and its translator through the game's own RTTI, so a game update
that moves code around does not break it.

## Source

The source is not public yet. It will be, once the mod has settled into use; this is a
stage, not a policy. What ships here is free to download and use.

The mod carries two files it did not write, `prism.dll` and `tolk.dll`, both from
[PRISM](https://github.com/ethindp/prism) under the Mozilla Public License 2.0 — see
[THIRD-PARTY.md](THIRD-PARTY.md).

## Translations

This README ships in every language the game supports. Only the English and Spanish ones
have been checked by a speaker; the rest were translated without one, and corrections are
welcome — a clumsy sentence can be fixed, a missing language leaves its players nothing to
correct.
