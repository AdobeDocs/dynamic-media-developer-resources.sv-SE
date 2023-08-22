---
title: op_blur
description: Oskärpebild. Använder ett oskärpefilter på bilddata.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
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

kommandot Lager. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`.

## Standard {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, utan oskärpeeffekt.

## Exempel {#section-1ebacde68388492eb108ae0fcd7424db}

Gör bakgrunden i en bild oskarp. En separat maskbild refereras till av `catalog::MaskPath`. Observera att `layer=0`måste anges explicit, annars `op_blur` används på hela den sammansatta bilden.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
