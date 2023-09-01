---
title: Kommandomakron
description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Kommandomakron{#command-macros}

Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.

Makron definieras i separata makrodefinitionsfiler som kan bifogas till bildkataloger eller standardkatalogen.

Makron kan anropas var som helst i en begäran efter ?, och var som helst i en `catalog::Modifier` fält. Makron kan bara representera ett eller flera fullständiga bildserverkommandon och måste därför omslutas av &#39;&amp;&#39;-avgränsare (utom när i början eller slutet av modifieringssträngen).

Makroanrop ersätts av motsvarande ersättningssträngar tidigt under tolkningen. Kommandon i makron åsidosätter samma kommandon i begäran om de inträffar före makroanropet i begäran. Det här flödet skiljer sig från `catalog::Modifier`, där kommandon i strängen request alltid åsidosätter kommandon i `catalog::Modifier` -sträng, oavsett positionen i begäran.

Makron kan kapslas. Ett makro kan bara anropas om det redan är definierat när makrodefinitionen tolkas. Det här flödet utförs antingen genom att det visas tidigare i samma makrodefinitionsfil eller genom att definitionen för ett sådant inbäddat makro placeras i standardmakrodefinitionsfilen.

Makron kan vara användbara om samma attribut ska användas på olika bilder.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

Du kan definiera ett makro för de gemensamma attributen:

`view wid=240&fmt=pdf&imageRes=300`

Makrot används enligt följande:

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

För `wid=` skiljer sig åt för den tredje begäran, du åsidosätter bara värdet *efter* makrot anropas (ange `wid=` *före* `$view$` har ingen effekt).

+ [name](r-name.md)
