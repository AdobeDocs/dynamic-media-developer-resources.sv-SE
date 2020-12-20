---
description: Bildkonverteringsverktyg.
seo-description: Bildkonverteringsverktyg.
seo-title: ic
solution: Experience Manager
title: ic
topic: Scene7 Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: e0f8153b038446180ddad313e591828223ed31e9
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 0%

---


# ic {#ic}

Bildkonverteringsverktyg.

`ic` är ett kommandoradsverktyg som konverterar bildfiler till det optimerade Pyramid TIFF-formatet (PTIFF). Även om det går att bearbeta bilder utan konvertering rekommenderar vi att du konverterar alla bilder som är större än 512 x 512 pixlar till PTIFF. Denna konvertering ger optimal serverprestanda och resursanvändning och minimerar svarstiderna.

Vi rekommenderar att PTIFF-filer som innehåller fotografiskt innehåll är JPEG-kodade (ange `-jpegcompress`). Datorgenererat innehåll kan dra nytta av förlustfri komprimering (antingen `-deflatecompress` eller `-lzwcompress`). Om inte en färgkonvertering eller konvertering av pixeltyp krävs, överförs JPEG-källbilddata till PTIFF utan avkodning för att undvika kvalitetsförsämring. I det här fallet gäller de angivna komprimeringsalternativen bara för pyramidnivåerna med lägre upplösning.

Om du inte konverterar stora bilder behöver du inte ange parametrar som styr hur mycket minne som ska användas. Om du är det kan du dock ge `ic` mer minne genom att använda inställningen `-maxmem` som beskrivs nedan. En bra tumregel för att beräkna mängden minne som krävs är att multiplicera bildens bredd gånger bildens höjd gånger antalet kanaler. Fyra för en RGB-bild med tre alfavärden. Om kanalerna dessutom är 16 bitar per komponent i stället för 8 gånger det slutliga resultatet.

## Användning {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]` *`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]` *`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]` *`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>alternativ</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Kommandoalternativ (se nedan). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>En enda indatabildfil. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>PTIFF-fil för enstaka utdata (inte giltig om den används med SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Mapp som innehåller indatabilder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Mappen som utdata-PTIFF-filer skrivs till. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returnerar {#section-36a2dcfa39824d29b69547c432366219}

0 om det lyckas. Om ett fel inträffar returneras ett värde som inte är noll och felinformation skickas till `stderr`.

