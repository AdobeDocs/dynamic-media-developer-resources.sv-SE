---
description: Använd följande kommandon när du kodar tecken.
solution: Experience Manager
title: Teckenkodning
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
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
   <td> <p><span class="varname"> HH</span> måste vara ett tvåsiffrigt hexadecimalt värde. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Ett Unicode-tecken. </p> </td> 
   <td> <p><span class="varname"> N</span> är ett heltal med 2 byte och ett Unicode-värde större än 32767 måste därför uttryckas som ett negativt tal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode-teckenstorlek. </p> </td> 
   <td> <p>Antal byte som motsvarar det angivna Unicode-tecknet. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Tecken från områden med låg ANSI följer efter. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Tecken från ANSI-områden följer. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Dubbelbytetecken följer. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
