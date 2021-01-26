---
description: Använd följande kommandon när du kodar tecken.
seo-description: Använd följande kommandon när du kodar tecken.
seo-title: Teckenkodning
solution: Experience Manager
title: Teckenkodning
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Teckenkodning{#character-encoding}

Använd följande kommandon när du kodar tecken.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Kommando </th> 
   <th class="entry"> Beskrivning </th> 
   <th class="entry"> Anteckningar </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Ett 8-bitarstecken. </p> </td> 
   <td> <p><span class="varname"> HH </span> måste vara ett tvåsiffrigt hexvärde. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>Ett Unicode-tecken. </p> </td> 
   <td> <p><span class="varname"> När </span> ett tvåbyte stort heltal med tecken och ett Unicode-värde större än 32767 måste därför uttryckas som ett negativt tal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Unicode-teckenstorlek. </p> </td> 
   <td> <p>Antal byte som motsvarar det angivna Unicode-tecknet. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>Tecken från områden med låg ANSI följer efter. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>Tecken från ANSI-områden följer. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>Dubbelbytetecken följer. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

