---
description: Standardsvarsbild. Anger den bild- eller katalogpost som ska användas när det inte går att hitta en bild.
seo-description: Standardsvarsbild. Anger den bild- eller katalogpost som ska användas när det inte går att hitta en bild.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# defaultImage{#defaultimage}

Standardsvarsbild. Anger den bild- eller katalogpost som ska användas när det inte går att hitta en bild.

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objekt </span></span> </p> </td> 
  <td class="stentry"> <p>Bildobjekt. </p> </td> 
 </tr> 
</table>

*`object`* kan vara antingen en katalogpost (inklusive en mall) eller en enkel bildfilssökväg. Användbart om du vill ersätta saknade bilder med standardbilder. Det här värdet åsidosätter värdet för motsvarande katalog `attribute::DefaultImage`. Ett tomt värde ( `defaultImage=`) inaktiverar standardbildhantering.

>[!NOTE]
>
>Standardbildmekanismen gäller inte för SVG-objekt. Ett fel returneras om SVG-objektet som anges i begäran inte kan hittas.

Om `attribute::DefaultImageMode=0`det *`object`* ersätter hela den ursprungliga begäran, även om bara en bild i en flerbildsdisposition saknas. De enda kommandona som behålls från den ursprungliga begäran är: `wid=`, `hei=`, `fmt=`, `qlt=`..

Om `attribute::DefaultImageMode=1`objektet bara ersätter den bild som saknas i lagret. attribut för det saknade lagret används och den sammansatta bilden bearbetas och returneras som vanligt.

## Egenskaper {#section-d30923d8dc4042eba10989212dd70887}

Begär attribut. Används oavsett den aktuella lagerinställningen. Ignoreras om `req=` är en annan än `img` eller `tmb`.

## Begränsningar {#section-30df31bc8cac41cd917f1e45196779c2}

Utländska bildkällor omfattas inte av standardbildmekanismen. ett fel returneras om en extern bildkälla inte är giltig.

Bildredigering återgår till `DefaultImageMode=0` när kapslad bildåtergivning eller FXG-återgivningsbegäranden misslyckas.

## Standard {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Se även {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
