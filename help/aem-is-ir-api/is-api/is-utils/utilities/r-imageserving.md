---
description: Image Serving control script. Skriptet används för att starta, stoppa eller starta om Image Serving Server Supervisor, som i sin tur startar, stoppar eller startar om alla andra Image Serving-komponenter.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# ImageServing{#imageserving}

Image Serving control script. Skriptet används för att starta, stoppa eller starta om Image Serving Server Supervisor, som i sin tur startar, stoppar eller startar om alla andra Image Serving-komponenter.

## Användning {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`kommando`*`

## Kommandon {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Kommando </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> start  </span> </p> </td> 
   <td colname="col2"> <p> Starta Server Supervisor och alla andra Image Serving-komponenter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Stoppa alla Image Serving-komponenter, inklusive Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> starta  </span> </p> </td> 
   <td colname="col2"> <p>Starta om alla Image Serving-komponenter, inklusive Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> starta om { ps | är | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Startar om Tomcat/Platform Server, Image Server eller SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | är | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Returnerar drifttid och aktuell minnesanvändningsinformation för Image Server, Tomcat/Platform Server och SVGserver, eller status för endast den angivna servern. Ett informationsmeddelande returneras i stället om Serverhanteraren inte körs. </p> </td> 
  </tr> 
 </tbody> 
</table>

