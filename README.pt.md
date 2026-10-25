# KOF XIV Reader

[English](README.md) · [Español](README.es.md) · [Deutsch](README.de.md) ·
[Français](README.fr.md) · [Italiano](README.it.md) · **Português** ·
[日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) ·
[繁體中文](README.zh-TW.md)

> Esta tradução não foi revisada por uma pessoa falante de português. Correções são
> bem-vindas.

Um mod de leitor de tela para **THE KING OF FIGHTERS XIV** (Steam, PC). Ele lê os menus, a
história, as listas e o texto da tela com o leitor de tela que você já usa — NVDA, JAWS e os
demais — para que o jogo possa ser jogado sem ver.

Ele fala **no idioma em que o jogo está**, qualquer um dos onze, porque quase tudo o que diz
é o texto do próprio jogo e não palavras do mod.

## O que ele lê

- **Menus e opções**: a tela em que você entrou, o item em foco e sua descrição; o nome de
  uma configuração, em que valor está e o que a mudança fez.
- **Controles**: a tela de controles, pelas opções e pelo menu de pausa — qual
  dispositivo cada jogador usa, a que cada ação está atribuída, e a própria atribuição:
  a tecla ou o botão tomado e o que ele deslocou. As teclas do teclado são lidas como o
  jogo as escreve. Os botões de um controle ainda não são lidos — as atribuições que o
  jogo entrega à sua tela ainda estão sendo decifradas —, por isso as linhas de um
  controle dizem só a ação.
- **Modo história**: cada linha de diálogo e cada final — sem voz neste jogo e, portanto,
  inacessíveis sem isso.
- **Listas de comandos**: como se executa um golpe, em cinco notações (F10 alterna entre
  elas): as palavras do jogo, arcade, arcade simplificada, FGC, FGC simplificada.
- **Desafios e tutorial**: o combo pedido, passo a passo, e o texto de cada lição com os
  comandos dentro da frase.
- **Seleção de personagens**: os lutadores, o painel de personalização (cor e traje) e a
  tela de ordem, com quem é o adversário e os estágios de chefe de três contra um.
- **Dados do jogador**: registros, rankings, seu perfil e sua ficha, registros e dados de
  personagem.
- **Galeria**: ilustrações, itens, filmes e sons, e o que ainda está bloqueado.
- **A luta em si, quando você pede**: vida, barras de poder e o cronômetro do ataque de
  tempo, lidos do próprio HUD do jogo (veja as teclas abaixo).
- **Online**: o menu, a partida ranqueada com sua pergunta inicial e suas configurações de
  busca, a lista de batalhas, os replays com as equipes que os jogaram, e o perfil online.
- **Avisos, confirmações e mensagens do sistema**, onde aparecerem.

As dicas de botões, o preenchimento de layout e os contadores de página **não** são lidos,
de propósito.

## O que ainda não cobre

- **As salas online**: partida livre e treino online — a lista de jogadores, a fila e as
  telas de espera.
- **As telas em volta de uma partida online**: o adversário encontrado e os resultados
  online com pontos de rank. As duas exigem outra pessoa, então nenhuma foi testada.
- **Assistir a um replay**: os controles da reprodução.

## Requisitos

