---
title: Kommandomakron
description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Kommandomakron{#command-macros}

Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Makronamn

Makron definieras i separata makrodefinitionsfiler som kan bifogas till materialkataloger eller standardkatalogen.

*[!DNL name]* är inte skiftlägeskänsligt och kan bestå av en kombination av ASCII-bokstäver, siffror, &#39;-&#39;, &#39;_&#39; och &#39;.&#39; tecken.

Anropa makron var som helst i en begäran efter ?, eller var som helst i en `vignette::Modifier` fält. Makron kan bara representera ett eller flera kommandon för bildåtergivning och måste separeras från andra kommandon med &quot;&amp;&quot;-avgränsare.

Makroanrop ersätts av motsvarande ersättningssträngar tidigt under tolkningen. Kommandon i makron åsidosätter samma kommandon i begäran om de inträffar före makroanropet i begäran. Det här arbetsflödet skiljer sig från `vignette::Modifier`, där kommandon i strängen request åsidosätter kommandon i `vignette::Modifier` -sträng, oavsett positionen i begäran.

Kommandomakron kan inte ha argumentvärden, men egna variabler kan användas för att skicka värden från begäran till makrot.

Makron får inte kapslas.

**Exempel**

Makron kan vara användbara om samma kommandon eller attribut ska användas på olika återgivna bilder.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Du kan definiera ett makro för de gemensamma attributen:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

Makrot används enligt följande:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

För `qlt=` skiljer sig åt för den tredje begäran, så åsidosätter programmet värdet efter att makrot har anropats (ange `qlt=` *före* `$render$`är ineffektivt).

**Se även**

`catalog::MacroFile`, `catalog::Modifier`, makrodefinitionsreferens

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
