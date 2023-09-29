---
title: wid
description: Visa bredd. Anger svarsbildens bredd (visningsbild) när fit= inte finns i begäran.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# wid{#wid}

Visa bredd. Anger svarsbildens bredd (visningsbild) när fit= inte finns i begäran.

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Bildbredd i pixlar (int större än 0). </p> </td> 
 </tr> 
</table>

Om båda `hei=` och `scl=` anges kan den sammansatta bilden beskäras enligt `align=` -attribut. När `fit=` är närvarande, `wid=` anger den exakta, minimala eller maximala bildbredden för svar; se beskrivningen av `fit=` för mer information.

If `scl=` om inget anges skalas den sammansatta bilden så att den passar. Om båda `wid=` och `hei=` anges, och `scl=` anges inte, så skalas bilden så att den passar helt inom den breda/hei-rektangeln, så att så lite bakgrundsområde som möjligt visas. I det här fallet placeras bilden inom visningsrektangeln enligt `align=` -attribut.

>[!NOTE]
>
>Ett fel returneras om den beräknade eller standardinställda svarsbilden är större än `attribute::MaxPix`.

## Standard {#section-976d4c8554a34c899f85d172f6ac6f58}

Om ingen `wid=`, `hei=`, eller `scl=` anges har svarsbilden antingen samma storlek som den sammansatta bilden, eller `attribute::DefaultPix`, beroende på vad som är mindre.

## Egenskaper {#section-c93b7ce1b0d2475f80b06264b45d1285}

Visa attribut. Det används oavsett den aktuella lagerinställningen.

## Exempel {#section-82bc98b7c15a451bbe9b915d414c0470}

Begär en bild så att den får plats i en 200x200-rektangel. I det övre högra hörnet justeras bilden om den inte är fyrkantig. Alla bakgrundsområden fylls med `attribute::BkgColor`.

` http:// *`Server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Samma bild, med en fast bredd på 200 pixlar, men med en variabel höjd för att bibehålla bildens proportioner. I det här fallet har den returnerade bilden aldrig några bakgrundsfyllningsområden. I detta fall `align=` skulle inte ha någon effekt alls.

` http:// *`Server`*/myRootId/myImageId?wid=200`

## Se även {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
