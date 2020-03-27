---
description: Anpassa svarsbilden till läget. Anger hur skalningsfaktorn beräknas, som används för att skala den sammansatta bilden till svarsbilden när svarsstorleken anges med wid= och hei= och scl=.
seo-description: Anpassa svarsbilden till läget. Anger hur skalningsfaktorn beräknas, som används för att skala den sammansatta bilden till svarsbilden när svarsstorleken anges med wid= och hei= och scl=.
seo-title: anpassa
solution: Experience Manager
title: anpassa
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# anpassa{#fit}

Anpassa svarsbilden till läget. Anger hur skalningsfaktorn beräknas, som används för att skala den sammansatta bilden till svarsbilden när svarsstorleken anges med wid= och hei= och scl=.

` fit= *`aningen`*, *`skala`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> läge </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> anpassa|begränsa|beskära|svep|sträcka|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> uppskalning </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

I följande beskrivning av lägesalternativen antas *`xScale`* förhållandet mellan den sammansatta bildens bredd och svarsbildens bredd och *`yScale`* förhållandet mellan den sammansatta bildens höjd och svarsbildens höjd.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> anpassa </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden så att den passar in i det utrymme som tilldelats med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span>, med minimalt mellanrum och utan beskärning. Svarsbilden får exakt den storlek som anges med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span>. Det mindre av <span class="varname"> xScale </span> och <span class="varname"> yScale </span> används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> begränsa </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden så som den <span class="codeph"> passar </span> så att den passar in i det utrymme som tilldelats med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span>, men den faktiska svarsbilden kan vara mindre än den som anges med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span> för att undvika tomt utrymme. Det mindre av <span class="varname"> xScale </span> och <span class="varname"> yScale </span> används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> beskära </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden så att den fyller hela svarsbilden, med minimal beskärning och utan mellanrum. Den större av <span class="varname"> xScale </span> och <span class="varname"> yScale </span> används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> bryt </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden som <span class="codeph"> beskärning </span> så att den täcker hela svarsbilden, men den faktiska svarsbilden kan vara större än vad som angetts med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span> för att undvika beskärning. Den större av <span class="varname"> xScale </span> och <span class="varname"> yScale </span>används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> sträckning </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden separat i x och y så att hela svarsbilden fylls, utan beskärning och utan mellanrum. Detta ändrar vanligtvis bildens proportioner. <span class="varname"> xScale </span> används för vågrät skalförändring och <span class="varname"> yScale </span> för lodrät skalförändring. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Använder <span class="varname"> xScale </span> för att göra bilden vågrät, med trolig beskärning eller tomt utrymme längst upp och/eller längst ned. Användbart för specialprogram. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vinst </span> </p> </td> 
   <td colname="col2"> <p>Använder <span class="varname"> yScale </span> för att anpassa bilden lodrätt, med trolig beskärning eller tomt utrymme till vänster och/eller höger. Användbart för specialprogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ange *`upscale`* till &#39;1&#39; om du vill tillåta uppskalning eller till &#39;0&#39; om du vill begränsa *`xScale`*och *`yScale`* vara begränsad till 1:1. Om uppskalning är inaktiverat kan det finnas ytterligare tomt utrymme om den sammansatta bilden är mindre än svarsbilden.

Beskärning och tomt utrymme centreras som standard. deras position kan styras med `align=`. Färgen och opaciteten för blankstegsfyllningen bestäms av `bgc=`.

## Egenskaper {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Visa attribut. Används oavsett den aktuella lagerinställningen. Minst en av `wid=` eller `hei=` måste också anges, annars returneras ett fel. både `wid=` och `hei=` måste anges för att passningslägena ska fungera enligt beskrivningen. Ett fel returneras när `req=tmb` det också anges.

## Standard {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Se även {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
