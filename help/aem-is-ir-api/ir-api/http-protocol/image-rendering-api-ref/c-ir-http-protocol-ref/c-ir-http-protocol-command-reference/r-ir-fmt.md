---
title: fmt
description: Svara i bildformat. Anger bildkodningsformatet för bilddata som skickas till klienten och motsvarande MIME-svarstyp för HTTP-svarshuvudet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# fmt {#fmt}

Svara i bildformat. Anger bildkodningsformatet för bilddata som skickas till klienten och motsvarande MIME-svarstyp för HTTP-svarshuvudet.

` fmt= *`format`*[,[ *`pixelType`*][, *`tiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> format </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>Förstörande JPEG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>Förstörande JPG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>förlustfri PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>förlustfri PNG med alfakanal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>TIFF med alfakanal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>Förstörande JPEG inbäddad i en Macromedia swf-fil. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>Förstörande JPEG och dekomprimerad mask inbäddad i en Macromedia swf-fil. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>PDF </p> </td> 
  <td class="stentry"> <p>Bilden är inbäddad i PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>Okomprimerad binär kapslad PostScript. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF med 256 färger. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF med 255 färger plus genomskinlighet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Returnera bilddata för RGB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>grå </p> </td> 
  <td class="stentry"> <p>Returnera gråskalebilddata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>Returnera CMYK-bilddata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>ingen </p> </td> 
  <td class="stentry"> <p>Okomprimerad. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>LZW-komprimering (icke-förstörande) (Lempel-Ziv-Welch). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Deflate-komprimering (icke-förstörande). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG-komprimering (förstörande). </p> </td> 
 </tr> 
</table>

*`pixelType`* Effekterar konvertering av utdatafärgrymd när `icc=` inte anges. Standardfärgprofilen som motsvarar *`pixelType`* används. Om färghantering är inaktiverat används tidigare konvertering. *`pixelType`* ignoreras när `icc=` anges, vilket avgör utdatapixeltypen.

*`compression`* Tillåts endast om tif, tif-alpha eller PDF har angetts som *`format`*. I tabellen nedan finns information om vilka komprimeringsalternativ som stöds för dessa bildformat.

`qlt-` Anger kodningsalternativ för JPEG för följande format: JPEG, TIFF med JPEG-komprimering, PDF med JPEG-komprimering och SWF. Använd `quantize=` om `fmt=gif` eller `fmt=gif-alpha`. Mer information finns i kommandobeskrivningarna. De andra formaten har inga inställningsbara alternativ.

Åtta bitar per pixelkomponent returneras för alla format och pixeltyper.

I följande tabell visas giltiga kombinationer av *`format`* och *`pixelType`*, motsvarande MIME-typer för HTTP-svar, om ICC-profiler kan bäddas in (se [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) och vilka formatspecifika kommandon som kan användas.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> format </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>MIME-typ för svar </p> </th> 
   <th colname="col4" class="entry"> <p>Bädda in ICC-profil </p> </th> 
   <th colname="col5" class="entry"> <p>Alternativ </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (ingen|lzw|zip|jpeg), pathEmbed=, qlt </span> </p> <p>( <span class="codeph"> qlt= </span> ignoreras såvida inte <span class="varname"> tiffCompression </span> är inställd på jpeg.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nej </p> <p>(Flashen Player ignorerar inbäddade ICC-profiler.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribut::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PDF </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (ingen|zip|jpeg),qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> ignoreras såvida inte <span class="varname"> tiffCompression </span> är inställd på jpeg.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> <p>(Data konverteras till palett efter konvertering till grå eller rgb.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nej </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Anger kodningsformat för svarsbilddata som skickas till klienten och motsvarande MIME-svarstyp för HTTP-svarsrubriken.

`png-alpha` Returnerar oassocierad alfa (d.v.s. alfa förmultiplicerar inte pixelvärdena), medan `tif-alpha` och `swf-alpha` returnerar associerad alfa (d.v.s. alfavärdena förmultipliceras med alfavärdena). Alfakanalen motsvarar den inverterade delen av vinjettens bakgrundsmask för `req=img` och gruppen eller objektmasken om det finns `req=object`. Om du vill använda alfa när du använder en kapslad IR-begäran lägger du till `fmt=` med lämpligt alfafilformat i den inbäddade IR-begäran och huvudbegäran. Inga alfavärden returneras om en CMYK- eller gråskale-ICC-profil har angetts med `icc=`.

## Egenskaper {#section-eb12a82c69d84622bcea153dd84d95b3}

Kan förekomma var som helst i begäran.

## Standard {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* har standardvärdet `attribute::Format` och *`tiffCompression`* har standardvärdet `attribute::TiffEncoding`. *`pixelType`* är som standard `rgb` om `icc=` inte anges, annars motsvarar det pixeltypen för den angivna ICC-profilen.

## Se även {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [attribute::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb), [&rbrace;kvantisera=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
