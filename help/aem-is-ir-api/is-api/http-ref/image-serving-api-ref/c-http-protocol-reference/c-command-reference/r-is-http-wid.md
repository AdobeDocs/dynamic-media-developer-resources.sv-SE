---
description: Visa bredd. Anger svarsbildens bredd (visningsbild) när fit= inte finns i begäran.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# wid{#wid}

Visa bredd. Anger svarsbildens bredd (visningsbild) när fit= inte finns i begäran.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Bildbredd i pixlar (int större än 0). </p> </td> 
 </tr> 
</table>

Om både `hei=` och `scl=` anges kan den sammansatta bilden beskäras enligt attributet `align=`. När `fit=` finns med anger `wid=` den exakta, minsta eller maximala svarsbildens bredd; Mer information finns i beskrivningen av `fit=`.

Om `scl=` inte anges skalas den sammansatta bilden så att den passar. Om både `wid=` och `hei=` har angetts och `scl=` inte har angetts, skalas bilden så att den får plats helt inom rektangeln bredd/hei, så att så lite bakgrundsområde som möjligt visas. I det här fallet placeras bilden inom visningsrektangeln enligt attributet `align=`.

>[!NOTE]
>
>Ett fel returneras om den beräknade eller standardinställda svarsbildstorleken är större än `attribute::MaxPix`.

## Standard {#section-976d4c8554a34c899f85d172f6ac6f58}

Om varken `wid=`, `hei=` eller `scl=` anges har svarsbilden antingen samma storlek som den sammansatta bilden eller `attribute::DefaultPix`, beroende på vilket värde som är lägst.

## Egenskaper {#section-c93b7ce1b0d2475f80b06264b45d1285}

Visa attribut. Används oavsett den aktuella lagerinställningen.

## Exempel {#section-82bc98b7c15a451bbe9b915d414c0470}

Begär att en bild ska få plats i en 200x200-rektangel. justera bilden uppåt åt höger om den inte är fyrkantig. Alla bakgrundsområden fylls med `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Samma bild, med en fast bredd på 200 pixlar, men med en variabel höjd för att bibehålla bildens proportioner. I det här fallet har den returnerade bilden aldrig några bakgrundsfyllningsområden. Observera att align= i det här fallet inte har någon effekt alls.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Se även {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [attribut::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [attribut::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
