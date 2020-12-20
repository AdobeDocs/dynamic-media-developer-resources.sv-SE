---
description: Visa höjd. Anger svarsbildens höjd (visningsbild) när det inte finns någon passning i begäran.
seo-description: Visa höjd. Anger svarsbildens höjd (visningsbild) när det inte finns någon passning i begäran.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---


# hei{#hei}

Visa höjd. Anger svarsbildens höjd (visningsbild) när det inte finns någon passning i begäran.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Bildhöjd i pixlar (int större än 0). </p> </td> 
 </tr> 
</table>

Om både `wid=` och `scl=` anges kan den sammansatta bilden beskäras enligt attributet `align=`. När `fit=` finns med anger `hei=` den exakta, minsta eller maximala höjden på svarsbilden; Mer information finns i beskrivningen av ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)`.

Om `scl=` inte anges skalas den sammansatta bilden så att den passar. Om både `wid=` och `hei=` anges och `scl=` inte anges, skalas bilden så att den får plats helt inom rektangeln bredd/hei, så att så lite bakgrundsområde som möjligt visas. I det här fallet är bilden placerad inom visningsrektangeln enligt attributet `align=`. Bakgrundsområdet fylls med `bgc=` eller, om det inte anges med `attribute::BkgColor`.

>[!NOTE]
>
>Ett fel returneras om den beräknade svarsbildens storlek är större än `attribute::MaxPix`.

## Egenskaper {#section-534923644a1e464496eeba83dedcbd3c}

Visa attribut. Används oavsett den aktuella lagerinställningen.

## Standard {#section-76544d34806d4124a8b173e229cba71f}

Om varken `wid=`, `hei=` eller `scl=` har angetts har svarsbilden antingen samma storlek som den sammansatta bilden eller `attribute::DefaultPix`, beroende på vilket värde som är lägst.

## Exempel {#section-eb10df7cd67e4733984810aaffd0b9e2}

Begär att en bild ska få plats i en 200x200-rektangel. justera bilden uppåt åt vänster om den inte är fyrkantig. Alla bakgrundsområden fylls med `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Samma bild, med en fast höjd på 200 pixlar, men med en variabel bredd som matchar bildens proportioner. I det här fallet har den returnerade bilden aldrig några bakgrundsfyllningsområden. Observera att i det här fallet skulle `align=` inte ha någon effekt alls.

`http://server/myRootId/myImageId?hei=200`

## Se även {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)  [rgn=¥,¥attribute::DefaultPix¥,¥attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
