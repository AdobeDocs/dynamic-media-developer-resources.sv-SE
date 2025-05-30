---
title: clipPath
description: Lagerklippsbana. Anger en klippbana för aktuellt lager.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# clipPath{#clippath}

Lagerklippsbana. Anger en klippbana för aktuellt lager.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition </span> </span> </p> </td> 
  <td class="stentry"> <p>Bandata. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName </span></span> </p> </td> 
  <td class="stentry"> <p>Namnet på banan som är inbäddad i lagerkällbilden (endast ASCII). </p></td> 
 </tr> 
</table>

Alla delar av lagret som ligger utanför det område som definieras av `clipPath=` återges som genomskinliga.

`*`pathName`*` är namnet på en bana som är inbäddad i lagerkällbilden. Banan omformas automatiskt för att bibehålla den relativa justeringen med bildinnehållet. Om mer än en `*`pathName`*` har angetts klipper servern ut bilden till skärningspunkten för sökvägarna. Alla `*`pathName`*` som inte hittas i källbilden ignoreras.

>[!NOTE]
>
>Endast ASCII-strängar stöds för `*`pathName`*`.

`*`pathDefinition`*` tillåter att explicit sökvägsdata anges i lagerpixelkoordinater.

Om `size=` har angetts och inte 0,0, förstorleksändras lagret. I det här fallet är bankoordinaterna relativa till lagrets övre vänstra hörn och lagret placeras baserat på `origin=` eller dess standardvärde. Alla områden i banan utanför lagrets rektangel förblir genomskinliga.

Om `size=` inte anges för en heltäckande färg eller ett textlager betraktas lagret som självanpassat i den utsträckning som banan bestämmer dess storlek. Om `origin=` inte anges används (0,0) av sökvägens koordinatmodell som standard. Med den här arbetsflödesprocessen kan du ange bankoordinater i förhållande till origo för lager 0.

>[!NOTE]
>
>Kommandona `scale=`, `rotate=` och `anchor=` tillåts inte för helstora färglager som ändrar storlek automatiskt.

`*`pathDefinition`*` accepterar en sträng som liknar värdet för attributet `d=` i elementet SVG `<path>` förutom att kommatecken används i stället för mellanslag för att skilja värden åt. `*`pathDefinition`*` kan innehålla en eller flera underbanor med sluten slinga.

Följande sökvägskommandon stöds i `*`pathDefinition`*`:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Kommando</b> </th> 
   <th class="entry"> <b> namn </b> </th> 
   <th class="entry"> <b> Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y </span> </td> 
   <td> <p> moveto absolut </p> </td> 
   <td> <p> Starta en ny delbana vid x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y </span> </td> 
   <td> <p> flytta relativt </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolut </p> </td> 
   <td> <p> Rita en linje från den aktuella positionen till x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relativ </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *<span class="varname"> x1,y1,x2,y2,x,y</span> </td> 
   <td> <p> krängande absolut </p> </td> 
   <td> <p> Rita en Bezier-kurva från den aktuella positionen till x,y. x1,y1 är kontrollpunkten i början av kurvan och x2,y2 är kontrollpunkten i slutet av kurvan. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *&lbrace;<span class="varname"> x1,y1,x2,y2,x,y</span> </td> 
   <td> <p> kurvförhållande </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Stäng den aktuella delbanan med en rak linje. </p> </td> 
  </tr> 
 </tbody> 
</table>

Kommandon med versaler anger att koordinatvärdena är i absoluta pixelpositioner (i förhållande till lagrets övre vänstra hörn). Pixelförskjutningar följer gemena kommandon i förhållande till den aktuella positionen.

m eller M startar alltid en ny delbana. Delbanor stängs automatiskt (med en rak linje) om &#39;Z&#39; eller &#39;z&#39; inte anges i slutet.

Om en underbana börjar med en relativ rörelse (&#39;m&#39;) är den relativ till något av följande:

* Startpunkten för den föregående delbanan, om den stängdes med &quot;z&quot; eller &quot;Z&quot;.
* Slutpunkten för den tidigare delbanan, om den inte stängdes explicit.
* 0,0, om det är den första delbanan.

## Egenskaper {#section-d4127db0dac54e3cbd44f7ea1e001960}

Lagerattribut. Gäller det aktuella lagret eller den sammansatta bilden om `layer=comp`. Effektlager ignorerar det.

Modifieraren `clipPathE=` ignoreras om det inte finns någon bana med det angivna namnet i lagrets källbild eller om lagerkällan inte är en bild.

## Standard {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Ingen, om du inte vill ha någon ytterligare urklippning av lagret.

## Se även {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
