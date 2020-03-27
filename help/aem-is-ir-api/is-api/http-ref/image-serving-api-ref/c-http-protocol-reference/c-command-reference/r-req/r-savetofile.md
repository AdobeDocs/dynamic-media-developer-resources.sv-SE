---
description: Spara bild i fil.
seo-description: Spara bild i fil.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveToFile{#savetofile}

Spara bild i fil.

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fil</span> </p> </td> 
  <td class="stentry"> <p>Relativ sökväg till målbildfilen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Timeoutintervall (millisekunder). </p></td> 
 </tr> 
</table>

Sparar svarsbilden i en fil på servern i stället för att returnera den till klienten.

När begäran om att spara har slutförts returneras flera Java-formaterade egenskaper, bland annat följande:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Egenskap</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p>Tid när filen skapades (antal millisekunder sedan midnatt, 1 januari 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> heltal </p> </td> 
   <td> <p> Antal pixlar i sparad bild. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> gjort</span> om det lyckades. </p> </td> 
  </tr> 
 </tbody> 
</table>

Returnerar HTTP-svarsstatus 200 om den lyckas och 403 om begäran misslyckas eller timeout uppstår. Svaret har MIME-typ `text/plain` och är inte tillgängligt.

Viktigt att spara till filer måste aktiveras genom att du anger sökvägen till en befintlig skrivbar mapp i `attribute::SavePath`. `saveToFile=` misslyckas om `attribute::SavePath` är tom.

*`file`* är obligatoriskt och måste vara en relativ sökväg som kombineras med `attribute::SavePath`. Image Serving skapar inte mappar. Målmappen måste finnas på servern och ha rätt behörighetsinställningar för att Image Serving ska kunna skapa filer.

`timeout=` är valfritt. Standardtidsgränsen är 60 000 msek eller det värde som är konfigurerat med `PS::SaveTimeout`.
