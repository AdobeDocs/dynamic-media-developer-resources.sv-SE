---
description: Alternativ som används vid automatisk beskärning av bilder baserat på genomskinlighet.
solution: Experience Manager
title: AutoTransparentBeskärningsalternativ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 351f63a4-cc1b-4db9-93df-c21acd02e12a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 0%

---

# [!DNL AutoTransparentCropOptions]{#autotransparentcropoptions}

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
   <td colname="col1"> <span class="codeph"> tolerans </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Tar bort tomt utrymme från bildkanter baserat på genomskinlighet. Använder: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 om du vill matcha färgerna exakt. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 för att möjliggöra de största färgskillnaderna. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
