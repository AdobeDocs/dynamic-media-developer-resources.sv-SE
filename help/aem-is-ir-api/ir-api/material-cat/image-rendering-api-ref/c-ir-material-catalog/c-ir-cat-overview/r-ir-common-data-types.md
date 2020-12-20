---
description: Katalogattribut och -fält kan innehålla data av någon av följande typer.
seo-description: Katalogattribut och -fält kan innehålla data av någon av följande typer.
seo-title: Vanliga datatyper
solution: Experience Manager
title: Vanliga datatyper
topic: Scene7 Image Serving - Image Rendering API
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Vanliga datatyper{#common-data-types}

Katalogattribut och -fält kan innehålla data av någon av följande typer.

**Färg**

Färgvärde. Hexadecimalt, packat RGB-värde, eventuellt föregånget av 0x. RGB-värdet `128,255,0` kan till exempel anges som `0x80ff00` eller `80ff00`.

**Flagga**

`0`=false,  `1`=true, alla andra värden betyder okänd eller ospecificerad.

**Enum**

0 anger ett okänt eller ospecificerat värde, samma som ett tomt fält. Giltiga `enum`-värden är heltal i följd med början på 1.

**Heltal**

Signerat heltalsvärde (t.ex. 0, -12, 34). 0 eller negativa värden kan ha en speciell betydelse.

**Realnummer**

Signerat flyttalsvärde (t.ex. `0, 12.5, 245 , -2.34e4`). 0 eller negativa värden kan ha en speciell betydelse.

**Textsträng**

Strängavgränsare är valfria, såvida inte strängen innehåller några `<CR>`-, `<LF>`- eller `<TAB>`-tecken. Enkla och dubbla citattecken kan användas som avgränsare. Om citattecken används måste alla sådana citattecken som är inbäddade i strängen föregås av två citattecken (t.ex. &#39; `This month''s Special`&#39;).
