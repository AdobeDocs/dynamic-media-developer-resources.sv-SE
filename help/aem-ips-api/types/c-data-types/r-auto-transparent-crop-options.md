---
description: Alternativ som används vid automatisk beskärning av bilder baserat på genomskinlighet.
seo-description: Alternativ som används vid automatisk beskärning av bilder baserat på genomskinlighet.
seo-title: AutoTransparentBeskärningsalternativ
solution: Experience Manager
title: AutoTransparentBeskärningsalternativ
topic: Scene7 Image Production System API
uuid: 4c3d365d-e011-4f38-bea7-68cf0cba7893
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---


# AutoTransparentCropOptions{#autotransparentcropoptions}

Alternativ som används vid automatisk beskärning av bilder baserat på genomskinlighet.

Syntax

## Parametrar {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> tolerans</span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3">Tar bort tomt utrymme från bildkanter baserat på genomskinlighet. Använder: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 om du vill matcha färgerna exakt. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 för att möjliggöra de största färgskillnaderna. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

