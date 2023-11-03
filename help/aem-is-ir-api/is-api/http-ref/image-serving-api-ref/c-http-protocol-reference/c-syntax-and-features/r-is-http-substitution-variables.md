---
description: Ersättningsvariabler används för att överföra värden från begärande-URL:en till sammansättningsmallar som lagras i bildkataloger. Variabler kan också användas för att förmedla samma värde till olika platser i en komplex begäran.
solution: Experience Manager
title: Ersättningsvariabler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Ersättningsvariabler{#substitution-variables}

Ersättningsvariabler används för att överföra värden från begärande-URL:en till sammansättningsmallar som lagras i bildkataloger. Variabler kan också användas för att förmedla samma värde till olika platser i en komplex begäran.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variabelnamn. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Värdet som variabeln ska anges till (sträng). </p> </td> 
 </tr> 
</table>

Variabeldefinitioner och referenser kan förekomma i frågedelen av begäran i `catalog::Modifier`och in `catalog::PostModifier`.

Variabler definieras enligt ovan, ungefär som andra IS-kommandon. Med radavståndet &#39;$&#39; identifieras kommandot som en variabeldefinition. Variabler måste definieras innan de refereras.

Variabelnamnet *`var`* är inte skiftlägeskänsligt och kan bestå av en kombination av ASCII-bokstäver, siffror, &#39;-&#39;, &#39;_&#39; och &#39;.&#39;.

>[!NOTE]
>
>*`value`* måste vara URL-kodad med ett-pass för säker HTTP-överföring. Dubbel kodning krävs om *`value`* överförs på nytt via HTTP. Detta är fallet när *`value`* ersätts i en kapslad utländsk begäran eller i href-attributet för en SVG `<image>` -element.

Variabelreferenser består av variabelnamnet som avgränsas av radavståndet och efterföljande &#39;$&#39; ($)*var*$). Referenser kan förekomma var som helst i värdedelen av ett IS-kommando (det vill säga mellan &#39;=&#39; efter kommandonamnet och efterföljande &#39;&amp;&#39; eller slutet av begäran). Det går inte att använda anpassade variabler på `layer=` och `effect=` kommandon. Flera variabler tillåts i samma kommandovärde. Servern ersätter varje förekomst av ` $ *`var`*$` med *`value`*.

Variabelreferenser får inte kapslas. Eventuella förekomster av ` $ *`var`*$` inom *`value`* ersätts inte.

Exempelvis begärandefragmentet:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

matchar:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; är inte ett reserverat tecken. Det kan annars inträffa i begäran. Till exempel: `src=my$image$file.tif` är ett giltigt kommando (förutsatt att en katalogpost eller bildfil med namnet `my$image$file.tif` finns), while `wid=$number$` inte, eftersom `wid` kräver ett numeriskt argument.

## Variabel bearbetning i kapslade begäranden {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` referenser kan förekomma var som helst inom klammerparenteserna för en kapslad bildserver eller begäran om bildåtergivning, inklusive till vänster om ? avgränsar sökvägen från frågan. Servern ersätter dessa referenser med värden (antingen från url eller från `catalog::Modifier` av huvudbildkatalogen) innan den kapslade begäran analyseras och bearbetas ytterligare.

Dessutom innehåller alla ` $ *`var`*=` definitioner från webbadressen eller `catalog::Modifier` vidarebefordras till alla kapslade begäranden om bildservrar och bildåtergivning. Detta garanterar att alla variabeldefinitioner är tillgängliga för alla mallar, oavsett kapslingsnivå.

Oavsett kapslingsnivån måste bara HTTP-kodning i ett enda steg användas för variabelvärden som ska ersättas var som helst i en kapslad begäran om bildåtergivning eller bildservning eller deras associerade `catalog::Modifier` strängar.

## Variabel bearbetning i inbäddade externa begäranden {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` referenser som förekommer var som helst inom klammerparenteserna för en inbäddad extern begäran ersätts med matchande variabeldefinitionsvärden. Detta gör att inbäddade externa begäranden kan placeras i en mall i en bildkatalog.

Variabelvärden som ska ersättas i externa begäranden måste vanligtvis dubbelkodas, eftersom ingen omkodning används innan servern försöker överföra den slutliga externa URL:en.

## Variabel bearbetning i SVG-filer {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` referenser kan förekomma i SVG-filer i attributvärden och i `<text>` strängar. Bild Serving ersätter dessa med matchningen ` $ *`var`*=` definitioner som är kända vid den begärda kapslingsnivå där SVG-filen anges.

>[!NOTE]
>
>Alla variabelvärden som ska ersättas med ett `href` Attributvärdet måste vara dubbel URL-kodat. Alla andra måste vara enskilt kodade.

## Fördefinierad sökvägsvariabel {#section-930d0dd12e8f49499becc9fe8df24092}

The *`object`* som anges i begärandesökvägen tilldelas den fördefinierade variabeln `*`$object`*`. &#39; ` $ *`object`*$`&#39; kan placeras var som helst i begäran, i den mall som begäran refererar till eller i en kapslad/inbäddad begäran där ett sådant objekt tillåts, inklusive värdet för `src=` och `mask=`och sökvägen till en kapslad/inbäddad begäran.

Följande begäran återanvänder till exempel den bild som anges i sökvägen som källa för ett lager i en kapslad begäran:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Detta motsvarar

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

Definitionen av `*`$object`*` kan åsidosättas genom att explicit ange ` $ *`object`*=` med det önskade värdet.

Den fördefinierade variabeln path används vanligtvis tillsammans med `template=`.

## Standard {#section-b02483d15529444586a2e9504805b155}

Ingen. Endast variabler som har definierats ersätts av servern (förutom den fördefinierade sökvägsvariabeln $object, som alltid ersätts). Eventuella förekomster av ` $ *`var`*$` förblir literal om `*`var`*`kan inte matchas med en befintlig variabeldefinition.

## Exempel {#section-fba9393df6984247b7e30b3f93992e86}

Se&quot;Exempel A&quot; i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Se även {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
