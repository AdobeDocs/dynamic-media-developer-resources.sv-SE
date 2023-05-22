---
description: textPs= stöder ett antal olika användningsmodeller som beskrivs i det här avsnittet.
solution: Experience Manager
title: Textlager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%

---

# Textlager{#text-layers}

textPs= stöder ett antal olika användningsmodeller som beskrivs i det här avsnittet.

>[!NOTE]
>
>Detta avsnitt gäller inte för `text=`.

Gemensamma regler och definitioner är följande:

* Självstorlekande textlager är lager som inte innehåller en `size=` kommando eller för vilka `size=0,0` har angetts.

* Lagerstorleken för textlager som ändrar storlek efter den faktiska texten.
* Standardlagerankarpunkten för textlager med automatisk storlek är vanligtvis *not* i mitten av lagret (se nedan).
* If `anchor=` eller `origin=` är specificerat för textlager som ändrar storlek automatiskt, och textlagrets position påverkas av textinnehållet.

* När `size=` anges kan delar av tecken återges utanför lagrets rektangel.
* `pos=` kan användas i alla fall för att flytta ett textlager.

## Punkttext (självstorleksändring) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punkttext i Photoshop-format simuleras när `textPs=` anges utan `size=`, `textPath=`, eller `textFlowPath=`. Lagerstorleken bestäms vågrätt av den återgivna textens bredd och lodrätt av radavståndet. Texten radbryts aldrig automatiskt.

Om ingen `anchor=` eller `origin=` anges, den första textraden placeras omedelbart ovanför lagerorigo, stycken markerade med `\ql` placeras till höger om lagerorigo, stycken som innehåller `\qr` återges till vänster om origo och stycken med `\qc` centreras vågrätt runt origo. Standardplaceringsregler för lager gäller om `anchor=` eller `origin=` anges.

If `color=` anges fylls begränsningsramen för den faktiska texten.

Följande RTF-kommandon ignoreras: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rektangulär textruta {#section-1d3ab11df26d4004a1a801546756475d}

If `size=` anges utöver `textPs=` (utan `textPath=` och `textFlowPath=`) begränsas texten till den angivna rektangeln. Lagret placeras som vanligt. Teckentecken nära textrutans kanter kan återges delvis utanför textrutan.

`color=` fyller det område som definieras av `size=`.

Alla RTF-kommandon används som förväntat.

## Textruta med variabel höjd {#section-e1233d1c9f8e43218667361dc0c4fd06}

Ange `size=` med 0 höjd kan textrutan storleksändras lodrätt för att passa allt innehåll. Lagerbredden definieras av bredden på `size=`och lagerhöjden med höjden på den faktiska återgivna texten. Lagret placeras som vanligt. Teckentecken nära textrutans vänstra och högra kant kan återges delvis utanför textrutan.

`color=` fyller rektangeln som definieras av bredden som anges med `size=` och höjden på den faktiska texten.

Följande RTF-kommandon ignoreras:

`\vertal*`

## Självstorleksändring av text i bana {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` i kombination med `textPs=` kan användas för att definiera ett eller flera områden i vilka text ska flödas. `textFlowXPath=` kan anges som ett alternativ för att utesluta text från att flöda in i ett eller flera områden. If `size=` om det inte anges är det resulterande textlagret självanpassat och lagerstorleken bestäms av begränsningsramen för den återgivna texten.

Om ingen `origin=` eller `anchor=` är angivna blir lagerankarpunkten (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna, vilket ger absolut positionering oavsett återgiven text. If `anchor=` eller `origin=` anges placeras lagret i förhållande till (och anpassar till) begränsningsramen för det faktiska innehållet.

`color=` fyller markeringsramen för den faktiska återgivna texten.

Följande RTF-kommandon ignoreras:

`\marg*`

## Förinställd text i bana {#section-ed492a8a54414cd4bde360500cec6968}

If `size=` anges tillsammans med `textFlowPath=`, är lagerstorleken förbestämd. (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna finns i det övre vänstra hörnet av lagerrektangeln.

The `textFlowPath=` -områden kan finnas utanför lagrets rektangel. Text flödas och återges alltid i alla banområden, även om det resulterar i att text återges utanför lagrets rektangel. `extend=0,0,0,0`kan användas för att beskära den återgivna texten till lagrets rektangel.

Lagerrektangeln baseras på den angivna `size=`oavsett hur mycket text som återges, även om en del av den finns utanför lagrets rektangel. Standardlagerplacering gäller.

`color=` fyller det rektangulära området som definieras av `size=`.

Följande RTF-kommandon ignoreras för `textFlowPath=`:

`\marg*`

## Textstorlek på bana {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definierar en eller flera banor på vilka text anges med `textPs=` bör återges. När `size=` om inget anges, blir det resulterande textlagret självanpassat. Lagerstorleken bestäms av begränsningsramen för den faktiska texten som återges.

Om ingen `origin=` eller `anchor=` är specificerade blir lagerankarpunkten (0,0) av pixelkoordinatmodellen som används för att definiera banan, placeringen av den återgivna texten är fast oavsett hur mycket text som återges. If `anchor=` eller `origin=` anges placeras lagret i förhållande till (och anpassar till) begränsningsramen för det faktiska innehållet.

`color=` fyller markeringsramen för den faktiska återgivna texten.

Följande RTF-kommandon ignoreras:

* `\marg*`
* `\hyph*`
* `\vertal*`

All text efter den första `\par` eller `\line` ignoreras.

## Förinställd text på bana {#section-a3bbbc5187f448b192e53d27e2c53f2f}

If `size=` anges tillsammans med `textPath=`, är lagerstorleken förbestämd. (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna finns i det övre vänstra hörnet av lagerrektangeln.

Banorna kan vara delvis eller helt placerade utanför lagrets rektangel. Texten används och återges alltid längs hela banan, även utanför lagrets rektangel. `extend=0,0,0,0` kan användas för att beskära den återgivna texten till lagrets rektangel.

Lagerrektangeln baseras på den angivna `size=`även om en del av texten återges utanför lagrets rektangel. Standardlagerplacering gäller.

`color=` fyller det område som definieras av `size=`.

Följande RTF-kommandon ignoreras:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

All text efter den första `\par` eller `\line` ignoreras.
