---
title: fmt
description: Svarsbildformat.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: b861d383d0a1af63ae18eb1e73231758c3352a55
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---

# fmt{#fmt}

Svarsbildformat.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | heic | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | PDF | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | Beskrivning |
|---|---|
| `avif-alpha` | Förstörande och förlustfri AVIF med alfakanal. |
| `avif` | Förstörande och förlustfri AVIF. |
| `eps` | Okomprimerad binär kapslad PostScript. |
| `f4m` | Flash Streaming Server-manifestformat. |
| `gif-alpha` | GIF med 2 till 255 färger plus genomskinlighet för nyckelfärger. |
| `gif` | GIF med 2 till 256 färger. |
| `heic` | Förlustfri HEIC. Det här formatet hämtas som standard från webbläsaren om det inte stöds. |
| `jpeg` | Förstörande JPEG. |
| `jpeg2000-alpha` | Förstörande och förlustfri JPEG 2000 med alfakanal. |
| `jpeg2000` | Förstörande och förlustfri JPEG 2000. |
| `jpegxr-alpha` | Förstörande och förlustfri JPEG XR med alfakanal. |
| `jpegxr` | Förstörande och förlustfri JPEG XR. |
| `jpg` | Förstörande JPG. |
| `m3u8` | Apple Streaming Server, manifestformat. |
| `pdf` | Bilden är inbäddad i PDF. |
| `pjpeg` | Progressiv JPEG. |
| `png-alpha` | 24-bitars förlustfri PNG med alfakanal. |
| `png` | 24-bitars förlustfri PNG. |
| `png8-alpha` | 8-bitars förlustfri PNG med alfakanal. |
| `png8` | 8-bitars förlustfri PNG. |
| `swf-alpha` | Förstörande JPEG och dekomprimerad mask inbäddad i en Adobe AS2-swf-fil. |
| `swf` | Förstörande JPEG inbäddad i en Adobe AS2-swf-fil. |
| `swf3-alpha` | Förstörande JPEG och dekomprimerad mask inbäddad i en Adobe AS3-swf-fil. **Obs!** swf- och swf-alpha-format används bäst för ActionScript 2-program (Flash Player 8 och tidigare). Formaten swf3 och swf3-alpha rekommenderas för ActionScript3-program (Flash Player 9 och senare). |
| `swf3` | Förstörande JPEG inbäddad i en SWF-fil i Adobe. |
| `tif-alpha` | TIFF med alfakanal. |
| `tif` | TIFF. |
| `webp-alpha` | Förstörande och förlustfri WebP med alfakanal. |
| `webp` | Förstörande och förlustfri WebP. |

| *`pixelType`* - rgb | grå | cmyk |
| *`pixelType`* | Beskrivning |
|---|---|
| `cmyk` | Returnera CMYK-bilddata. |
| `gray` | Returnera gråskalebilddata. |
| `rgb` | Returnera bilddata för RGB. |

| *`compression`* - jpeg | förstörande | förlustfri | lzw | ingen | zip |
| *`compression`* | Beskrivning |
|---|---|
| `jpeg` | JPEG-komprimering (förstörande). |
| `lossy` | JPEG 2000, JPEG XR-komprimering (förstörande) och WebP. |
| `lossless` | HEIC, JPEG 2000, JPEG XR-komprimering (icke-förstörande) och WebP. |
| `lzw` | LZW-komprimering (icke-förstörande) (Lempel-Ziv-Welch). |
| `none` | Okomprimerad. |
| `zip` | Deflate-komprimering (icke-förstörande). |

* *`format`* anger bildkodningsformatet för bilddata som skickas till klienten och motsvarande MIME-svarstyp för HTTP-svarshuvudet.
* *`pixelType`* kan användas för att påverka konvertering av färgrymd för utdata när `icc=` inte har angetts.

  Standardfärgprofilen som motsvarar *`pixelType`* används. Om färghantering är inaktiverat används tidigare konvertering. *`pixelType`* ignoreras när `icc=` anges, vilket avgör utdatapixeltypen.

* *`compression`* tillåts bara om `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr` eller `jpegxr-alpha` har angetts som *`format`*. I tabellen nedan finns information om vilka komprimeringsalternativ som stöds för dessa bildformat.

Du kan använda `qlt=` för att ange kodningsalternativ för JPEG för följande format: JPEG, TIFF med JPEG-komprimering, PDF med JPEG-komprimering och SWF. WebP, JPEG 2000 och JPEG XR använder också `qlt=`, men värdena ger olika kvaliteter för de olika formaten. Använd `quantize=` om `fmt=gif` eller `fmt=gif-alpha`. Mer information finns i kommandobeskrivningarna. De andra formaten har inga inställningsbara alternativ.

8 bitar per pixelkomponent returneras för alla *`formats`* och *`pixelTypes`* (8 bitar per pixel för GIF).

