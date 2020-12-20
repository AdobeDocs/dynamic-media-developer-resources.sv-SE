---
description: Intresseregion. Anger ett rektangulärt intresseområde (ROI) i den sammansatta bilden, uttryckt i pixlar.
seo-description: Intresseregion. Anger ett rektangulärt intresseområde (ROI) i den sammansatta bilden, uttryckt i pixlar.
seo-title: gradera
solution: Experience Manager
title: gradera
topic: Scene7 Image Serving - Image Rendering API
uuid: 08657925-c52a-4279-8357-c26ad5c5ef3d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# rgn{#rgn}

Intresseregion. Anger ett rektangulärt intresseområde (ROI) i den sammansatta bilden, uttryckt i pixlar.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixelförskjutning från det övre vänstra hörnet av den sammansatta bilden till det övre vänstra hörnet av avkastningen (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Storlek på avkastning i pixlar (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` definierar bara en avkastning utan att beskära bilden. När även `wid=` och/eller `hei=` större än storlek används, kan ytterligare data från den sammansatta bilden visas i den slutliga svarsbilden.

## Egenskaper {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Visa attribut. Används oavsett den aktuella lagerinställningen.

Alla områden i avkastningen som sträcker sig utanför den sammansatta bilden läggs till med `bgc=`.

`rgn=` används före slutlig skalning och anpassning med  `scl=`,  `wid=`,  `hei=`,  `fit=`,  `rect=`eller  `align=`.

## Standard {#section-6a3df8f670084def900ffef9dab7e94a}

Hela den sammansatta bilden ( `rgn=0,0,width,height`).

## Se även {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)  [align=¥,¥fit=¥,¥rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
