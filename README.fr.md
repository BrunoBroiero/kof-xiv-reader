# KOF XIV Reader

[English](README.md) · [Español](README.es.md) · [Deutsch](README.de.md) · **Français** ·
[Italiano](README.it.md) · [Português](README.pt.md) · [日本語](README.ja.md) ·
[한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

> Cette traduction n'a pas été relue par une personne francophone. Les corrections sont
> bienvenues.

Un mod de lecteur d'écran pour **THE KING OF FIGHTERS XIV** (Steam, PC). Il lit les menus,
l'histoire, les listes et le texte à l'écran avec le lecteur d'écran que vous utilisez déjà
— NVDA, JAWS et les autres — pour que le jeu soit jouable sans voir.

Il parle **dans la langue du jeu**, quelle que soit celle des onze, parce que presque tout
ce qu'il dit est le texte du jeu lui-même et non celui du mod.

## Ce qu'il lit

- **Menus et options** : l'écran où vous êtes entré, l'entrée qui a le focus et sa
  description ; le nom d'un réglage, sa valeur actuelle et ce qu'a fait le changement.
- **Commandes** : l'écran des commandes, depuis les options et depuis le menu pause —
  l'appareil de chaque joueur, ce à quoi chaque action est assignée, et l'assignation
  elle-même : la touche ou le bouton pris et celui qu'il a délogé. Les touches du clavier
  sont lues telles que le jeu les écrit ; les boutons d'une manette sont nommés d'après
  les assignations que le jeu transmet à son écran — nouveau dans cette version et encore
  en vérification.
- **Mode histoire** : chaque ligne de dialogue et chaque fin — sans voix dans ce jeu, donc
  inaccessibles sans cela.
- **Listes de commandes** : comment s'exécute un coup, en cinq notations (F10 les change) :
  les mots du jeu, arcade, arcade simplifiée, FGC, FGC simplifiée.
- **Défis et tutoriel** : le combo demandé, pas à pas, et le texte de chaque leçon avec les
  entrées intégrées à la phrase.
- **Sélection des personnages** : les combattants, le panneau de personnalisation (couleur
  et tenue) et l'écran d'ordre, avec l'adversaire et les étapes de boss à trois contre un.
- **Données du joueur** : registres, classements, votre profil et votre fiche, registres et
  données de personnage.
- **Galerie** : illustrations, objets, films et sons, et ce qui est encore verrouillé.
- **Le combat lui-même, à la demande** : la vie, les barres de puissance et le chrono de
  l'attaque chrono, lus sur l'ATH du jeu (voir les touches ci-dessous).
- **En ligne** : le menu, le match classé avec sa question initiale et ses réglages de
  recherche, la liste des combats, les replays avec les équipes qui les ont joués, et le
  profil en ligne.
- **Avis, confirmations et messages système**, où qu'ils apparaissent.

Les indications de touches, le remplissage de mise en page et les compteurs de page ne sont
**volontairement pas** lus.

## Ce qui n'est pas encore couvert

- **Les salons en ligne** : match libre et entraînement en ligne — la liste des joueurs, la
  file d'attente et les écrans d'attente.
- **Les écrans autour d'un match en ligne** : l'adversaire trouvé et les résultats en ligne
  avec les points de rang. Les deux demandent une autre personne, donc aucun n'est testé.
- **Regarder un replay** : les commandes de lecture.

## Prérequis

- La version Steam PC de KOF XIV.
- Un lecteur d'écran en cours d'exécution (NVDA, JAWS, ...). Le mod parle via
  [PRISM](https://github.com/ethindp/prism), qui utilise celui qui est actif.
- Windows x64.

## Installation

Copiez trois fichiers dans le dossier du jeu, à côté de `kofxiv.exe` :

```
winmm.dll     le mod
prism.dll     PRISM
tolk.dll      la passerelle NVDA/JAWS de PRISM
```

Rien d'autre ne change, et aucun fichier du jeu n'est modifié ni renommé. Pour désinstaller,
supprimez ces trois fichiers.

Le mod se charge parce que le jeu utilise `winmm.dll` ; la copie placée dans le dossier du
jeu transmet toutes les fonctions de cette bibliothèque à la vraie, celle de `System32`, si
bien que rien d'autre dans le processus ne s'en aperçoit.

## Touches

| Touche | Ce qu'elle fait |
|--------|-----------------|
| Haut / Bas | Parcourent ce que l'écran garde — une liste de commandes, un tableau de scores, le générique. Avec une boîte de dialogue ouverte, elles déplacent son curseur |
| F1 | Dit tout ce que l'écran garde. Avec une boîte de dialogue : son message, ce qu'elle montre (les joueurs d'un replay, sa date et son mode) et l'option sélectionnée |
| F2 | Un pas en arrière. Avec une boîte de dialogue : son message et l'option sélectionnée |
| F3 | Un pas en avant. Avec une boîte de dialogue : ce qu'elle montre au sujet de sa question |
| Stick droit, en combat | Par côté, comme les barres à l'écran : à gauche la vie du joueur 1, à droite celle du joueur 2 ; en haut les barres de puissance du joueur 1, en bas celles du joueur 2 |
| Clic du stick droit, en combat | Les deux joueurs d'un coup : « PLAYER 1, 62%, POWER 2, PLAYER 2, 40%, POWER 1 ». En attaque chrono, le temps écoulé |
| Stick droit, ailleurs | F1 à F3 pour la manette : haut vaut F2, bas vaut F3, gauche et droite valent F1, le clic change la notation comme F10. Dans un défi ou une leçon cela reste ainsi, clic compris : là, les directions appartiennent au combattant, et les entrées comptent plus que les barres |
| F10 | Change la façon de dire une entrée, parmi les cinq notations |
| F11, ou les deux clics de stick sur la manette | Éteint tout le lecteur, et le rallume. Éteint, il ne dit plus rien ; ces deux-là répondent toujours, et chaque session démarre avec le lecteur allumé |
| F7 | Arrête de parler |
| F8 | Dit quel lecteur d'écran le mod a trouvé — entendre quelque chose signifie déjà que le mod fonctionne |
| F9 | Marque ce moment dans le journal, en silence : « le problème est ici » |
| F5 | Diagnostic : vider les prochaines traductions et demander au film ce que le mod ne peut pas lire |
| F6 | Active ou désactive le journal de diagnostic (activé par défaut) |

En **survie**, F1 à F3 et les directions du stick disent la vie restante en pourcentage ;
en **attaque chrono**, le temps écoulé, au format des résultats.

Ce qu'un écran garde s'arrête à ses extrémités au lieu de recommencer : passer après le
dernier morceau ne dit rien, et revenir avant le premier non plus. Ce silence marque le
début et la fin — les étapes d'un combo, les phrases d'une leçon, les lignes d'un tableau.
Ce qui est gardé en un seul morceau n'a pas d'extrémités et se dit en entier chaque fois
qu'on le demande.

**Le mod n'a pas de mots à lui.** Tout ce qu'il dit est le texte du jeu, dans la langue du
jeu, ou un nom. Là où il devrait dire quelque chose de lui — une touche de lecture sans rien
à lire, une marque posée dans le journal —, il ne dit rien, et le silence est la réponse.
Les bascules répondent avec les mots du jeu pour activé et désactivé.

## Ce que le mod écrit

`KofXIVReader.learned`, à côté du journal, garde les rares choses que le jeu ne montre
qu'une fois : quels combattants ont une ligne de tenue dans le panneau de personnalisation.
Le jeu dessine cette ligne la première fois qu'elle doit apparaître et n'en reparle jamais,
donc la voir est le seul moyen de le savoir. L'écrire fait que le mod est en retard une fois
et non à chaque démarrage. Supprimez le fichier pour qu'il réapprenne tout.

`KofXIVReader.settings`, à côté, garde ce que vous avez choisi plutôt que ce que le jeu a
montré : pour l'instant, la notation dans laquelle les commandes sont lues. Le lecteur
éteint n'est délibérément pas gardé : un mod qui s'en souviendrait démarrerait un jeu muet
sans rien pour dire pourquoi.

## Signaler un problème

Appuyez sur **F6** dans le jeu pour activer le journal, sur **F9** au moment où quelque
chose est mal lu, puis quittez normalement. Le journal est `KofXIVReader.log`, dans le
dossier du jeu, et la session précédente reste à côté sous `KofXIVReader.prev.log`. Il note
ce que le jeu a affiché, dans quel champ, de quel écran cela venait et ce que le mod en a
dit — de quoi voir ce qu'il aurait dû dire. Pas besoin d'écrire ce que vous avez entendu :
le journal en a les mots exacts.

## Code source

Le code source n'est pas encore public. Il le sera une fois le mod installé dans l'usage ;
c'est une étape, pas une décision définitive. Ce qui est publié ici est libre à télécharger
et à utiliser.

Le mod embarque deux fichiers qui ne sont pas les siens, `prism.dll` et `tolk.dll`, tous
deux de [PRISM](https://github.com/ethindp/prism) sous licence Mozilla Public License 2.0 —
voir [THIRD-PARTY.md](THIRD-PARTY.md).

## Code source

Le code source n'est pas encore public. Il le sera une fois le mod installé dans l'usage ;
c'est une étape, pas une décision définitive. Ce qui est publié ici est libre à télécharger
et à utiliser.

Le mod embarque deux fichiers qui ne sont pas les siens, `prism.dll` et `tolk.dll`, tous
deux de [PRISM](https://github.com/ethindp/prism) sous licence Mozilla Public License 2.0 —
voir [THIRD-PARTY.md](THIRD-PARTY.md).

## Traductions

Ce README existe dans toutes les langues prises en charge par le jeu. Seules les versions
anglaise et espagnole ont été relues par des locuteurs ; les autres non, et les corrections
sont bienvenues : une phrase maladroite se corrige, une langue absente ne laisse à ses
joueurs rien à corriger.