I följande tabell visas giltiga kombinationer av *`format`*och *`pixelType`*, motsvarande MIME-typer för HTTP-svar, om ICC-profiler kan bäddas in (se [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) och vilka formatspecifika alternativ du kan använda.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format </i> </b> </th> 
   <th class="entry"> <b> <i> pixelType </i> </b> </th> 
   <th class="entry"> <b> MIME-svarstyp </b> </th> 
   <th class="entry"> <b>Bädda in ICC-profil</b> </th> 
   <th class="entry"> <b> alternativ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>Nej </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> komprimering </span> </span> ( <span class="codeph"> förstörande </span>, <span class="codeph"> förlustfri </span>) </p> <p> <span class="codeph"> qlt= </span> ignoreras för <span class="codeph"> förlustfri </span>. </p> <p>Eftersom det inte finns något koncept för krominanshämtning med WebP-formatet ignoreras det andra värdet ( <span class="codeph"> qlt </span>) om du använder ett andra värde (till exempel <span class="codeph"> qlt=80,1 </span>). <span class="codeph"> 1 </span> ignoreras. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> <p>Data konverteras till palett efter konvertering till grå eller rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nej </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> kvantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nej </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, grå </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Nej </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> komprimering </span> </span> ( <span class="codeph"> förstörande </span>, <span class="codeph"> förlustfri </span>) </p> <p> <span class="codeph"> qlt= </span> ignoreras för <span class="codeph"> förlustfri </span>. </p> <p>Eftersom det inte finns något koncept för krominanshämtning med WebP-formatet ignoreras det andra värdet ( <span class="codeph"> qlt </span>) om du använder ett andra värde (till exempel <span class="codeph"> qlt=80,1 </span>). <span class="codeph"> 1 </span> ignoreras. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>Parametern <span class="codeph"> pscan= </span> gäller bara för pjpeg-format. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Nej </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> komprimering </span> </span> ( <span class="codeph"> förstörande </span>, <span class="codeph"> förlustfri </span>) </p> <p> <span class="codeph"> qlt= </span> ignoreras för <span class="codeph"> förlustfri </span>. </p> <p>Eftersom det inte finns något koncept för krominanshämtning med WebP-formatet ignoreras det andra värdet ( <span class="codeph"> qlt </span>) om du använder ett andra värde (till exempel <span class="codeph"> qlt=80,1 </span>). <span class="codeph"> 1 </span> ignoreras. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> PDF </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> komprimering </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> ignoreras såvida inte <span class="codeph"> <span class="varname"> compression </span> </span> är inställd på <span class="codeph"> jpeg </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nej </p> <p> <p>Obs! Flashen Player Adobe ignorerar inbäddade ICC-profiler. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribut::TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> komprimering </span> </span> <p> ( <span class="codeph"> ingen|lzw|zip|jpeg </span>) </p> <p>Endast tiff; tiff-alpha stöder inte jpeg-komprimering. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> ignoreras såvida inte <span class="varname"> compression </span> är inställd på <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;bild/webp&gt; </span> </p> </td> 
   <td> <p>Nej </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> komprimering </span> </span> ( <span class="codeph"> förstörande </span>, <span class="codeph"> förlustfri </span>) </p> <p> <span class="codeph"> qlt= </span> ignoreras för <span class="codeph"> förlustfri </span>. </p> <p>Eftersom det inte finns något koncept för krominanshämtning med WebP-formatet ignoreras det andra värdet ( <span class="codeph"> qlt </span>) om du använder ett andra värde (till exempel <span class="codeph"> qlt=80,1 </span>). <span class="codeph"> 1 </span> ignoreras. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Begär attribut. Tillämpas oavsett aktuell lagerinställning om `req=img` (standard) eller `req=mask`; annars ignoreras.

*`type`* ignoreras om `iccProfile=` anges.

## Standard {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, där *`defaultType`* hanteras enligt följande: Om `icc=` anges motsvarar *`defaultType`* pixeltypen för den angivna ICC-profilen. Om `icc=` inte anges är *`defaultType`* `gray` om `req=mask`, annars är det `rgb`.

## Exempel {#section-b93222e652df404a84c69025247f07df}

**Begär en liten förhandsvisningsbild med låg kvalitet i JPEG-format (standard):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Begär samma bild konverterad till gråskala:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Begär samma bild i ett förlustfritt format med alfakanal och hög upplösning:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Begär alfakanalen för samma bild som en TIFF-bild i gråskala:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Konvertera samma bild till cmyk med ICC-standardprofilerna:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Konvertera samma bild till CMYK med en annan ICC-profil och bädda in profilen i TIFF-bilden:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Leverera den här bilden som en TIF-fil med JPEG-komprimering utan konvertering av pixeltyp:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Konvertera en bild till ett GIF med två toner med transparens och tvinga färger till svartvitt:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Förstörande med kvalitetsinställningen 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Icke-förstörande med alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Förstörande med kvalitetsinställningen 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Icke-förstörande med alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Förstörande med kvalitetsinställningen 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Icke-förstörande med alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Se även {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [kvantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
