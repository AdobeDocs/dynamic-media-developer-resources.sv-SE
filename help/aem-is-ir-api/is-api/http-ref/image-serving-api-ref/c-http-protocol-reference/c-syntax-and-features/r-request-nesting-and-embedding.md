---
description: Image Serving har stöd för obegränsad kapsling av Image Serving-begäranden, inbäddning av begäranden om bildåtergivning samt inbäddning av bilder som hämtats från externa servrar. Det är bara lagerbilder och lagermasker som har stöd för dessa mekanismer.
seo-description: Image Serving har stöd för obegränsad kapsling av Image Serving-begäranden, inbäddning av begäranden om bildåtergivning samt inbäddning av bilder som hämtats från externa servrar. Det är bara lagerbilder och lagermasker som har stöd för dessa mekanismer.
seo-title: Begär kapsling och inbäddning
solution: Experience Manager
title: Begär kapsling och inbäddning
topic: Scene7 Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 0%

---


# Begär kapsling och inbäddning{#request-nesting-and-embedding}

Image Serving har stöd för obegränsad kapsling av Image Serving-begäranden, inbäddning av begäranden om bildåtergivning samt inbäddning av bilder som hämtats från externa servrar. Det är bara lagerbilder och lagermasker som har stöd för dessa mekanismer.

>[!NOTE]
>
>Vissa e-postklienter och proxyservrar kan koda klammerparenteserna som används för syntaxen för kapsling och inbäddning. I program där detta är ett problem bör parenteser användas i stället för klammerparenteser.

## Begäranden om kapslad bildservering {#section-6954202119e0466f8ff27c79f4f039c8}

En hel Image Serving-begäran kan användas som en lagerkälla genom att ange den i kommandot `src=` (eller `mask=`) med följande syntax:

`…&src=is( nestedRequest)&…`

Token `is` är skiftlägeskänslig.

