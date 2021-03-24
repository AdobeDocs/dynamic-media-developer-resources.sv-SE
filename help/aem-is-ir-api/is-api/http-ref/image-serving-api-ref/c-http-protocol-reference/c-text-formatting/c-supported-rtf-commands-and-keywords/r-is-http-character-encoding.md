---
description: Använd följande kommandon när du kodar tecken.
solution: Experience Manager
title: Teckenkodning
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
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

