---
description: textPs= stöder ett antal olika användningsmodeller som beskrivs i det här avsnittet.
solution: Experience Manager
title: Textlager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Textlager{#text-layers}

textPs= stöder ett antal olika användningsmodeller som beskrivs i det här avsnittet.

>[!NOTE]
>
>Det här avsnittet gäller inte för `text=`.

Gemensamma regler och definitioner är följande:

* Självstorlekande textlager är lager som inte innehåller något `size=`-kommando eller för vilka `size=0,0` har angetts.

* Lagerstorleken för textlager som ändrar storlek efter den faktiska texten.
* Standardlagerankarpunkten för textlager som ändrar storlek automatiskt är vanligtvis *inte* i mitten av lagret (se nedan).
* Om `anchor=` eller `origin=` har angetts för textlager med automatisk storlek påverkas textlagrets position av textinnehållet.

* När `size=` har angetts kan delar av teckenglyfer återges utanför lagrets rektangel.
* `pos=` kan användas i alla fall för att flytta ett textlager.

## Punkttext (självstorleksändring) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punkttext i Photoshop-format simuleras när `textPs=` anges utan `size=`, `textPath=` eller `textFlowPath=`. Lagerstorleken bestäms vågrätt av den återgivna textens bredd och lodrätt av radavståndet. Texten radbryts aldrig automatiskt.

Om varken `anchor=` eller `origin=` anges placeras den första textraden omedelbart ovanför lagerorigo. Stycken som är markerade med `\ql` placeras till höger om nollpunkten, stycken som innehåller `\qr` återges till vänster om origo och stycken med `\qc` centreras vågrätt runt origo. Standardplaceringsregler för lager gäller om `anchor=` eller `origin=` anges.

Om `color=` anges fylls begränsningsramen för den faktiska texten.

Följande RTF-kommandon ignoreras: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rektangulär textruta {#section-1d3ab11df26d4004a1a801546756475d}

Om `size=` anges förutom `textPs=` (utan `textPath=` och `textFlowPath=`) begränsas texten till den angivna rektangeln. Lagret placeras som vanligt. Teckentecken nära textrutans kanter kan återges delvis utanför textrutan.

`color=` fyller det område som definieras av `size=`.

Alla RTF-kommandon används som förväntat.

## Textruta med variabel höjd {#section-e1233d1c9f8e43218667361dc0c4fd06}

Om du anger `size=` med 0 höjd kan textrutan storleksändras lodrätt så att allt innehåll får plats. Lagerbredden definieras av bredden på `size=` och lagerhöjden av höjden på den faktiska återgivna texten. Lagret placeras som vanligt. Teckentecken nära textrutans vänstra och högra kant kan återges delvis utanför textrutan.

`color=` fyller rektangeln som definieras av bredden som anges med `size=` och höjden på den faktiska texten som återges.

Följande RTF-kommandon ignoreras:

`\vertal*`

## Självstorleksändring av text i bana {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` tillsammans med `textPs=` kan användas för att definiera ett eller flera områden som texten ska flödas i. `textFlowXPath=` kan anges om du vill exkludera text från att flöda in i ett eller flera områden. Om `size=` inte anges är det resulterande textlagret självanpassat och lagerstorleken bestäms av begränsningsramen för den återgivna texten.

Om varken `origin=` eller `anchor=` anges används som standard (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna, vilket garanterar absolut placering oavsett återgiven text. Om `anchor=` eller `origin=` anges placeras lagret i förhållande till (och anpassar sig till) begränsningsramen för det faktiska innehållet.

`color=` fyller markeringsramen för den faktiska återgivna texten.

Följande RTF-kommandon ignoreras:

`\marg*`

## Förinställd text i bana {#section-ed492a8a54414cd4bde360500cec6968}

Om `size=` anges tillsammans med `textFlowPath=` är lagerstorleken förbestämd. (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna finns i det övre vänstra hörnet av lagerrektangeln.

`textFlowPath=`-områdena kan finnas utanför lagrets rektangel. Text flödas och återges alltid i alla banområden, även om det resulterar i att text återges utanför lagrets rektangel. `extend=0,0,0,0` kan användas för att beskära den återgivna texten till lagrets rektangel.

För lagerpositioneringssyften baseras lagerektangeln på den angivna `size=`, oavsett hur mycket text som återges, även om en del av den finns utanför lagerektangeln. Standardlagerplacering gäller.

`color=` fyller det rektangulära området som definieras av `size=`.

Följande RTF-kommandon ignoreras för `textFlowPath=`:

`\marg*`

## Textstorlek på bana {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definierar en eller flera sökvägar till vilka text som anges med `textPs=` ska återges. Om `size=` inte anges är textlagret självstorleksförändrande. Lagerstorleken bestäms av begränsningsramen för den faktiska texten som återges.

Om varken `origin=` eller `anchor=` anges används som standard (0,0) av pixelkoordinatmodellen som används för att definiera banan. Positionen för den återgivna texten är fast oavsett hur mycket text som återges. Om `anchor=` eller `origin=` anges placeras lagret i förhållande till (och anpassar sig till) begränsningsramen för det faktiska innehållet.

`color=` fyller markeringsramen för den faktiska återgivna texten.

Följande RTF-kommandon ignoreras:

* `\marg*`
* `\hyph*`
* `\vertal*`

All text efter den första `\par` eller `\line` ignoreras.

## Förinställd text på bana {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Om `size=` anges tillsammans med `textPath=` är lagerstorleken förbestämd. (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna finns i det övre vänstra hörnet av lagerrektangeln.

Banorna kan vara delvis eller helt placerade utanför lagrets rektangel. Texten används och återges alltid längs hela banan, även utanför lagrets rektangel. `extend=0,0,0,0` kan användas för att beskära den återgivna texten till lagerrektangeln.

För lagerpositioneringssyften baseras lagerektangeln på den angivna `size=`, även om en del av texten återges utanför lagrets rektangel. Standardlagerplacering gäller.

`color=` fyller det område som definieras av `size=`.

Följande RTF-kommandon ignoreras:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

All text efter den första `\par` eller `\line` ignoreras.
