---
title: Storlek
description: Decal size. Bredd, höjd och tjocklek för ett dekalt materialobjekt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Storlek{#size}

Decal size. Bredd, höjd och tjocklek för ett dekalt materialobjekt.

## Egenskaper {#section-967bf1112eec4032a91ed0c8a7b10a07}

Tre reella tal avgränsade med kommatecken. Den får inte vara negativ. Ställ in oanvända värden på 0. Efterföljande nollor kan utelämnas.

Ange bara både bredd och höjd om bilden ska sträckas ut för att passa den angivna storleken (proportionerna kan ändras). Ange antingen bredd eller höjd om du vill skalförändra bilden proportionellt. Ange både bredd och höjd till 0 om du vill använda `catalog::Resolution` för att bestämma objektstorleken.

Ange ett tjockleksvärde för att lägga till en skugga till det dekala objektet. Valfritt för dekala material, ignorerat av alla andra material.

## Standard {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Detta anger att den dekala storleken ska bestämmas utifrån katalog::Upplösning och att objektet inte har någon tjocklek (därför återges ingen skugga).

## Exempel {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>Dekalen är 12x3 tum stor och har ingen tjocklek (det vill säga ingen skugga). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>Dekalen är 5 tum bred, höjden bestäms av bildens proportioner och en skugga återges baserat på en tjocklek på 1 tum. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,,5 </p></td> 
  <td class="stentry"> <p>Dekalbredden och höjden bestäms av katalogen::Upplösning och att den är ½ tum tjock. </p></td> 
 </tr> 
</table>

## Se även {#section-31a164e781d14e92bd9d379d3c329e92}

[katalog::Upplösning](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