- A versão da Steam para PC de KOF XIV.
- Um leitor de tela em execução (NVDA, JAWS, ...). O mod fala por meio do
  [PRISM](https://github.com/ethindp/prism), que usa o que estiver ativo.
- Windows x64.

## Instalação

Copie três arquivos para a pasta do jogo, ao lado de `kofxiv.exe`:

```
winmm.dll     o mod
prism.dll     PRISM
tolk.dll      a ponte do PRISM com NVDA e JAWS
```

Nada mais muda, e nenhum arquivo do jogo é modificado ou renomeado. Para desinstalar,
apague esses três arquivos.

O mod é carregado porque o jogo usa `winmm.dll`; a cópia que fica na pasta do jogo repassa
todas as funções dessa biblioteca para a verdadeira, a de `System32`, de modo que nada mais
no processo percebe que ela está ali.

## Teclas

| Tecla | O que faz |
|-------|-----------|
| Cima / Baixo | Percorrem o que a tela guarda — uma lista de comandos, uma tabela de pontos, os créditos. Com uma caixa de diálogo aberta, movem o cursor dela |
| F1 | Diz tudo o que a tela guarda. Com uma caixa de diálogo: a mensagem, o que ela mostra (os jogadores de um replay, a data e o modo) e a opção em foco |
| F2 | Um passo para trás. Com uma caixa de diálogo: a mensagem e a opção em foco |
| F3 | Um passo para frente. Com uma caixa de diálogo: o que ela mostra sobre aquilo que pergunta |
| Analógico direito, na luta | Por lado, como as barras aparecem na tela: à esquerda a vida do jogador 1, à direita a do jogador 2; para cima as barras de poder do jogador 1, para baixo as do jogador 2 |
| Clique do analógico direito, na luta | Os dois jogadores juntos: "PLAYER 1, 62%, POWER 2, PLAYER 2, 40%, POWER 1". No ataque de tempo, o tempo decorrido |
| Analógico direito, fora da luta | F1 a F3 no controle: cima é F2, baixo é F3, esquerda e direita são F1, e o clique muda a notação como o F10. Em um desafio ou uma lição continua assim, inclusive o clique: ali as direções são do personagem, e os comandos importam mais que as barras |
| F10 | Muda como um comando é dito, entre as cinco notações |
| F11, ou os dois cliques dos sticks no controle | Desliga o leitor inteiro, e liga de novo. Desligado não diz nada; estas duas continuam respondendo, e cada partida começa com o leitor ligado |
| F7 | Para de falar |
| F8 | Diz qual leitor de tela o mod encontrou — ouvir algo já significa que o mod está funcionando |
| F9 | Marca este momento no log, em silêncio: "o problema é aqui" |
| F5 | Diagnóstico: despejar as próximas traduções e perguntar ao filme o que o mod não consegue ler |
| F6 | Liga ou desliga o log de diagnóstico (ligado por padrão) |

No **sobrevivência**, F1 a F3 e as direções do analógico dizem a vida restante em
porcentagem; no **ataque de tempo**, o tempo decorrido, no formato dos resultados.

O que uma tela guarda termina nas suas pontas em vez de voltar ao começo: passar do último
trecho não diz nada, e voltar antes do primeiro também não. Esse silêncio é onde começa e
onde termina — os passos de um combo, as frases de uma lição, as linhas de uma tabela. O que
está guardado como uma peça única não tem pontas e é dito inteiro cada vez que você pede.

**O mod não tem palavras próprias.** Tudo o que ele diz é texto do jogo, no idioma do jogo,
ou um nome. Onde ele teria de dizer algo seu — uma tecla de leitura apertada sem nada para
ler, uma marca colocada no log — ele não diz nada, e o silêncio é a resposta. O que liga e
desliga responde com as palavras do próprio jogo.

## O que o mod escreve

`KofXIVReader.learned`, ao lado do log, guarda as poucas coisas que o jogo mostra uma única
vez: quais lutadores têm linha de traje no painel de personalização. O jogo desenha essa
linha na primeira vez que ela precisa aparecer e nunca mais a menciona, então vê-la é o
único jeito de saber. Anotar isso faz o mod ficar atrasado uma vez, e não a cada início.
Apague o arquivo para que ele aprenda tudo de novo.

`KofXIVReader.settings`, ao lado, guarda o que você escolheu, e não o que o jogo mostrou:
por enquanto, a notação em que os comandos são lidos. O leitor desligado não é guardado de
propósito: um mod que lembrasse disso começaria um jogo mudo sem nada que explicasse por
quê.

## Relatar um problema

Aperte **F6** no jogo para ligar o log, **F9** no momento em que algo é lido errado, e então
saia normalmente. O log é `KofXIVReader.log`, na pasta do jogo, e a sessão anterior fica ao
lado como `KofXIVReader.prev.log`. Ele registra o que o jogo mostrou, em qual campo, de qual
tela veio e o que o mod disse a respeito — o bastante para ver o que ele deveria ter dito.
Não precisa escrever o que você ouviu: o log já tem as palavras exatas.

## Código-fonte

O código-fonte ainda não é público. Será, quando o mod estiver firmado no uso; é uma etapa,
não uma decisão definitiva. O que é publicado aqui é livre para baixar e usar.

O mod leva dois arquivos que não são dele, `prism.dll` e `tolk.dll`, ambos do
[PRISM](https://github.com/ethindp/prism) sob a licença Mozilla Public License 2.0 — veja
[THIRD-PARTY.md](THIRD-PARTY.md).

## Código-fonte

O código-fonte ainda não é público. Será, quando o mod estiver firmado no uso; é uma etapa,
não uma decisão definitiva. O que é publicado aqui é livre para baixar e usar.

O mod leva dois arquivos que não são dele, `prism.dll` e `tolk.dll`, ambos do
[PRISM](https://github.com/ethindp/prism) sob a licença Mozilla Public License 2.0 — veja
[THIRD-PARTY.md](THIRD-PARTY.md).

## Traduções

Este README existe em todos os idiomas que o jogo suporta. Apenas o inglês e o espanhol
foram revisados por quem os fala; os outros não, e correções são bem-vindas: uma frase
desajeitada se corrige, e um idioma ausente não deixa aos seus jogadores nada para corrigir.
