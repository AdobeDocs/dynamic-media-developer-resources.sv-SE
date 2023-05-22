---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`varaktighet`*[, *`antal`*][, *`tona`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> varaktighet</span> </span> </p> </td> 
   <td colname="col2"> <p>Anger antalet sekunder som spetstexten visas innan den döljs. När inställt på <span class="codeph"> -1</span>visas alltid meddelandet, även om användaren aktiverar den utfällbara texten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> antal</span> </span> </p> </td> 
   <td colname="col2"> <p>Anger hur många gånger texten visas när nya bilder i uppsättningen visas. Värdet för <span class="codeph"> -1</span> betyder att texten alltid visas när du visar en bild i uppsättningen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tona</span> </span> </p> </td> 
   <td colname="col2"> <p>Anger varaktigheten för en tonad animering som inträffar när texten visas eller försvinner. Värdet för <span class="codeph"> 0</span> betyder ingen tonad övergång. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Valfritt.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Exempel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
