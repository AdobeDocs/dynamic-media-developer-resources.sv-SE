---
title: Kommandomakron
description: Kommandomakron innehåller namngivna kortkommandon för kommandouppsättningar. Makron definieras i separata makrodefinitionsfiler som kan bifogas till bildkataloger eller standardkatalogen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '310'
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

`*`name`*` är inte skiftlägeskänsligt och kan bestå av en kombination av ASCII-bokstäver, siffror, &#39;-&#39;, &#39;_&#39; och &#39;.&#39; tecken.

Makron kan anropas var som helst i en begäran efter ?, och var som helst i en `catalog::Modifier` eller `catalog::PostModifier` fält. Makron kan bara representera ett eller flera, fullständiga, bildserverkommandon och måste separeras från andra kommandon med `&` avgränsare.

Makroanrop ersätts av motsvarande ersättningssträngar tidigt under tolkningen. Kommandon i makron åsidosätter samma kommandon i begäran om de inträffar före makroanropet i begäran. Detta bearbetningsflöde skiljer sig från `catalog::Modifier`, där kommandon i strängen request alltid åsidosätter kommandon i `catalog::Modifier` sträng, oavsett position i begäran.

Kommandomakron kan inte ha argumentvärden, men egna variabler kan användas för att skicka värden från begäran till makrot.

Makron kan vara kapslade. Ett makro kan bara anropas om det redan är definierat när makrodefinitionen tolkas. Det här arbetsflödet utförs antingen genom att det visas tidigare i samma makrodefinitionsfil eller genom att definitionen för ett sådant inbäddat makro placeras i standardmakrodefinitionsfilen.

## Exempel {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Makron kan vara användbara om samma attribut ska användas på olika bilder.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Du kan definiera ett makro för de gemensamma attributen:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Makrot används enligt följande:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

För `wid=` skiljer sig åt för den tredje begäran, du kan helt enkelt åsidosätta värdet *efter* makrot anropas (ange `wid=`*före* `$view$` har ingen effekt).

## Se även {#section-8cdba0ed2480444ca61e719e54f8871c}

[katalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [katalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Makrodefinitionsreferens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
