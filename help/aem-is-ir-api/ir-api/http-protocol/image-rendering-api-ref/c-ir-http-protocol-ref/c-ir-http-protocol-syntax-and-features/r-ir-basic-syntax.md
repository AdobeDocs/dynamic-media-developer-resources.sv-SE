---
title: Grundläggande syntax för HTTP-protokoll för bildåtergivning
description: I det här avsnittet beskrivs den grundläggande syntaxen för HTTP-protokollet Dynamic Media Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Grundläggande syntax för HTTP-protokoll för bildåtergivning{#image-rendering-http-protocol-basic-syntax}

I det här avsnittet beskrivs den grundläggande syntaxen för HTTP-protokollet Dynamic Media Image Rendering.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Objekt </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> begäran</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> modifiers</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vinjettering </span> </p> </td> 
   <td colname="col2"> <p>Vinjettspecificerare (relativ filsökväg eller vinjetteringskataloginlägg). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifierare </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname">-kommando</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> kommentar </span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">-kommando </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> makro </span> </p> </td> 
   <td colname="col2"> <p>Namnet på ett kommandomakro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> kommentar </span> </p> </td> 
   <td colname="col2"> <p>Kommentarssträng (ignoreras av servern). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>Namnet på ett kommando eller attribut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Namnet på en anpassad variabel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> värde </span> </p> </td> 
   <td colname="col2"> <p>Kommando eller variabelvärde. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* och *`var`* är skiftlägeskänsliga. Servern bevarar skiftläget för alla andra strängvärden.

**Server-ID**

Rotkontexten `/ir/render` krävs för alla HTTP-begäranden till bildåtergivning.

**Kommentarer**

Kommentarer kan bäddas in i begärande strängar var som helst och identifieras med en punkt (.) omedelbart efter kommandoavgränsaren (&amp;). Kommentaren avslutas av nästa förekomst av en (okodad) kommandoavgränsare. Den här funktionen kan användas för att lägga till information i begäran som inte är avsedd för Image Serving, t.ex. tidsstämplar och databas-ID:n.

**HTTP-avkodning**

Bildåtergivning extraherar först *`object`* och *`modifiers`* från den inkommande begäran. *`object`* separeras sedan till sökvägselement som är individuellt HTTP-avkodade. Strängen *`modifiers`* separeras till *`command`*= *`value`* par och *`value`* HTTP-avkodas sedan före kommandospecifik bearbetning.
