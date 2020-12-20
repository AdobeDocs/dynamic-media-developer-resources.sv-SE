---
description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar. Makron definieras i separata makrodefinitionsfiler som kan bifogas till bildkataloger eller standardkatalogen.
seo-description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar. Makron definieras i separata makrodefinitionsfiler som kan bifogas till bildkataloger eller standardkatalogen.
seo-title: Kommandomakron
solution: Experience Manager
title: Kommandomakron
topic: Scene7 Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---


# Kommandomakron{#command-macros}

Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar. Makron definieras i separata makrodefinitionsfiler som kan bifogas till bildkataloger eller standardkatalogen.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Makronamn. </p></td> 
 </tr> 
</table>

` *`Namnet `*` är inte skiftlägeskänsligt och kan bestå av en kombination av ASCII-bokstäver, siffror, &#39;-&#39;, &#39;_&#39; och &#39;.&#39; tecken.

Makron kan anropas var som helst i en begäran efter &#39;?&#39; samt var som helst i ett `catalog::Modifier`- eller `catalog::PostModifier`-fält. Makron kan bara representera ett eller flera fullständiga bildserverkommandon och måste separeras från andra kommandon med &quot;&amp;&quot;-avgränsare.

Makroanrop ersätts av motsvarande ersättningssträngar tidigt under tolkningen. Kommandon i makron åsidosätter samma kommandon i begäran om de inträffar före makroanropet i begäran. Detta skiljer sig från `catalog::Modifier`, där kommandon i begärandesträngen alltid åsidosätter kommandon i `catalog::Modifier`-strängen, oavsett position i begäran.

Kommandomakron kan inte ha argumentvärden, men egna variabler kan användas för att skicka värden från begäran till makrot.

Makron kan kapslas med följande begränsningar: Ett makro kan bara anropas om det redan är definierat när makrodefinitionen tolkas, antingen genom att det visas tidigare i samma makrodefinitionsfil eller genom att definitionen för ett sådant inbäddat makro placeras i standardmakrodefinitionsfilen.

## Exempel {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Makron kan vara användbara om samma attribut ska användas på olika bilder.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Vi kan definiera ett makro för de gemensamma attributen:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Makrot används enligt följande:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Eftersom `wid=` inte är samma för den tredje begäran åsidosätter vi bara värdet *efter* att makrot anropas (om du anger `wid=`*innan* `$view$` skulle inte ha någon effekt).

## Se även {#section-8cdba0ed2480444ca61e719e54f8871c}

[katalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [katalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md),  [Makrodefinitionsreferens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
