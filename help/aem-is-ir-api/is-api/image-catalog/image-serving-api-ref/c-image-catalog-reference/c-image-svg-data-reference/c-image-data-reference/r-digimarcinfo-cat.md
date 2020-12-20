---
description: Information om Digimarc-bilder. Aktiverar Digimarc-inbäddning och anger typ av vattenstämpel och associerade bildspecifika data.
seo-description: Information om Digimarc-bilder. Aktiverar Digimarc-inbäddning och anger typ av vattenstämpel och associerade bildspecifika data.
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
topic: Scene7 Image Serving - Image Rendering API
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 7%

---


# DigimarcInfo{#digimarcinfo}

Information om Digimarc-bilder. Aktiverar Digimarc-inbäddning och anger typ av vattenstämpel och associerade bildspecifika data.

## Egenskaper {#section-62af219e8bac422b8541841221c9ce4f}

Fyra heltalsvärden, avgränsade med kommatecken.

` *``*, *``*, *`typeflagsval1`*, *`val2`*`

` *``*` typeaktiverar Digimarc-inbäddning och anger vattenstämpeltypen:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>Typ av vattenstämpel</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Ingen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Grundläggande. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Bild-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transaktions-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Copyright-år. </p> </td> 
  </tr> 
 </tbody> 
</table>

` *`Ett `*` bitfält med tre värden flaggas. Ange bit 0 för att ange kopieringsskyddat innehåll, bit 1 för att ange begränsat innehåll och bit 2 för att ange innehåll för vuxna:

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> flaggor</span> </span> </p> </th> 
   <th class="entry"> <p><b>Beskrivning</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Kopieringsskyddad. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Begränsat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Kopieringsskyddad, begränsad. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Motionsinnehåll. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Kopiera skyddat, vuxeninnehåll. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Begränsat innehåll för vuxna. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Kopieringsskyddat, begränsat, moget innehåll. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tolkningen av ` *`val1`*` och ` *`val2`*` beror på ` *`typ`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Används inte. </p> </td> 
   <td> <p>Används inte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Används inte. </p> </td> 
   <td> <p>Används inte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Bild-ID. </p> </td> 
   <td> <p>Används inte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transaktions-ID. </p> </td> 
   <td> <p>Används inte. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Första copyrightåret. </p> </td> 
   <td> <p>Andra copyrightåret. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Standard {#section-4bb97e5f79074be89cc691e73449eb43}

Ärvs från attribut::DigimarcInfo om fältet inte finns eller om det är tomt.

## Exempel {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot; inaktiverar Digimarc-vattenstämplar för den här bilden.

&quot;1,5,0,0&quot; anger en grundläggande vattenstämpel med flaggan för innehåll som är anpassat och kopieringsskyddat.

&quot;2,0,4567,0&quot; anger en vattenstämpel med ett bild-ID.

&quot;3,2,56483,0&quot; anger en vattenstämpel med ett transaktions-ID och flaggan för begränsat innehåll.

&quot;4,0,1998,2001&quot; anger en vattenstämpel med copyright-år.

## Se även {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ,  [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
