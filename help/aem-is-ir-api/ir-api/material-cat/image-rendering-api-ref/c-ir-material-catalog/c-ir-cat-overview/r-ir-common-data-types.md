---
title: Vanliga datatyper
description: Katalogattribut och -fält kan innehålla data av någon av följande typer.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Vanliga datatyper{#common-data-types}

Katalogattribut och -fält kan innehålla data av någon av följande typer.

**Färg**

Färgvärde. Hexadecimal, packat RGB, eventuellt föregånget av 0x. Värdet RGB `128,255,0` kan anges som `0x80ff00` eller `80ff00`.

**Flagga**

`0`=false, `1`=true, alla andra värden betyder okänd eller ospecificerad.

**Enum**

`0` anger ett okänt eller ospecificerat värde, samma som ett tomt fält. Giltig `enum` värden är heltal i följd, med början med 1.

**Heltal**

Värde för signerat heltal (till exempel `0, -12, 34`). `0` eller negativa värden kan ha en speciell betydelse.

**Realnummer**

Signerat flyttalsvärde (till exempel `0, 12.5, 245 , -2.34e4`). 0 eller negativa värden kan ha en speciell betydelse.

**Textsträng**

Strängavgränsare är valfria, såvida inte strängen innehåller några `<CR>`, `<LF>`, eller `<TAB>` tecken. Enkla och dubbla citattecken kan användas som avgränsare. Om citattecken används måste alla sådana citattecken som är inbäddade i strängen föregås av två på varandra följande citattecken (t.ex. &#39; `This month''s Special`&#39;).
