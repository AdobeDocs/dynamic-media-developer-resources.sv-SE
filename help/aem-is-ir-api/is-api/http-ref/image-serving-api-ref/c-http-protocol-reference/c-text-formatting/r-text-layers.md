---
description: textPs= stöder ett antal olika användningsmodeller som beskrivs i det här avsnittet.
seo-description: textPs= stöder ett antal olika användningsmodeller som beskrivs i det här avsnittet.
seo-title: Textlager
solution: Experience Manager
title: Textlager
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---


# Textlager{#text-layers}

textPs= stöder ett antal olika användningsmodeller som beskrivs i det här avsnittet.

>[!NOTE]
>
>Det här avsnittet gäller inte för `text=`.

Gemensamma regler och definitioner är följande:

* Självstorlekande textlager är lager som inte innehåller kommandot `size=` eller för vilka `size=0,0` har angetts.

* Lagerstorleken för textlager som ändrar storlek efter den faktiska texten.
* Standardlagerankarpunkten för textlager med automatisk storlek är i allmänhet *inte* i mitten av lagret (se nedan).
* Om `anchor=` eller `origin=` har angetts för textlager med automatisk storlek påverkas textlagrets position av textinnehållet.

* När `size=` har angetts kan delar av tecken återges utanför lagrets rektangel.
* `pos=` kan användas i alla fall för att flytta ett textlager.

## Punkttext (självstorleksändring) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punkttext i Photoshop-format simuleras när `textPs=` anges utan `size=`, `textPath=` eller `textFlowPath=`. Lagerstorleken bestäms vågrätt av den återgivna textens bredd och lodrätt av radavståndet. Texten radbryts aldrig automatiskt.

Om varken `anchor=` eller `origin=` anges placeras den första textraden omedelbart ovanför lagerorigo. stycken som är markerade med `\ql` placeras till höger om lagrets ursprung, stycken som innehåller `\qr` återges till vänster om origo och stycken med `\qc` centreras vågrätt runt origo. Standardplaceringsregler för lager gäller om `anchor=` eller `origin=` har angetts.

Om `color=` anges fylls begränsningsramen för den faktiska texten.

Följande RTF-kommandon ignoreras: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rektangulär textruta {#section-1d3ab11df26d4004a1a801546756475d}

Om `size=` anges förutom `textPs=` (utan `textPath=` och `textFlowPath=`) begränsas texten till den angivna rektangeln. Lagret placeras som vanligt. Teckentecken nära textrutans kanter kan återges delvis utanför textrutan.

`color=` fyller i det område som definieras av  `size=`.

Alla RTF-kommandon används som förväntat.

## Textruta för variabel höjd {#section-e1233d1c9f8e43218667361dc0c4fd06}

Om du anger `size=` med 0 höjd kan textrutans storlek ändras lodrätt så att allt innehåll får plats. Lagerbredden definieras av bredden `size=` och lagerhöjden av höjden på den faktiska återgivna texten. Lagret placeras som vanligt. Teckentecken nära textrutans vänstra och högra kant kan återges delvis utanför textrutan.

`color=` fyller rektangeln som definieras av bredden som anges med  `size=` och höjden på den faktiska texten som återges.

Följande RTF-kommandon ignoreras:

`\vertal*`

## Självstorleksanpassad text i sökvägen {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` tillsammans med  `textPs=` kan användas för att definiera ett eller flera områden i vilka text ska flödas. `textFlowXPath=` kan anges som ett alternativ för att utesluta text från att flöda in i ett eller flera områden. Om `size=` inte anges är det resulterande textlagret självstorleksförändrande och lagerstorleken bestäms av begränsningsramen för texten som återges.

Om varken `origin=` eller `anchor=` har angetts används (0,0) av pixelkoordinatmodellen som standard för lagerankarpunkten för att definiera banan/banorna, vilket garanterar absolut placering oavsett återgiven text. Om `anchor=` eller `origin=` anges placeras lagret i förhållande till (och anpassar till) begränsningsramen för det faktiska innehållet.

`color=` fyller markeringsramen för den faktiska återgivna texten.

Följande RTF-kommandon ignoreras:

`\marg*`

## Förinställd text i sökvägen {#section-ed492a8a54414cd4bde360500cec6968}

Om `size=` anges tillsammans med `textFlowPath=` är lagerstorleken förbestämd. (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna finns i det övre vänstra hörnet av lagerrektangeln.

`textFlowPath=`-områdena kan finnas utanför lagrets rektangel. Text flödas och återges alltid i alla banområden, även om det resulterar i att text återges utanför lagrets rektangel. `extend=0,0,0,0`kan användas för att beskära den återgivna texten till lagrets rektangel.

För lagerpositionering baseras lagerektangeln på den angivna `size=`, oavsett hur mycket text som återges, även om en del av den finns utanför lagerektangeln. Standardlagerplacering gäller.

`color=` fyller det rektangulära området som definieras av  `size=`.

Följande RTF-kommandon ignoreras för `textFlowPath=`:

`\marg*`

## Självstorleksanpassad text på sökvägen {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definierar en eller flera banor på vilka text som anges med  `textPs=` ska återges. När `size=` inte anges är textlagret självstorleksförändrande. Lagerstorleken bestäms av begränsningsramen för den faktiska texten som återges.

Om varken `origin=` eller `anchor=` har angetts blir lagerankarpunkten (0,0) av pixelkoordinatmodellen som används för att definiera banan. placeringen av den återgivna texten är fast oavsett hur mycket text som återges. Om `anchor=` eller `origin=` anges placeras lagret i förhållande till (och anpassar till) begränsningsramen för det faktiska innehållet.

`color=` fyller markeringsramen för den faktiska återgivna texten.

Följande RTF-kommandon ignoreras:

* `\marg*`
* `\hyph*`
* `\vertal*`

All text efter den första `\par` eller `\line` ignoreras.

## Förinställd text på bana {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Om `size=` anges tillsammans med `textPath=` är lagerstorleken förbestämd. (0,0) av pixelkoordinatmodellen som används för att definiera banan/banorna finns i det övre vänstra hörnet av lagerrektangeln.

Banorna kan vara delvis eller helt placerade utanför lagrets rektangel. Texten används och återges alltid längs hela banan, även utanför lagrets rektangel. `extend=0,0,0,0` kan användas för att beskära den återgivna texten till lagrets rektangel.

För lagerpositionering baseras lagerektangeln på det angivna `size=`, även om en del av texten återges utanför lagrets rektangel. Standardlagerplacering gäller.

`color=` fyller det område som definieras av  `size=`.

Följande RTF-kommandon ignoreras:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

All text efter den första `\par` eller `\line` ignoreras.
