# KOF XIV Reader

[English](README.md) · [Español](README.es.md) · [Deutsch](README.de.md) ·
[Français](README.fr.md) · **Italiano** · [Português](README.pt.md) ·
[日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) ·
[繁體中文](README.zh-TW.md)

> Questa traduzione non è stata controllata da una persona di lingua italiana. Le
> correzioni sono benvenute.

Una mod con lettore di schermo per **THE KING OF FIGHTERS XIV** (Steam, PC). Legge i menu,
la storia, gli elenchi e il testo a schermo con il lettore di schermo che già usi — NVDA,
JAWS e gli altri — così il gioco si può giocare senza vedere.

Parla **nella lingua in cui è impostato il gioco**, qualunque delle undici sia, perché
quasi tutto ciò che dice è il testo del gioco stesso e non parole della mod.

## Cosa legge

- **Menu e opzioni**: la schermata in cui sei entrato, la voce che ha il focus e la sua
  descrizione; il nome di un'impostazione, su cosa è impostata e cosa ha fatto la modifica.
- **Modalità storia**: ogni battuta di dialogo e ogni finale — senza voce in questo gioco, e
  quindi inaccessibili senza questo.
- **Liste dei comandi**: come si esegue una mossa, in cinque notazioni (F10 le cambia): le
  parole del gioco, arcade, arcade semplificata, FGC, FGC semplificata.
- **Prove e tutorial**: la combo richiesta, passo per passo, e il testo di ogni lezione con
  i comandi dentro la frase.
- **Selezione dei personaggi**: i lottatori, il pannello di personalizzazione (colore e
  costume) e la schermata dell'ordine, con l'avversario e le fasi boss tre contro uno.
- **Dati giocatore**: registri, classifiche, il tuo profilo e la tua scheda, registri e dati
  dei personaggi.
- **Galleria**: illustrazioni, oggetti, filmati e suoni, e ciò che è ancora bloccato.
- **Il combattimento stesso, su richiesta**: vita, barre di potenza e il cronometro della
  modalità a tempo, letti dall'HUD del gioco (vedi i tasti qui sotto).
- **Online**: il menu, la partita classificata con la sua domanda iniziale e le sue
  impostazioni di ricerca, l'elenco delle sfide, i replay con le squadre che li hanno
  giocati, e il profilo online.
- **Avvisi, conferme e messaggi di sistema**, dove compaiano.

I suggerimenti dei tasti, il riempimento del layout e i contatori di pagina **non** vengono
letti, di proposito.

## Cosa non copre ancora

- **Le stanze online**: sfida libera e allenamento online — l'elenco dei giocatori, la coda
  e le schermate di attesa.
- **Le schermate attorno a una partita online**: l'avversario trovato e i risultati online
  con i punti di rango. Entrambe richiedono un'altra persona, quindi nessuna è stata
  provata.
- **Guardare un replay**: i comandi della riproduzione.

## Requisiti

