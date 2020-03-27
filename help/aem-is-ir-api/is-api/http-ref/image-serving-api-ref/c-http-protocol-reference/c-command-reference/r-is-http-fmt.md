---
description: Svarsbildformat.
seo-description: Svarsbildformat.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
translation-type: tm+mt
source-git-commit: f490c0b927679917d5fbf3553e60aa90952735c3

---


# fmt{#fmt}

Svarsbildformat.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*]]

*`format`* — jpeg| jpg| pjpeg| png| png8| png-alpha| png8-alpha| tif| tif-alpha| swf| swf-alpha| swf3| swf3-alpha| eps| gif| gif-alpha| m3u8| f4m| webb| webp-alpha| jpeg2000| jpeg2000-alpha| jpegxr| jpegxr-alpha

| *`format`* | Beskrivning |
|---|---| 
| `jpeg` | Förstörande JPEG |
| `jpg` | Förstörande JPG |
| `pjpeg` | Progressiv JPEG |
| `png` | 24-bitars förlustfri PNG |
| `png8` | 8-bitars förlustfri PNG |
| `png-alpha` | 24-bitars förlustfri PNG med alfakanal |
| `png8-alpha` | 8-bitars förlustfri PNG med alfakanal |
| `tif` | TIFF |
| `tif-alpha` | TIFF med alfakanal |
| `pdf` | Bild inbäddad i PDF |
| `eps` | Okomprimerad binär kapslad PostScript |
| `gif` | GIF med 2 till 256 färger |
| `gif-alpha` | GIF med 2 till 255 färger plus genomskinlighet för nyckelfärger |
| `swf` | Förstörande JPEG inbäddad i en Adobe AS2 swf-fil |
| `swf-alpha` | Förstörande JPEG och dekomprimerad mask inbäddad i en Adobe AS2 swf-fil |
| `swf3` | Förstörande JPEG inbäddad i en Adobe AS3 swf-fil |
| `swf3-alpha` | Förstörande JPEG och en dekomprimerad mask som är inbäddad i en Adobe AS3 swf-fil. **Obs**: swf- och swf-alpha-formaten används bäst för ActionScript 2-program (Flash Player 8 och tidigare). swf3 och swf3-alpha rekommenderas för ActionScript3-program (Flash Player 9 och senare) |
| `m3u8` | Manifestformat för Apple Streaming Server |
| `f4m` | Manifestformat för Flash Streaming Server |
| `webp` | Förstörande och förlustfri WebP |
| `webp-alpha` | Förstörande och icke-förstörande WebP med alfakanal |
| `jpeg2000` | Förstörande och förlustfri JPEG 2000 |
| `jpeg2000-alpha` | Förstörande och förlustfri JPEG 2000 med alfakanal |
| `jpegxr` | Förstörande och förlustfri JPEG XR |
| `jpegxr-alpha` | Förstörande och förlustfri JPEG XR med alfakanal |


| *`pixelType`* — rgb | grå | cmyk |
| *`pixelType`* | Beskrivning |
|---|---|
| `rgb` | Returnera RGB-bilddata. |
| `gray` | Returnera gråskalebilddata. |
| `cmyk` | Returnera CMYK-bilddata. |

| *`compression`* - ingen | lzw | zip | jpeg | förstörande | förlustfri |
| *`compression`* | Beskrivning |
|---|---|
| `none` | Okomprimerad |
| `lzw` | LZW-komprimering (icke-förstörande) |
| `zip` | &quot;Deflate&quot;-komprimering (icke-förstörande) |
| `jpeg` | JPEG-komprimering (förstörande) |
| `lossy` | WebP-, JPEG 2000- och JPEG XR-komprimering (förstörande) |
| `lossless` | WebP-, JPEG 2000- och JPEG XR-komprimering (icke-förstörande) |

* *`format`* anger bildkodningsformatet för bilddata som skickas till klienten och motsvarande MIME-svarstyp för HTTP-svarshuvudet.
* *`pixelType`* kan användas för att påverka konvertering av färgrymd för utdata när `icc=` inte har angetts.

   Standardfärgprofilen som motsvarar *`pixelType`* används. Om färghantering är inaktiverat används tidigare konvertering. *`pixelType`* ignoreras när `icc=` anges, vilket anger utdatapixeltypen.

