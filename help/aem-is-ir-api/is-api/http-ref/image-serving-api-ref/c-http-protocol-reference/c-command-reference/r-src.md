---
description: Lagerbild.
seo-description: Lagerbild.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# src{#src}

Lagerbild.

` src= *``*|{[is|ir|fxg]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>Bildobjekt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Kapslad bildhantering, bildåtergivning eller extern begäran. </p> </td> 
 </tr> 
</table>

## Beskrivning {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Anger källbilden för ett bildlager.

*`object`* kan antingen vara en katalogpost eller en bild-/SVG-fil.

Se [objekt](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Kapslade eller inbäddade begäranden omsluts av klammerparenteser. Lägg till en inbäddad begäran om bildbehandling `is`som prefix, en inbäddad begäran om bildåtergivning med `ir`och en begäran om FXG-grafikåtergivning med `fxg`. En begäran till en extern server antas om inget prefix anges.

Se [Begär kapsling och inbäddning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

>[!NOTE]
>
>FXG-grafikåtergivning är endast tillgängligt i Scene7-värdmiljön och kan kräva ytterligare licensiering. Kontakta Scene7 Support för mer information.

## Egenskaper {#section-2c22bb89a35d470f833df8ba898efd93}

Lagerattribut. Gäller för `layer=0` if `layer=comp`. Ömsesidigt uteslutande med `text=` och `textPs=` i samma lager. den sista förekomsten av antingen `text=`, `textPs=`eller `src=` gäller och avgör om det är en bild eller ett textlager. Ignoreras av effektlager.

*`object`*kan inte matchas till en annan katalogpost som innehåller ett `src=` - eller `mask=` -kommando i dess `catalog::Modifier`. (Använd kapsling av begäranden för att uppnå en liknande effekt.)

Prefixen `is`, `ir`och `fxg` är skiftlägeskänsliga.

## Standard {#section-a92f3882041b4d43ae2caf014647165f}

För lager 0 används objektet från bankomponenten i URL:en om `src=` inte anges. Inget standardvärde för andra lager.

## Se även {#section-e467e03330564796932ac081f1c9c1d0}

[katalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribut::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[object¥,¥Templates¥,¥Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
