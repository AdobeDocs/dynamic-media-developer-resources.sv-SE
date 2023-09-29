---
title: hei
description: Visa höjd. Anger svarsbildens höjd (visningsbild) när det inte finns någon passning i begäran.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# hei{#hei}

Visa höjd. Anger svarsbildens höjd (visningsbild) när det inte finns någon passning i begäran.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Bildhöjd i pixlar (int större än 0). </p> </td> 
 </tr> 
</table>

Om båda `wid=` och `scl=` anges kan den sammansatta bilden beskäras enligt `align=`-attribut. När `fit=` är närvarande, `hei=` anger den exakta, minsta eller maximala svarshöjden i bilden. Se beskrivningen av [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) för mer information.

If `scl=` om inget anges skalas den sammansatta bilden så att den passar. Om båda `wid=` och `hei=` anges, och `scl=` anges inte, så skalas bilden så att den passar helt inom den breda/hei-rektangeln, så att så lite bakgrundsområde som möjligt visas. I det här fallet placeras bilden inom visningsrektangeln enligt `align=` -attribut. Bakgrundsområdet fylls med `bgc=`eller, om det inte anges med `attribute::BkgColor`.

>[!NOTE]
>
>Ett fel returneras om den beräknade svarsbilden är större än `attribute::MaxPix`.

## Egenskaper {#section-534923644a1e464496eeba83dedcbd3c}

Visa attribut. Det används oavsett den aktuella lagerinställningen.

## Standard {#section-76544d34806d4124a8b173e229cba71f}

Om ingen `wid=`, `hei=`, eller `scl=` anges har svarsbilden antingen samma storlek som den sammansatta bilden, eller `attribute::DefaultPix`, beroende på vad som är mindre.

## Exempel {#section-eb10df7cd67e4733984810aaffd0b9e2}

Begär en bild så att den får plats i en 200x200-rektangel. I det övre vänstra hörnet justeras bilden om den inte är fyrkantig. Alla bakgrundsområden fylls med `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Samma bild, med en fast höjd på 200 pixlar, men med en variabel bredd som matchar bildens proportioner. I det här fallet har den returnerade bilden aldrig några bakgrundsfyllningsområden. Och i det här fallet `align=` skulle inte ha någon effekt alls.

`http://server/myRootId/myImageId?hei=200`

## Se även {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