* *`compression`* är endast tillåtet om `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`eller `jpegxr-alpha` anges som *`format`*. I tabellen nedan finns information om vilka komprimeringsalternativ som stöds för dessa bildformat.

Du kan använda `qlt=` för att ange JPEG-kodningsalternativ för dessa format: JPEG, TIFF med JPEG-komprimering, PDF med JPEG-komprimering och SWF. WebP, JPEG 2000 och JPEG XR använder också `qlt=` men värdena ger olika kvaliteter för de olika formaten. Använd `quantize=` if `fmt=gif` eller `fmt=gif-alpha`. Mer information finns i kommandobeskrivningarna. De andra formaten har inga inställningsbara alternativ.

8 bitar per pixelkomponent returneras för alla *`formats`* och *`pixelTypes`* (8 bitar per pixel för GIF).

I följande tabell visas giltiga kombinationer av *`format`*och *`pixelType`*, motsvarande MIME-typer för HTTP-svar, om ICC-profiler kan bäddas in (se [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) och vilka formatspecifika alternativ du kan använda.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i></b> </th> 
   <th class="entry"> <b> <i> pixelType</i></b> </th> 
   <th class="entry"> <b> MIME-typ för svar</b> </th> 
   <th class="entry"> <b>Bädda in ICC-profil</b> </th> 
   <th class="entry"> <b> Alternativ</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>Parametern <span class="codeph"> pscan= </span> gäller bara för pjpeg-format. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> komprimering </span></span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>endast tiff; tiff-alpha stöder inte jpeg-komprimering. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> ignoreras om inte <span class="varname"> komprimering </span> är inställd på <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nej </p> <p> <p>Obs!  Inbäddade ICC-profiler ignoreras i Adobe Flash Player. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribut::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> komprimering </span></span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> ignoreras såvida inte <span class="codeph"> komprimeringen <span class="varname"></span> är inställd på </span> jpeg <span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Ja </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, grå </p> <p>Data konverteras till palett efter konvertering till grå eller rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Nej </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> kvantifiera= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webb, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>Nej </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> komprimering </span> </span> ( <span class="codeph"> förstörande </span>, <span class="codeph"> icke-förstörande </span>) </p> <p> <span class="codeph"> qlt= </span> ignoreras för <span class="codeph"> förlustfri </span>. </p> <p>Eftersom det inte finns något koncept för nedsampling av krominanser i WebP-formatet, ignoreras det andra värdet ( <span class="codeph"> 1 </span> ) om du använder ett andra värde med <span class="codeph"> qlt </span>(till exempel <span class="codeph"> qlt=80,1 </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, grå </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Nej </p> </td> 
   <td> <p>Samma som ovan. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Nej </p> </td> 
   <td> <p>Samma som ovan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Begär attribut. Tillämpas oavsett aktuell lagerinställning om `req=img` (standard) eller `req=mask`. i annat fall ignoreras.

*`type`* ignoreras om `iccProfile=` anges.

## Standard {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, där *`defaultType`* hanteras enligt följande: Om `icc=` anges motsvarar *`defaultType`* pixeltypen för den angivna ICC-profilen. Om `icc=` inte anges, *`defaultType`* är `gray` if `req=mask`, annars är det `rgb`.

## Exempel {#section-b93222e652df404a84c69025247f07df}

**Begär en liten förhandsvisningsbild med låg kvalitet i JPEG-format (standard):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Begär att samma bild konverteras till gråskala:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Föreslå samma bild i ett förlustfritt format med alfakanal och hög upplösning:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Begär alfakanalen för samma bild som en TIFF-bild i gråskala:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Konvertera samma bild till CMYK med ICC-standardprofilerna:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Konvertera samma bild till CMYK med en annan ICC-profil och bädda in profilen i TIFF-bilden:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Leverera bilden som en TIF-fil med JPEG-komprimering utan konvertering av pixeltyp:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Konvertera bilden till en GIF-bild med två toner och genomskinlighet och tvinga färger till svartvitt:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Förstörande med en kvalitetsinställning på 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Icke-förstörande med alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Förstörande med en kvalitetsinställning på 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Icke-förstörande med alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Förstörande med en kvalitetsinställning på 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Icke-förstörande med alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Se även {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [Quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)pathEmbed=¥,¥pscan¥¥.
