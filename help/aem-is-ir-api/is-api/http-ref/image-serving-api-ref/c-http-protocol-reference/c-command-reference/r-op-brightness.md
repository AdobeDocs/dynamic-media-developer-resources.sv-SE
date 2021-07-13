---
description: Justera intensiteten. Minskar eller ökar bildens intensitet.
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# op_brightness{#op-brightness}

Justera intensiteten. Minskar eller ökar bildens intensitet.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Intensitetsjustering (-100..+100 int). </p></td> 
 </tr> 
</table>

## Egenskaper {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Lager, kommando. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Ignoreras av effektlager. CMYK-bilder eller -lager konverteras till RGB innan åtgärden tillämpas.

## Standard {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, utan ändring av ljusstyrkan.

## Exempel {#section-c25f952f1b77409abb9ccf885862d75c}

Gör bakgrunden i en bild något mörkare för att framhäva förgrundsinnehållet:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
