---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Anger när informationspanelen ska visas. </p> <p>Om <span class="codeph"> 1</span> anges visas informationspanelen när musen kommer till bildschemaområdet (om bildschemat inte är tomt, <span class="codeph"> rollover_key</span>-attribut). </p> <p>Om inställt på <span class="codeph"> 0</span> infopanelen aktiveras när användaren klickar på bildschemat (om bildschemat har ett icke-tomt <span class="codeph"> rollover_key</span> och tomt <span class="codeph"> href</span>-attribut). </p> <p> Ignoreras på pekenheter, inklusive datorer med pekskärm, och ställs automatiskt in på <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-ccfedc2da28f412a86d03f390db92b4b}

Valfritt.

## Standard {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Exempel {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
