---
description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.
seo-description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.
seo-title: Kommandomakron *
solution: Experience Manager
title: Kommandomakron *
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---


# Kommandomakron *{#command-macros}

Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Makronamn

Makron definieras i separata makrodefinitionsfiler som kan bifogas till materialkataloger eller standardkatalogen.

*[!DNL name]* är inte skiftlägeskänsligt och kan bestå av en kombination av ASCII-bokstäver, siffror, &#39;-&#39;, &#39;_&#39; och &#39;.&#39; tecken.

Anropa makron var som helst i en begäran efter &#39;?&#39;, eller var som helst i ett `vignette::Modifier`-fält. Makron kan bara representera ett eller flera fullständiga kommandon för bildåtergivning och måste separeras från andra kommandon med &quot;&amp;&quot;-avgränsare.

Makroanrop ersätts av motsvarande ersättningssträngar tidigt under tolkningen. Kommandon i makron åsidosätter samma kommandon i begäran om de inträffar före makroanropet i begäran. Detta skiljer sig från `vignette::Modifier`, där kommandon i begärandesträngen alltid åsidosätter kommandon i `vignette::Modifier`-strängen, oavsett positionen i begäran.

Kommandomakron kan inte ha argumentvärden, men egna variabler kan användas för att skicka värden från begäran till makrot.

Makron får inte kapslas.

**Exempel**

Makron kan vara användbara om samma kommandon eller attribut ska användas på olika återgivna bilder.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Du kan definiera ett makro för de gemensamma attributen:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

Makrot används enligt följande:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Eftersom `qlt=` inte är samma för den tredje begäran åsidosätter vi bara värdet efter att makrot har anropats (att ange `qlt=`*innan* `$render$`skulle inte ha någon effekt).

**Se även**

`catalog::MacroFile`,  `catalog::Modifier`, makrodefinitionsreferens

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

