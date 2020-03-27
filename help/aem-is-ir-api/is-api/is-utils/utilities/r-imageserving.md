---
description: Skript för bildserverkontroll. Skriptet används för att starta, stoppa eller starta om Image Serving Server Supervisor, som i sin tur startar, stoppar eller startar om alla andra Image Serving-komponenter.
seo-description: Skript för bildserverkontroll. Skriptet används för att starta, stoppa eller starta om Image Serving Server Supervisor, som i sin tur startar, stoppar eller startar om alla andra Image Serving-komponenter.
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Scene7 Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageServing{#imageserving}

Skript för bildserverkontroll. Skriptet används för att starta, stoppa eller starta om Image Serving Server Supervisor, som i sin tur startar, stoppar eller startar om alla andra Image Serving-komponenter.

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
   <td colname="col1"> <p> <span class="codeph"> start </span> </p> </td> 
   <td colname="col2"> <p> Starta Server Supervisor och alla andra Image Serving-komponenter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop </span> </p> </td> 
   <td colname="col2"> <p> Stoppa alla Image Serving-komponenter, inklusive Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> starta </span> </p> </td> 
   <td colname="col2"> <p>Starta om alla Image Serving-komponenter, inklusive Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> starta om { ps| är| svg } </span> </p> </td> 
   <td colname="col2"> <p> Startar om Tomcat/Platform Server, Image Server eller SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps| är| svg ] </span> </p> </td> 
   <td colname="col2"> <p>Returnerar drifttid och aktuell minnesanvändningsinformation för Image Server, Tomcat/Platform Server och SVGserver, eller status för endast den angivna servern. Ett informationsmeddelande returneras i stället om Serverhanteraren inte körs. </p> </td> 
  </tr> 
 </tbody> 
</table>