## Alternativ {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -okomprimerad  </span> </p> </td> 
   <td colname="col2"> <p>Komprimera inte utdatabilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress  </span> </p> </td> 
   <td colname="col2"> <p>Använd dekomprimering (zip) (standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>Använd LZW-komprimering (Lempel-Ziv-Welch). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>Använd JPEG-kodning. Ignoreras om <span class="codeph"> <span class="varname"> sourceFile </span> </span> innehåller alfakata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>JPEG-kvalitet (0-100; standard är 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplekrominans  </span> </p> </td> 
   <td colname="col2"> <p>Inaktivera JPEG-chroma-downsampling (kan förbättra kvaliteten på färgtext och bilder). Detta påverkar inte utdatabilder som är CMYK eller gråskala. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt;  &lt;&gt; threshold  </span>&gt;  &lt;&gt; monokrom  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Använd oskarp maskning på pyramidnivåer i delprov. Mer information finns i <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>. (Används inte för bilder med full upplösning.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>Använd klippsökvägen i källfilen, om det finns någon, för att skapa tillhörande alfadata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Utskriftsupplösning (dpi) för <span class="codeph"> <span class="varname"> destFile </span> </span>; om den inte anges kopieras utskriftsupplösningen för <span class="codeph"> srcFile </span> till <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop  &lt;&gt; corner  </span>&gt;  &lt;&gt; mode  </span>&gt;  &lt;&gt; olerans  </span>&gt;  &lt;&gt; infoFile  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Beräkna en beskärningsrektangel för att minimera en enfärgad bakgrund. Ingen beskärningsinformation genereras om algoritmen för automatisk beskärning skulle resultera i att hela bilden beskärs. </p> <p>Om du vill beräkna beskärningsrektangeln utan att konvertera bilden anger du <span class="codeph"> -autocrop </span> utan <span class="codeph"> -convert </span> och utan <span class="codeph"> <span class="varname"> målfil.</span> </span></p>

<p><i><b>corner</b></i> -ul | ur | alla | lr </p>
   <p> Anger vilket hörn i bilden som en startpunkt ska användas för. Ignoreras om läget är 1.</p>
   <p><i><b>läge</b></i>  - 0 | 1</p>
   <p>Ange 0 för beskärning baserat på färgen på den angivna hörnpixeln. fungerar på förmultiplicerade färgdata om alfadata är associerade med källbilden.</p>
   <p>Ange 1 för beskärning baserad på alfavärden. hörnet ignoreras och 0 är alltid startvärdet, ingen beskärning används om inga alfavärden är kopplade till källbilden.</p> 
   <p><i><b>tolerans</b></i>  - Matcha tolerans. Verkligt värde 0,0 till 1,0. Anger toleransen för att matcha pixelkomponentvärden. Ange 0 för exakta träffar.</p>
   <p><i><b>infoFile</b></i>  - Sökväg till och namn på den XML-utdatafil som beskärningsinfo ska skrivas till.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>Kopiera XMP metadata, om tillgängligt, från <span class="codeph"> <span class="varname"> sourceFile </span> </span> till <span class="codeph"> <span class="varname"> destFile </span> </span> utan ändring. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> Bädda in ICC-färgprofilen i <span class="codeph"> <span class="varname"> destFile </span> </span>, om den är tillgänglig (ingen profil bäddas in som standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Sökväg till och namn på en ICC-profilfil. Definierar färgrymden för <span class="codeph"> <span class="varname"> sourceFile </span> </span> och måste matcha dess pixeltyp. Ska bara anges om ingen profil är inbäddad i <span class="codeph"> <span class="varname"> sourceFile </span> </span> eftersom detta åsidosätter den inbäddade profilen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Sökväg till och namn på en ICC-profilfil. Definierar pixeltypen och färgrymden för <span class="codeph"> <span class="varname"> destFile </span> </span>. IC konverterar till den här profilen om <span class="codeph"> <span class="varname"> sourceFile </span> </span> har en inbäddad profil eller om <span class="codeph"> -imageprofile </span> också har angetts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual  </span> </p> </td> 
   <td colname="col2"> <p>Perceptuell återgivningsmetod för konvertering av färgrymd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric  </span> </p> </td> 
   <td colname="col2"> <p> Relativa färgvärden för återgivningsmetod för färgmodellskonverteringar (standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric  </span> </p> </td> 
   <td colname="col2"> <p>Absolut färgvärde för återgivningsmetod för färgmodellskonverteringar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>Mättnadsrenderingsmetod för konvertering av färgrymd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>Inaktivera svartpunktskompensation för vissa färgkonverteringar </p> <p>Aktiverat som standard. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>Inaktivera gitter (felspridning) vid färgkonvertering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype  </span> </p> </td> 
   <td colname="col2"> <p> Inaktivera automatisk konvertering från CMYK till RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>Tvinga avkodning och omkodning av JPEG-indatabilder. </p> <p> <b>Varning! </b> Om du använder det här alternativet kan bildkvaliteten försämras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>Använd standardfilter för omsampling av kvalitet (bilinjär). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>Använd ett omsamplingsfilter med högre kvalitet (Lanczos-fönster) (standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>Använd omsamplingsfilter med högre kvalitet (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BikubiskSharp  </span> </p> </td> 
   <td colname="col2"> <p>Nedsampla med Photoshop 8x8 bikubisk-skarp filter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> När det anges som det första alternativet undertrycks utdata av användningsinformation när ogiltiga alternativ påträffas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -overwrite  </span> </p> </td> 
   <td colname="col2"> <p>Tillåt att en befintlig <span class="codeph"> <span class="varname"> destFile </span> </span> skrivs över. Som standard läggs ett numeriskt suffix till i filnamnet för att förhindra att filen skrivs över. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden  </span> </p> </td> 
   <td colname="col2"> <p>Ignorera dolda källfiler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror  </span> </p> </td> 
   <td colname="col2"> <p>Avbryt inte bearbetningen när ett fel inträffar. Det har bara en effekt när du bearbetar flera filer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Loggfilens sökväg och namn (standardvärdet är <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel  &lt;&gt; level  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Loggnivå. </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 - Visa en lista över filer som ska bearbetas.</p>
   <p>1 - Lägg till rapportering för filer som inte behövs.</p>
   <p>2 - Lägg till förloppsrapportering.</p>
   <p>3 - Lägg till rapportering för varje fil som påträffas.</p>
   <p>4 - Lägg till förloppsrapportering på filnivå.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>Lägg till i loggfilen (standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>Skriv över loggfil. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressSsec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Loggningsintervall i msek för loggnivå 2 och senare (standard är 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; bytes  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Minnesanvändningsgräns. Måste vara minst 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent  &lt;&gt; percent  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Minnesanvändningsgräns. Standardvärdet är 25 % av det fysiska minnet. Om varken <span class="codeph"> maxmem </span> eller <span class="codeph"> maxmempercent </span> uttryckligen anges används maxmempercent-standard. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version  </span> </p> </td> 
   <td colname="col2"> <p> Returnera versionsinformation för det här verktyget. Ange utan andra alternativ. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Bildformat {#section-ab13d941d6724e65b9f84b62d949d31c} som stöds

I följande tabell visas de bildfilformat och formatalternativ som stöds av IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Format</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel </b> <b> TypeBits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Komprimering</b> </p> </th> 
   <th class="entry"> <p> <b> Anteckningar</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows-bitmapp) </p> </td> 
   <td> <p> RGB | indexerad </p> </td> 
   <td> <p> 3 | 5/6 | 8 </p> </td> 
   <td> <p> okomprimerad | RLE </p> </td> 
   <td> <p> 5/6 bitar/kanal anger stöd för 16-bitars RGB (5-5-5 och 5-6-5 bitar/kanal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMYK | RGB | grå </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binärt | JPEG </p> </td> 
   <td> <p> Endast EPS-filer som genererats av Photoshop stöds. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> indexerad </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> Om det finns något konverteras genomskinlighetsvärdet på paletten till alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | grå </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grå | grayA </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> okomprimerad | komprimerad </p> </td> 
   <td> <p> Endast sammanfogad bild; lager och extra kanaler ignoreras. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Endast bitmappsdata. vektordata ignoreras. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | grå | grayA | indexerad </p> </td> 
   <td> <p> 3 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> komprimerad </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | grå | grayA | indexerad </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> okomprimerad | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 | Paket </p> </td> 
   <td> <p> Med undantag för den första associerade alfakanalen ignoreras extra kanaler. </p> </td> 
  </tr> 
 </tbody> 
</table>

Inbäddade ICC-profiler känns igen i EPS-, JPG-, PSD-, PNG- och TIFF-filer.

Inbäddade sökvägar och XMP metadata känns igen i EPS-, JPG-, PSD- och TIFF-filer.

## Exempel {#section-3c1986b30315431989bd76b1ee5bef6d}

Konvertera en enda bild med bäst kvalitet och behåll den i samma mapp:

`ic -convert src/myFile.png src/myFile.tif`

Konvertera alla bilder i *`srcFolder`* till JPEG-kodad pyramid-TIFF och placera i *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Konvertera alla bilder i *`srcFolder`*. Den kodade bildinformationen för JPG-filer används för den förlustfria LZW-komprimeringen med full upplösning för resten av bildpyramidbilden för dessa bilder samt för hela utdatamilden för alla icke-JPG-indatafiler. Pixeltyper, inbäddade färgprofiler, XMP metadata osv. upprätthålls.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
