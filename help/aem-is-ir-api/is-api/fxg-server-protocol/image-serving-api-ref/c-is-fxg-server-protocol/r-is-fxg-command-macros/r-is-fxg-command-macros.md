---
description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.
seo-description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.
seo-title: Kommandomakron
solution: Experience Manager
title: Kommandomakron
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Kommandomakron{#command-macros}

Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.

Makron definieras i separata makrodefinitionsfiler som kan bifogas till bildkataloger eller standardkatalogen.

Makron kan anropas var som helst i en begäran efter &#39;?&#39; samt var som helst i ett `catalog::Modifier`-fält. Makron kan bara representera ett eller flera fullständiga bildserverkommandon, och måste därför omslutas av &#39;&amp;&#39;-avgränsare (utom i början eller slutet av modifieringssträngen).

Makroanrop ersätts av motsvarande ersättningssträngar tidigt under tolkningen. Kommandon i makron åsidosätter samma kommandon i begäran om de inträffar före makroanropet i begäran. Detta skiljer sig från `catalog::Modifier`, där kommandon i begärandesträngen alltid åsidosätter kommandon i `catalog::Modifier`-strängen, oavsett position i begäran.

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

Eftersom `wid=` inte är samma för den tredje begäran åsidosätter vi bara värdet *efter* att makrot anropas (om du anger `wid=`*innan* `$view$` skulle inte ha någon effekt).

+ [name](r-name.md)
