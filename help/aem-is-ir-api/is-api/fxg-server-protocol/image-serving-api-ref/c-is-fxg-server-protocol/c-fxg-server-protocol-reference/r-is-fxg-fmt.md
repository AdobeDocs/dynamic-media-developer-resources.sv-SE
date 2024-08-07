---
description: Svarsbildens format.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# fmt{#fmt}

Svarsbildens format.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | PDF | gif | gif-alpha | fxg | fxgraw </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Anger bildkodningsformatet för bilddata som skickas till klienten och motsvarande MIME-svarstyp för HTTP-svarshuvudet. </p> <p> <span class="codeph"> jpeg </span>: förstörande JPEG </p> <p> <span class="codeph"> png </span>: förlustfri PNG </p> <p> <span class="codeph"> png-alpha </span>: förlustfri PNG med alfakanal </p> <p> <span class="codeph"> tif </span>: TIFF </p> <p> <span class="codeph"> tif-alpha </span>: TIFF med alfakanal </p> <p> <span class="codeph"> swf </span>: förstörande JPEG inbäddad i en Adobe-swf-fil </p> <p> <span class="codeph"> pdf </span>: bild inbäddad i PDF </p> <p> <span class="codeph"> gif </span>: GIF med 2 till 256 färger </p> <p> <span class="codeph"> gif-alpha </span>: GIF med 2 till 255 färger plus genomskinlighet för nyckelfärg </p> <p> <span class="codeph"> fxg </span>: FXG med variabler och DOM-manipulering används </p> <p> <span class="codeph"> fxgraw </span>: ursprunglig FXG sparad på servern </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | grå | cmyk </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Kan användas för att påverka färgrymden för utdata. </p> <p> <span class="codeph"> rgb </span>: returnera RGB-bilddata </p> <p> <span class="codeph"> grå </span>: returnera gråskalebilddata </p> <p> <span class="codeph"> cmyk </span>: returnera CMYK-bilddata </p> </td> 
 </tr> 
</table>

`tiffCompression` tillåts bara om tif, tif-alpha har angetts som format. I tabellen nedan finns information om vilka komprimeringsalternativ som stöds för dessa bildformat.

`qlt=` kan användas för att ange kodningsalternativ för JPEG för följande format: JPEG, TIFF med JPEG-komprimering. Quantize= kan användas om fmt=gif eller fmt=gif-alpha. Mer information finns i kommandobeskrivningarna. De andra formaten har inga inställningsbara alternativ.

8 bitar per pixelkomponent returneras för alla format och `pixelTypes[7]`.

I följande tabell visas giltiga kombinationer av format och `pixelType`, motsvarande MIME-typer för HTTP-svar.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>MIME-typ för svar </p> </th> 
   <th colname="col4" class="entry"> <p>Bädda in ICC-profil </p> </th> 
   <th colname="col5" class="entry"> <p>Alternativ </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, grå </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression </span> (ingen) | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>PDF </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif-alfa </p> </td> 
   <td> <p>rgb, grå </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> kvantisera=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
