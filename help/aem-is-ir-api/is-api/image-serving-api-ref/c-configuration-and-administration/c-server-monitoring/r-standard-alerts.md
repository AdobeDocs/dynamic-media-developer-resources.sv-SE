---
description: Standardvarningar skickas med ett konsoliderat e-postmeddelande i slutet av det konfigurerade medelintervallet.
solution: Experience Manager
title: Standardvarningar
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Standardvarningar{#standard-alerts}

Standardvarningar skickas med ett konsoliderat e-postmeddelande i slutet av det konfigurerade medelintervallet.

I följande tabell beskrivs varje typ av standardvarning.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Aviseringstyp</b> </th> 
   <th class="entry"> <b>Titel-ID</b> </th> 
   <th class="entry"> <b>Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Låst begäran </p> </td> 
   <td> <p>Lås </p> </td> 
   <td> <p>Skickas när en begäran inte kan returnera ett svar till klienten inom det angivna tröskelvärdet. Kan vara ett tecken på avbrutna begäranden som kan leda till att Java-trådpoolen tar slut. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Hög samtidighet </p> </td> 
   <td> <p>Konc </p> </td> 
   <td> Skickas när antalet begäranden som behandlas samtidigt ( <i>överlappa</i>) överskrider det angivna tröskelvärdet. Kan vara en indikation på ett serveröverlagringsvillkor. </td> 
  </tr> 
  <tr> 
   <td> <p>Minsta trafik </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Genereras när den totala begärandehastigheten underskrider det angivna tröskelvärdet. Anger oftast ett serverkommunikationsproblem (t.ex. när en server tas offline). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Felfrekvens </p> </td> 
   <td> <p>Fel </p> </td> 
   <td> <p>Skickas när den genomsnittliga hastigheten för HTTP-felsvar under samplingsintervallet överskrider det angivna tröskelvärdet. Kan vara tecken på konfigurationsproblem, saknade bilder, webbplatsprogrammering eller databasfel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Svarstid </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Skickas när den genomsnittliga bearbetningstiden för begäranden under samplingsintervallet ökar över det angivna tröskelvärdet. Anger vanligtvis ett tillfälligt eller permanent överlagringstillstånd för servern eller serverdelens bildlagringssystem. </p> <p>Felsvar beaktas inte vid beräkning av den genomsnittliga svarstiden. </p> </td> 
  </tr> 
 </tbody> 
</table>