- La versione Steam per PC di KOF XIV.
- Un lettore di schermo in esecuzione (NVDA, JAWS, ...). La mod parla tramite
  [PRISM](https://github.com/ethindp/prism), che usa quello attivo.
- Windows x64.

## Installazione

Copia tre file nella cartella del gioco, accanto a `kofxiv.exe`:

```
winmm.dll     la mod
prism.dll     PRISM
tolk.dll      il ponte NVDA/JAWS di PRISM
```

Non cambia nient'altro, e nessun file del gioco viene modificato o rinominato. Per
disinstallare, elimina quei tre file.

La mod si carica perché il gioco usa `winmm.dll`; la copia nella cartella del gioco inoltra
tutte le funzioni di quella libreria a quella vera, in `System32`, così nient'altro nel
processo si accorge che c'è.

## Tasti

| Tasto | Cosa fa |
|-------|---------|
| Su / Giù | Scorrono quello che la schermata tiene — una lista di comandi, una tabella di punteggi, i titoli di coda. Con una finestra di dialogo aperta, muovono il suo cursore |
| F1 | Dice tutto quello che la schermata tiene. Con una finestra di dialogo: il messaggio, ciò che mostra (i giocatori di un replay, la data e la modalità) e l'opzione selezionata |
| F2 | Un passo indietro. Con una finestra di dialogo: il messaggio e l'opzione selezionata |
| F3 | Un passo avanti. Con una finestra di dialogo: ciò che mostra sull'oggetto della domanda |
| Stick destro, in combattimento | Per lato, come stanno le barre sullo schermo: a sinistra la vita del giocatore 1, a destra quella del giocatore 2; in alto le barre di potenza del giocatore 1, in basso quelle del giocatore 2 |
| Clic dello stick destro, in combattimento | Entrambi i giocatori insieme: "PLAYER 1, 62%, POWER 2, PLAYER 2, 40%, POWER 1". Nella modalità a tempo, il tempo trascorso |
| Stick destro, altrove | F1 a F3 per il pad: su è F2, giù è F3, sinistra e destra sono F1, il clic cambia la notazione come F10. In una prova o una lezione resta così, clic compreso: lì le direzioni sono del personaggio, e i comandi contano più delle barre |
| F10 | Cambia il modo in cui si dice un comando, tra le cinque notazioni |
| F4 | Attiva o disattiva la lettura dei menu |
| F7 | Smette di parlare |
| F8 | Dice quale lettore di schermo ha trovato la mod — sentire qualcosa significa già che la mod è attiva |
| F9 | Segna questo momento nel registro, in silenzio: "il problema è qui" |
| F5 | Diagnostica: scaricare le prossime traduzioni e chiedere al filmato ciò che la mod non riesce a leggere |
| F6 | Attiva o disattiva il registro di diagnostica (attivo per impostazione predefinita) |

In **sopravvivenza**, F1 a F3 e le direzioni dello stick dicono la vita rimasta in
percentuale; nella **modalità a tempo**, il tempo trascorso, nel formato dei risultati.

Quello che una schermata tiene finisce ai suoi estremi invece di ricominciare: andare oltre
l'ultimo pezzo non dice nulla, e tornare prima del primo nemmeno. Quel silenzio è l'inizio e
la fine — i passi di una combo, le frasi di una lezione, le righe di una tabella. Ciò che è
tenuto come un pezzo unico non ha estremi e si dice intero ogni volta che lo chiedi.

**La mod non ha parole proprie.** Tutto quello che dice è testo del gioco, nella lingua del
gioco, o un nome. Dove dovrebbe dire qualcosa di suo — un tasto di lettura premuto senza
nulla da leggere, un segno messo nel registro — non dice niente, e il silenzio è la
risposta. Gli interruttori rispondono con le parole del gioco per attivato e disattivato.

## Cosa scrive la mod

`KofXIVReader.learned`, accanto al registro, conserva le poche cose che il gioco mostra una
sola volta: quali lottatori hanno una riga del costume nel pannello di personalizzazione. Il
gioco disegna quella riga la prima volta che deve apparire e non la menziona più, quindi
vederla è l'unico modo per saperlo. Annotarlo fa sì che la mod sia in ritardo una volta e
non ad ogni avvio. Elimina il file per farle imparare tutto di nuovo.

## Segnalare un problema

Premi **F6** nel gioco per attivare il registro, **F9** nel momento in cui qualcosa viene
letto male, poi esci normalmente. Il registro è `KofXIVReader.log`, nella cartella del
gioco, e la sessione precedente resta accanto come `KofXIVReader.prev.log`. Annota cosa ha
mostrato il gioco, in quale campo, da quale schermata veniva e cosa ne ha detto la mod —
abbastanza per capire cosa avrebbe dovuto dire. Non serve scrivere quello che hai sentito:
il registro ha già le parole esatte.

## Codice sorgente

Il codice sorgente non è ancora pubblico. Lo sarà quando la mod si sarà assestata nell'uso;
è una fase, non una decisione definitiva. Quello che viene pubblicato qui è libero da
scaricare e usare.

La mod porta con sé due file che non sono suoi, `prism.dll` e `tolk.dll`, entrambi di
[PRISM](https://github.com/ethindp/prism) con licenza Mozilla Public License 2.0: vedi
[THIRD-PARTY.md](THIRD-PARTY.md).

## Traduzioni

Questo README esiste in tutte le lingue supportate dal gioco. Solo l'inglese e lo spagnolo
sono stati controllati da chi li parla; gli altri no, e le correzioni sono benvenute: una
frase goffa si corregge, una lingua assente non lascia ai suoi giocatori niente da
correggere.
