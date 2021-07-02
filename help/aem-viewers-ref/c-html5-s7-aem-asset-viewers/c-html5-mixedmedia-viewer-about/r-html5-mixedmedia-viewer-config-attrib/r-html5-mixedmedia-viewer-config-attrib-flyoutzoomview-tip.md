---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Visningsprogram,SDK/API,blandade medieuppsättningar
role: Developer,Business Practitioner
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`durationcountfade `*[, *``*][, *``*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> varaktighet</span></span> </p> </td> 
   <td colname="col2"> <p> Anger antalet sekunder som spetstexten visas innan den döljs. När det är inställt på <span class="codeph"> -1</span> visas alltid meddelandet, även om användaren aktiverar den utfällbara menyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> antal</span></span> </p> </td> 
   <td colname="col2"> <p> Anger hur många gånger texten visas när nya bilder i uppsättningen visas. Värdet <span class="codeph"> -1</span> betyder att texten alltid visas när du visar en bild i uppsättningen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tona</span></span> </p> </td> 
   <td colname="col2"> Anger varaktigheten för en tonad animering som inträffar när texten visas eller försvinner. Värdet <span class="codeph"> 0</span> anger ingen toningsövergång. </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-65be9301796240e38f31818229da7acc}

Valfritt.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Exempel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
