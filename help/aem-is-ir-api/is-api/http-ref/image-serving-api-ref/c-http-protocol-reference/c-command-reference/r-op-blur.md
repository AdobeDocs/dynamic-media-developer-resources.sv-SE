---
description: Oskärpebild. Använder ett oskärpefilter på bilddata.
seo-description: Oskärpebild. Använder ett oskärpefilter på bilddata.
seo-title: op_blur
solution: Experience Manager
title: op_blur
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# op_blur{#op-blur}

Oskärpebild. Använder ett oskärpefilter på bilddata.

`op_blur= *`radie`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radie</span> </p> </td> 
  <td class="stentry"> <p>Oskärpefiltrets radie i pixlar (verklig 0,100). </p></td> 
 </tr> 
</table>

*`radius`* är i pixlar i förhållande till den sammansatta bilden. Används även för luddlagereffekter.

## Egenskaper {#section-92573fe2c07746a7bab93a81fc3d208d}

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`.

## Standard {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, utan oskärpeeffekt.

## Exempel {#section-1ebacde68388492eb108ae0fcd7424db}

Gör bakgrunden i en bild oskarp. `catalog::MaskPath` refererar till en separat maskbild. Observera att `layer=0`måste anges explicit, annars används `op_blur` på hela den sammansatta bilden.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
