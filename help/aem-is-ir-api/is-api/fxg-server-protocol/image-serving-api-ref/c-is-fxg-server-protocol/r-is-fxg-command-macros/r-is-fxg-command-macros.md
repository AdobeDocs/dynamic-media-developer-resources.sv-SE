---
description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.
solution: Experience Manager
title: Kommandomakron
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Kommandomakron{#command-macros}

Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.

Makron definieras i separata makrodefinitionsfiler som kan bifogas till bildkataloger eller standardkatalogen.

Makron kan anropas var som helst i en begäran efter &#39;?&#39; samt var som helst i en `catalog::Modifier` fält. Makron kan bara representera ett eller flera fullständiga bildserverkommandon, och måste därför omslutas av &#39;&amp;&#39;-avgränsare (utom i början eller slutet av modifieringssträngen).

Makroanrop ersätts av motsvarande ersättningssträngar tidigt under tolkningen. Kommandon i makron åsidosätter samma kommandon i begäran om de inträffar före makroanropet i begäran. Det här skiljer sig från `catalog::Modifier`, där kommandona i begärandesträngen alltid åsidosätter kommandon i `catalog::Modifier` sträng, oavsett position i begäran.

Makron kan kapslas med följande begränsningar: Ett makro kan bara anropas om det redan är definierat när makrodefinitionen tolkas, antingen genom att det visas tidigare i samma makrodefinitionsfil eller genom att definitionen för ett sådant inbäddat makro placeras i standardmakrodefinitionsfilen.

Makron kan vara användbara om samma attribut ska användas på olika bilder.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Vi kan definiera ett makro för de gemensamma attributen:

`view wid=240&fmt=pdf&imageRes=300`

Makrot används enligt följande:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Sedan `wid=` skiljer sig åt för den tredje begäran, vi åsidosätter helt enkelt värdet *efter* makrot anropas (ange `wid=`*före* `$view$` skulle inte ha någon effekt).

+ [name](r-name.md)
