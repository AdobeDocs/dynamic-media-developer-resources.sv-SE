---
description: Färgvärden. Du kan ange färgvärden antingen hexadecimalt, med en kommaavgränsad lista över komponentvärden eller med decimaler.
seo-description: Färgvärden. Du kan ange färgvärden antingen hexadecimalt, med en kommaavgränsad lista över komponentvärden eller med decimaler.
seo-title: färg
solution: Experience Manager
title: färg
topic: Scene7 Image Serving - Image Rendering API
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 11%

---


# färg{#color}

Färgvärden. Du kan ange färgvärden antingen hexadecimalt, med en kommaavgränsad lista över komponentvärden eller med decimaler.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> färg</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> green</span>,<span class="varname"> blue</span>[,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>,  <span class="varname"> magenta</span>,  <span class="varname"> gult</span>,  <span class="varname"> svart</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> röd</span>,  <span class="varname"> grön</span>,  <span class="varname"> blå</span>,  <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>färgkomponentvärde (0...255, decimalint) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cyan</span>,  <span class="varname"> magenta</span>,  <span class="varname"> gult</span>,  <span class="varname"> svart</span>,  <span class="varname"> alfa</span></span> </p></td> 
  <td class="stentry"> <p>CMYK-färgkomponentvärde (0,100 %, decimalint) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> grå</span>,  <span class="varname"> alfa</span></span> </p> </td> 
  <td class="stentry"> <p>grått färgkomponentvärde (0...100%, decimalint) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>tvåsiffrigt hexadecimalt grått färgvärde (GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>fyrsiffrig hex-grå med alfafärgvärde (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>paketerat sexsiffrigt hexadecimalt RGB-färgvärde (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>packat åttasiffrigt hexadecimalt RGBA- (RRGGBBAA) eller CMYK-färgvärde (CCMYYKK) (om det anges med suffixet"k") </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>tio siffror hexadecimal CMYK med alfavärde (CCYMMKAA) </p> </td> 
 </tr> 
</table>

Decimalkomponentvärdena för RGB-färger ligger inom intervallet 0 till 255. Decimalkomponentvärdena för CMYK och grått ligger i intervallet 0,100 %. Alla hexadecimala komponentvärden ligger i intervallet 0...0xFF.

Färgkomponentvärdena antas vara oberoende av alfavärdet (inte förmultiplicerat).

Alla färgvärden, prefix och suffix är inte skiftlägeskänsliga.

Typsuffixet k krävs för CMYK-färgvärden. Ett typsuffix kan anges för RGB- och gråfärgvärden.

Prefixet 0x krävs för hexadecimala gråa färgvärden.

Suffixet s anger att färgvärdet är associerat med den inmatningsfärgrymd (källfärgrymd) som motsvarar färgvärdets pixeltyp (definierad med `attribute::IccProfileSrc*`). Om det här suffixet inte finns är färgvärdet associerat med utdatafärgrymden (mål) (definierad med `icc=` eller `attribute::IccProfile*`).

## Standard {#section-737082a7da544acca8092a48d88480e7}

Om ett alfavärde inte anges uttryckligen antas det vara 255, 0xFF eller 100 % (helt ogenomskinligt).

## Exempel {#section-4ac69026349949f8b595a6d4a9ce474d}

Några exempel på giltiga färgspecifikationer och deras motsvarande pixeltyp, färgvärde, alfavärde och standardfärgrymd:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>färg</i> </b> </th> 
   <th class="entry"> <b>Pixeltyp</b> </th> 
   <th class="entry"> <b>Färgvärde</b> </th> 
   <th class="entry"> <b>Alfavärde</b> </th> 
   <th class="entry"> <b>Standardfärgrymd  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160 177 194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>grå </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75 g </p> </td> 
   <td> <p>grå </p> </td> 
   <td> <p>50 % </p> </td> 
   <td> <p>75 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>grå </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>grå </p> </td> 
   <td> <p>87 % </p> </td> 
   <td> <p>93 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33 kB </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26 KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25 % </p> </td> 
   <td> <p>26 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13 % </p> </td> 
   <td> <p>14 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Den utdatafärgrymd som anges med `icc=` används i stället för standardfärgrymden när pixeltypen för en utdatafärg motsvarar pixeltypen för utdatabilden.
