---
title: anpassa
description: Anpassa svarsbilden till läget. Anger hur skalningsfaktorn beräknas, som används för att skala den sammansatta bilden till svarsbilden när svarsstorleken anges med wid= och hei= och scl=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# anpassa{#fit}

Anpassa svarsbilden till läget. Anger hur skalningsfaktorn beräknas, som används för att skala den sammansatta bilden till svarsbilden när svarsstorleken anges med wid= och hei= och scl=.

` fit= *`mode`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> anpassa|begränsning|beskär|bryt|sträck|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

I följande beskrivning av lägesalternativen antas *`xScale`* vara förhållandet mellan den sammansatta bildens bredd och svarsbildens bredd och *`yScale`* är förhållandet mellan den sammansatta bildens höjd och svarsbildens höjd.

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
   <td colname="col2"> <p>Skalar den sammansatta bilden så att den passar in i utrymmet som tilldelats med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span>, med minimalt mellanrum och utan beskärning. Svarsbilden har exakt den storlek som anges med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span>. Det mindre av <span class="varname"> xScale </span> och <span class="varname"> yScale </span> används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">-begränsning </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden som <span class="codeph"> fit </span> så att den passar in i det utrymme som tilldelats med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span>, men den faktiska svarsbilden kan vara mindre än vad som angetts med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span> för att undvika tomt utrymme. Det mindre av <span class="varname"> xScale </span> och <span class="varname"> yScale </span> används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> beskär </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden så att den fyller hela svarsbilden, med minimal beskärning och utan mellanrum. Det större av <span class="varname"> xScale </span> och <span class="varname"> yScale </span> används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> radbrytning </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden som <span class="codeph"> beskär </span> så att den täcker hela svarsbilden, men den faktiska svarsbilden kan vara större än vad som angetts med <span class="codeph"> wid= </span> och <span class="codeph"> hei= </span> för att undvika beskärning. Den större av <span class="varname"> xScale </span> och <span class="varname"> yScale </span> används. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> stretch </span> </p> </td> 
   <td colname="col2"> <p>Skalar den sammansatta bilden separat i x och y så att hela svarsbilden fylls, utan beskärning och utan mellanrum. Detta ändrar vanligtvis bildens proportioner. <span class="varname"> xScale </span> används för vågrät skalning och <span class="varname"> yScale </span> för lodrät skalning. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> anpassa </span> </p> </td> 
   <td colname="col2"> <p>Använder <span class="varname"> xScale </span> för att anpassa bilden vågrätt, med trolig beskärning eller tomt utrymme högst upp och/eller längst ned. Användbart för specialprogram. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Vfit </span> </p> </td> 
   <td colname="col2"> <p>Använder <span class="varname"> yScale </span> för att anpassa bilden lodrätt, med trolig beskärning eller tomt utrymme till vänster och/eller höger. Användbart för specialprogram. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ange *`upscale`* till 1 om du vill tillåta uppskalning eller till 0 om du vill begränsa *`xScale`*och *`yScale`* till 1:1. Om uppskalning är inaktiverat kan det finnas ytterligare tomt utrymme om den sammansatta bilden är mindre än svarsbilden.

Beskärning och tomt utrymme centreras som standard. Deras position kan styras med `align=`. Färgen och opaciteten för blankstegsfyllningen bestäms av `bgc=`.

## Egenskaper {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Visa attribut. Används oavsett den aktuella lagerinställningen. Minst en av `wid=` eller `hei=` måste också anges, annars returneras ett fel. Både `wid=` och `hei=` måste anges för att passningslägena ska fungera enligt beskrivningen. Ett fel returneras när även `req=tmb` anges.

## Standard {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Se även {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
