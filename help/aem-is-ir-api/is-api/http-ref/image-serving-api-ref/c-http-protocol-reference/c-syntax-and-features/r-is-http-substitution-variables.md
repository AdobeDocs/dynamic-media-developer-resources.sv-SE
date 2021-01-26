---
description: Ersättningsvariabler används för att överföra värden från begärande-URL:en till sammansättningsmallar som lagras i bildkataloger. Variabler kan också användas för att förmedla samma värde till olika platser i en komplex begäran.
seo-description: Ersättningsvariabler används för att överföra värden från begärande-URL:en till sammansättningsmallar som lagras i bildkataloger. Variabler kan också användas för att förmedla samma värde till olika platser i en komplex begäran.
seo-title: Ersättningsvariabler
solution: Experience Manager
title: Ersättningsvariabler
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# Ersättningsvariabler{#substitution-variables}

Ersättningsvariabler används för att överföra värden från begärande-URL:en till sammansättningsmallar som lagras i bildkataloger. Variabler kan också användas för att förmedla samma värde till olika platser i en komplex begäran.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Variabelnamn. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Värdet som variabeln ska anges till (sträng). </p> </td> 
 </tr> 
</table>

Variabeldefinitioner och referenser kan förekomma i frågedelen av begäran, i `catalog::Modifier` och i `catalog::PostModifier`.

Variabler definieras enligt ovan, på samma sätt som andra IS-kommandon. radavståndet &#39;$&#39; identifierar kommandot som en variabeldefinition. Variabler måste definieras innan de refereras.

Variabelnamnet *`var`* är inte skiftlägeskänsligt och kan bestå av en kombination av ASCII-bokstäver, siffror, &#39;-&#39;, &#39;_&#39; och &#39;.&#39;.

>[!NOTE]
>
>*`value`* måste vara URL-kodad med ett-pass för säker HTTP-överföring. Dubbel kodning krävs om *`value`* överförs på nytt via HTTP. Detta är fallet när *`value`* ersätts till en kapslad extern begäran eller till href-attributet för ett SVG `<image>`-element.

Variabelreferenser består av variabelnamnet som avgränsas av inledande och avslutande &#39;$&#39; ($*var*$). Referenser kan förekomma var som helst i värdedelen av ett IS-kommando (d.v.s. mellan &#39;=&#39; efter kommandonamnet och efterföljande &#39;&amp;&#39; eller slutet av begäran). Det går inte att använda anpassade variabler för kommandona `layer=` och `effect=`. Flera variabler tillåts i samma kommandovärde. Servern ersätter varje förekomst av ` $ *`var`*$` med *`value`*.

Variabelreferenser får inte kapslas. Förekomster av ` $ *`var`*$` i *`value`* ersätts inte.

Exempelvis begärandefragmentet:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

matchar:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; är inte ett reserverat tecken; det kan inträffa på annat sätt i begäran. `src=my$image$file.tif` är till exempel ett giltigt kommando (förutsatt att det finns en katalogpost eller bildfil med namnet `my$image$file.tif`), medan `wid=$number$` inte är det, eftersom `wid` kräver ett numeriskt argument.

## Variabel bearbetning i kapslade begäranden {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *``*$` varianter kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om &#39;?&#39; avgränsar sökvägen från frågan. Servern ersätter dessa referenser med värden (antingen från url eller `catalog::Modifier` i huvudbildkatalogen) innan den kapslade begäran analyseras och bearbetas ytterligare.

Dessutom vidarebefordras alla ` $ *`var`*=`-definitioner från URL:en eller `catalog::Modifier` till alla kapslade begäranden om bildservering och bildåtergivning. Detta garanterar att alla variabeldefinitioner är tillgängliga för alla mallar, oavsett kapslingsnivå.

Oavsett kapslingsnivån måste bara HTTP-kodning i en enda omgång användas för variabelvärden som ska ersättas var som helst i en kapslad begäran om bildåtergivning eller bildservning eller deras associerade `catalog::Modifier`-strängar.

## Variabel bearbetning i inbäddade externa begäranden {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *``*$` variabelreferenser som förekommer var som helst inom klammerparenteserna för en inbäddad extern begäran ersätts med matchande variabeldefinitionsvärden. Detta gör att inbäddade externa begäranden kan placeras i en mall i en bildkatalog.

Variabelvärden som ska ersättas i externa begäranden måste vanligtvis dubbelkodas, eftersom ingen omkodning används innan servern försöker överföra den slutliga externa URL:en.

## Variabel bearbetning i SVG-filer {#section-a8359f9909764142b6a18ae778dca913}

` $ *`Det kan finnas `*$` varianter i SVG-filer i attributvärden och i  `<text>` strängar. Image Serving ersätter dessa med de matchande ` $ *`var`*=`-definitionerna som är kända vid den begärandekapslingsnivå där SVG-filen anges.

>[!NOTE]
>
>Alla variabelvärden som ska ersättas med ett `href`-attributvärde måste vara dubbelURL-kodade; alla andra måste kodas separat.

## Fördefinierad sökvägsvariabel {#section-930d0dd12e8f49499becc9fe8df24092}

*`object`* som anges i sökvägen till begäran tilldelas den fördefinierade variabeln `*`$object`*`. &#39; ` $ *`object`*$`&#39; kan placeras var som helst i begäran, i mallen som begäran refererar till eller i en kapslad/inbäddad begäran där ett sådant objekt tillåts, inklusive värdet för `src=` och `mask=` samt sökvägen för en kapslad/inbäddad begäran.

Följande begäran återanvänder till exempel den bild som anges i sökvägen som källa för ett lager i en kapslad begäran:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Detta motsvarar

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

Definitionen för `*`$object`*` kan åsidosättas genom att explicit ange ` $ *`object`*=` med önskat värde.

Den fördefinierade variabeln path används vanligtvis tillsammans med `template=`.

## Standard {#section-b02483d15529444586a2e9504805b155}

Ingen. Endast variabler som har definierats ersätts av servern (förutom den fördefinierade sökvägsvariabeln $object, som alltid ersätts). Alla förekomster av ` $ *`var`*$` är literala om `*`var`*`inte kan matchas med en befintlig variabeldefinition.

## Exempel {#section-fba9393df6984247b7e30b3f93992e86}

Se&quot;Exempel A&quot; i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
