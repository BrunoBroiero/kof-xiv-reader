# KOF XIV Reader

[English](README.md) · **Español** · [Deutsch](README.de.md) · [Français](README.fr.md) ·
[Italiano](README.it.md) · [Português](README.pt.md) · [日本語](README.ja.md) ·
[한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

Un mod de lector de pantalla para **THE KING OF FIGHTERS XIV** (Steam, PC). Lee los menús,
la historia, las listas y el texto en pantalla con el lector de pantalla que ya usás —NVDA,
JAWS y los demás—, así que el juego se puede jugar sin ver.

Habla **en el idioma en que está el juego**, cualquiera de los once, porque casi todo lo
que dice es el texto del propio juego y no palabras del mod.

## Qué lee

- **Menús y opciones**: la pantalla en la que entraste, la entrada donde estás y su
  descripción; el nombre de una opción, en cuánto está y qué quedó al cambiarla.
- **Controles**: la pantalla de controles, desde las opciones y desde el menú de pausa:
  qué dispositivo usa cada jugador, a qué está asignada cada acción, y la asignación
  misma: la tecla o el botón que tomó y el que haya desplazado. Las teclas se leen tal
  como el juego las escribe; los botones de un mando se nombran a partir de las
  asignaciones que el juego le pasa a su pantalla, algo nuevo en esta versión y todavía
  en comprobación.
- **Modo historia**: cada línea de diálogo y cada final. En este juego no tienen voz, así
  que sin esto no hay manera de saber qué pasa.
- **Listas de comandos**: cómo se hace cada movimiento, en cinco notaciones (F10 las
  cambia): las palabras del juego, arcade, arcade simplificado, FGC y FGC simplificado.
- **Desafíos y tutorial**: el combo que te piden, paso por paso, y el texto de cada
  lección con los botones metidos en la frase.
- **Selección de personajes**: los personajes, el panel de personalización (color y traje)
  y la pantalla de orden, con quién vas a pelear y las etapas de tres contra uno.
- **Datos de jugador**: registros, rankings, tu perfil y tu ficha, registros y datos de
  personaje.
- **Galería**: ilustraciones, ítems, películas y sonidos, y lo que todavía no obtuviste.
- **La pelea misma, cuando se lo pedís**: vida, barras de poder y el reloj del ataque de
  tiempo, leídos del propio HUD del juego (mirá las teclas más abajo).
- **En línea**: el menú, el enfrentamiento clasificado con su aviso inicial y su
  configuración de búsqueda, la lista de peleas, las repeticiones con los equipos que
  jugaron, y el perfil en línea.
- **Avisos, confirmaciones y mensajes del sistema**, donde aparezcan.

Las ayudas de botones, el relleno de las pantallas y los contadores de página **no** se
leen, a propósito.

## Lo que todavía no cubre

- **Las salas en línea**: enfrentamiento libre y entrenamiento en línea, con su lista de
  jugadores, los turnos y las pantallas de espera.
- **Las pantallas alrededor de una pelea en línea**: el rival encontrado y los resultados
  con puntos de rango. Para llegar a las dos hace falta otra persona, así que ninguna está
  probada.
- **Ver una repetición**: los controles de la reproducción.

## Requisitos

- La versión de Steam para PC de KOF XIV.
- Un lector de pantalla andando (NVDA, JAWS, etc.). El mod habla a través de
  [PRISM](https://github.com/ethindp/prism), que usa el que esté activo.
- Windows x64.

## Instalación

Copiá tres archivos en la carpeta del juego, al lado de `kofxiv.exe`:

```
winmm.dll     el mod
prism.dll     PRISM
tolk.dll      el puente de PRISM con NVDA y JAWS
```

No cambia nada más, y ningún archivo del juego se modifica ni se renombra. Para
desinstalar, borrá esos tres archivos.

El mod se carga porque el juego usa `winmm.dll`; la copia que queda en la carpeta del juego
reenvía todas las funciones de esa biblioteca a la de verdad, la de `System32`, así que
nada más en el proceso se da cuenta de que está.

## Teclas

| Tecla | Qué hace |
|-------|----------|
| Arriba / Abajo | Recorren lo que la pantalla tiene guardado: una lista de comandos, una tabla de puntajes, los créditos. Con un aviso abierto, mueven su cursor |
| F1 | Dice todo lo que la pantalla tiene guardado. Con un aviso abierto: el mensaje, lo que muestra (los jugadores de una repetición, su fecha y su modo) y la opción donde estás |
| F2 | Un paso atrás en lo guardado. Con un aviso abierto: el mensaje y la opción donde estás |
| F3 | Un paso adelante. Con un aviso abierto: lo que muestra sobre aquello que te pregunta |
| Stick derecho, en una pelea | Por lados, como están las barras en pantalla: izquierda la vida del jugador 1, derecha la del jugador 2; arriba las barras de poder del 1, abajo las del 2 |
| Click del stick derecho, en una pelea | Todo junto: "PLAYER 1, 62%, POWER 2, PLAYER 2, 40%, POWER 1". En ataque de tiempo, el tiempo que llevás |
| Stick derecho, fuera de una pelea | F1 a F3 para el mando: arriba es F2, abajo es F3, izquierda y derecha son F1, y el click cambia la notación igual que F10. En un desafío o una lección sigue siendo así, el click incluido: ahí las flechas son del personaje, y los comandos importan más que las barras |
| F10 | Cambia cómo se dice un comando, entre las cinco notaciones |
| F11, o los dos clics de stick en el mando | Apaga el lector entero, y lo vuelve a encender. Apagado no dice nada; estas dos siguen respondiendo, y cada partida empieza con el lector encendido |
| F7 | Deja de hablar |
| F8 | Dice qué lector de pantalla encontró el mod. Escuchar algo ya significa que el mod está vivo |
| F9 | Marca este momento en el log, en silencio: "el problema es acá" |
| F5 | Diagnóstico: volcar las próximas traducciones y preguntarle a la película lo que el mod no puede leer |
| F6 | Activa o desactiva el log de diagnóstico (viene activado) |

En **supervivencia**, F1 a F3 y las direcciones del stick dicen la vida que te queda en
porcentaje; en **ataque de tiempo**, el tiempo que llevás, con el mismo formato de los
resultados.

Lo que una pantalla tiene guardado termina en sus extremos y no vuelve a empezar: pasarse
del último trozo no dice nada, y tampoco volver más atrás del primero. Ese silencio es
dónde empieza y dónde termina: los pasos de un combo, las frases de una lección, las filas
de una tabla. Lo que está guardado como una sola pieza no tiene extremos y se dice entero
cada vez que lo pedís.

**El mod no tiene palabras propias.** Todo lo que dice es texto del juego, en el idioma en
que está el juego, o un nombre. Donde tendría que decir algo suyo —una tecla de lectura
apretada sin nada que leer, una marca puesta en el log— no dice nada, y el silencio es la
respuesta. Lo que se activa o se desactiva responde con las palabras del propio juego.

## Qué escribe el mod

`KofXIVReader.learned`, al lado del log, guarda las pocas cosas que el juego muestra una
sola vez: qué personajes tienen fila de traje en el panel de personalización. El juego
dibuja esa fila la primera vez que tiene que aparecer y no la vuelve a mencionar, así que
verla es la única forma de saberlo. Anotarlo hace que el mod quede atrasado una vez y no
cada vez que arranca. Si borrás el archivo, lo vuelve a aprender todo.

`KofXIVReader.settings`, al lado, guarda lo que elegiste vos y no lo que mostró el juego:
por ahora, la notación en la que se leen los comandos. Que el lector esté apagado no se
guarda a propósito: un mod que lo recordara arrancaría un juego mudo sin nada que explique
por qué.

## Informar un problema

Apretá **F6** en el juego para activar el log, **F9** en el momento en que algo se lee mal,
y después salí normalmente. El log es `KofXIVReader.log`, en la carpeta del juego, y la
sesión anterior queda al lado como `KofXIVReader.prev.log`. Anota qué mostró el juego, en
qué campo, de qué pantalla vino y qué dijo el mod al respecto: alcanza para ver qué
debería haber dicho. No hace falta que escribas lo que escuchaste, porque el log ya tiene
las palabras exactas.

## Código fuente

El código todavía no es público. Va a serlo cuando el mod esté asentado en el uso; es una
etapa, no una decisión definitiva. Lo que se publica acá es libre de bajar y usar.

El mod lleva dos archivos que no son suyos, `prism.dll` y `tolk.dll`, de
[PRISM](https://github.com/ethindp/prism), con licencia Mozilla Public License 2.0: ver
[THIRD-PARTY.md](THIRD-PARTY.md).

## Código fuente

El código todavía no es público. Va a serlo cuando el mod esté asentado en el uso; es una
etapa, no una decisión definitiva. Lo que se publica acá es libre de bajar y usar.

El mod lleva dos archivos que no son suyos, `prism.dll` y `tolk.dll`, de
[PRISM](https://github.com/ethindp/prism), con licencia Mozilla Public License 2.0: ver
[THIRD-PARTY.md](THIRD-PARTY.md).

## Traducciones

Este README viene en todos los idiomas que soporta el juego. Solo el inglés y el español
los revisó alguien que los habla; el resto se tradujeron sin revisión, y las correcciones
son bienvenidas: una frase torpe se arregla, y un idioma ausente deja a sus jugadores sin
nada que corregir.