Den kapslade begäran får inte innehålla serverrotsökvägen (vanligtvis ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>De kapslade avgränsningstecknen för begäran ( `'(',')'`) och kommandoavgränsningstecknen ( `'?'`, `'&'`, `'='`) i kapslade begäranden får inte vara HTTP-kodade. I praktiken måste kapslade begäranden kodas på samma sätt som den yttre (kapslade) begäran.

Förbearbetningsregler tillämpas på kapslade begäranden.

Följande kommandon ignoreras när de anges i kapslade begäranden (antingen i begärande-URL eller i `catalog::Modifier` eller `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Om den resulterande bilden av den kapslade begäran innehåller maskdata (alfavärden) skickas den till inbäddningslagret som lagermask.

Även `attribute::MaxPix`och `attribute::DefaultPix` för bildkatalogen som gäller för den kapslade begäran ignoreras.

Bildresultatet av en kapslad IS-begäran kan cachelagras genom att inkludera `cache=on`. Som standard är cachelagring av mellanliggande data inaktiverad. Cachelagring bör endast aktiveras när den mellanliggande bilden förväntas återanvändas i en annan begäran inom en rimlig tidsperiod. Standardhantering av cache på serversidan gäller. Data cachelagras i ett icke-förstörande format.

## Begäranden om inbäddad bildåtergivning {#section-69c5548db930412b9b90d9b2951a6969}

När Scene7 Image Rendering är aktiverat på servern kan återgivningsbegäranden användas som lagerkällor genom att ange dem med kommandot src= (eller mask=). Använd följande syntax:

` …&src=ir( *[!DNL renderRequest]*)&…`

Token `ir` är skiftlägeskänslig.

*[!DNL renderRequest]* är den vanliga begäran om bildåtergivning, exklusive HTTP-rotsökvägen  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>De kapslade avgränsningstecknen för begäran ( `'(',')'`) och kommandoavgränsningstecknen ( `'?'`, `'&'`, `'='`) i kapslade begäranden får inte vara HTTP-kodade. Inbäddade begäranden måste i själva verket kodas på samma sätt som den yttre (inbäddade) begäran.

Följande kommandon för bildåtergivning ignoreras när de anges i kapslade begäranden:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Även `attribute::MaxPix` och `attribute::DefaultPix` ignoreras för materialkatalogen som gäller för den kapslade återgivningsbegäran.

Bildresultatet av en kapslad IR-begäran kan cachelagras genom att inkludera `cache=on`. Som standard är cachelagring av mellanliggande data inaktiverad. Cachelagring bör endast aktiveras när den mellanliggande bilden förväntas återanvändas i en annan begäran inom en rimlig tidsperiod. Standardhantering av cache på serversidan gäller. Data cachelagras i ett icke-förstörande format.

## Inbäddade FXG-återgivningsbegäranden {#section-c817e4b4f7da414ea5a51252ca7e120a}

När FXG-grafikåtergivaren (även [!DNL AGMServer]) är installerad och aktiverad med Image Serving, kan FXG-begäranden användas som lagerkällor genom att ange dem med kommandona `src=` (eller `mask=`). Använd följande syntax:

`…&src=fxg( renderRequest)&…`

Token `fxg` är skiftlägeskänslig.

>[!NOTE]
>
>FXG-grafikåtergivning är endast tillgängligt i Scene7 värdmiljö och kan kräva ytterligare licensiering. Kontakta Scene7 Support för mer information.

*[!DNL renderRequest]* är den vanliga FXG-återgivningsbegäran, exklusive HTTP-rotsökvägen  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Avgränsningstecknen ( `'(',')'`) och kommandoavgränsningstecknen ( `'?'`, `'&'`, `'='`) i kapslade begäranden får inte vara HTTP-kodade. Inbäddade begäranden måste i själva verket kodas på samma sätt som den yttre (inbäddade) begäran.

Följande FXG-kommandon ignoreras när de anges i kapslade begäranden:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Externa bildkällor {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Serving stöder åtkomst till källbilder på externa HTTP-servrar.

>[!NOTE]
>
>Endast HTTP-protokollet stöds för fjärr-URL:er.

Om du vill ange en extern URL för ett `src=`- eller `mask=`-kommando avgränsar du det externa URL- eller URL-fragmentet med parenteser:

`…&src=( foreignUrl)&…`

Viktigt! Avgränsartecken ( `'(',')'`) och kommandoavgränsartecken ( `'?'`, `'&'`, `'='`) i kapslade begäranden får inte vara HTTP-kodade. Inbäddade begäranden måste i själva verket kodas på samma sätt som den yttre (inbäddade) begäran.

Fullständiga absoluta URL:er (om `attribute::AllowDirectUrls` har angetts) och URL:er i förhållande till `attribute::RootUrl` tillåts. Ett fel inträffar om en absolut URL är inbäddad och attributet: `AllowDirectUrls` är 0 eller om en relativ URL har angetts och `attribute::RootUrl` är tom.

Även om externa URL:er inte kan anges direkt i sökvägskomponenten i den begärda URL:en, går det att ställa in en förbearbetningsregel som tillåter konvertering av relativa sökvägar till absoluta URL:er (se exemplet nedan).

Externa bilder cachelagras av servern enligt de cachelagringsrubriker som ingår i HTTP-svaret. Om varken en `ETag` eller en Senast ändrad HTTP-svarshuvud finns, cachelagras inte svaret. Detta kan orsaka dålig prestanda vid upprepad åtkomst för samma externa bild, eftersom Image Serving måste hämta om och validera bilden vid varje åtkomst.

Den här funktionen stöder samma bildfilsformat som stöds av verktyget Bildkonvertering (IC), med undantag för källbilder med 16 bitar per komponent.

>[!NOTE]
>
>Image Serving kör automatiskt valideringsverktyget när en extern bild används första gången, för att säkerställa att bilden är giltig och inte har skadats under överföringen. Detta kan orsaka en viss fördröjning vid första åtkomsten. För bästa prestanda bör du begränsa storleken på sådana bilder och/eller använda ett bildfilsformat som komprimeras väl.

## Begränsningar {#section-fb68e3f0d40947feb94d7bf183b64929}

Storleken på bilden som skapas av kapslade/inbäddade begäranden optimeras normalt automatiskt. Om cachelagring av kapslade begärandebilder är aktiverat, kan inkrementella prestandavinster uppnås genom att ange den exakta storleken på den kapslade bilden, så att ingen ytterligare skalning krävs när cacheposten återanvänds.

Viktig bildhantering stöder inte dubbel kodning av kapslade eller inbäddade begäranden. Kapslade och inbäddade begäranden måste HTTP-kodas precis som enkla begäranden.

## Exempel {#section-d800cfc31abe46d2a964f8e7929231f1}

**Lagermall med cachelagring:**

Använd kapsling för att lägga till cachelagring i en lagermall. Ett begränsat antal bakgrundsbilder överlappas med mycket variabel text. Den inledande mallsträngen kan se ut så här:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Med mindre ändringar kan vi förskala bilden för lager 0 och cachelagra den permanent, vilket minskar serverbelastningen:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Bädda in begäranden om Scene7 bildåtergivning**

Använda en mall som lagras i [!DNL myCatalog/myTemplate]; generera bilden för lager2 i mallen med Scene7 Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Lägg märke till de kapslade klammerparenteserna. Begäran om bildåtergivning bäddar in ett anrop tillbaka till Image Serving för att hämta en repeterbar textur.

## Se även {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference,  [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
