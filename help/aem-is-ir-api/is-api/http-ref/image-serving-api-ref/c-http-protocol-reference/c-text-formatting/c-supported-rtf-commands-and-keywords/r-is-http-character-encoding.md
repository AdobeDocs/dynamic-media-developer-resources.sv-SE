---
title: Teckenkodning
description: Använd följande kommandon när du kodar tecken.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '87'
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
   <td> <p><span class="varname"> N</span> är ett tvåbyte stort heltal med tecken och ett Unicode-värde som är större än 32767 måste därför uttryckas som ett negativt tal. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode-teckenstorlek. </p> </td> 
   <td> <p>Antal byte som motsvarar ett givet Unicode-tecken. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Tecken från området med låg ANSI. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Tecken från det övre ANSI-området. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Dubbelbytetecken följer. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
