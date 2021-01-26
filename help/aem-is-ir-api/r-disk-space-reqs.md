---
description: 'Utöver det utrymme som krävs för att installera programmet har Image Serving följande krav på diskutrymme '
solution: Experience Manager
title: Krav och rekommendationer för diskutrymme
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---


# Krav och rekommendationer för diskutrymme{#disk-space-requirements-and-recommendations}

Utöver det utrymme som krävs för att installera programmet har Image Serving följande krav på diskutrymme:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Beskrivning/standardplats/ Ange med</b> </th> 
   <th class="entry"> <b>Beräkning/rekommendation</b> </th> 
   <th class="entry"> <b>Kommentarer</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Källbilder, teckensnitt, ICC-profiler</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>Varianter; se kommentarerna nedan. </p> </td> 
   <td> <p>Endast behöver vara tillgänglig för Image Server. servrarna aldrig ändrar data. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache för HTTP-svarsdata</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2; minst 2 GB rekommenderas. </p> </td> 
   <td> <p>Det här cacheminnet lagrar även kapslade/inbäddade data och externa källbilder. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Datacache för bildkatalog</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>Tillåt att katalogmappen använder 1,5 gånger utrymmet. </p> </td> 
   <td> <p>Fylls i när kataloger läses in från början. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Loggdata</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>minst 100 MB. </p> </td> 
   <td> <p>Varierar beroende på loggningskonfiguration och serveranvändning. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Tillfälliga filer för Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MBytes räcker för de flesta användningsområden. </p> </td> 
   <td> <p>Kortlivade uppgifter. kan behövas för andra källbilder än PTIFF och vissa svarsbildformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Krav för diskutrymme för källbilder {#section-317da75099ad480d9a461c7e706d4f1c}

Du bör konvertera alla källbilder till PTIFF-format (pyramid TIFF) med kommandoradsverktyget Bildkonverterare (IC). Den här konverteringen ger optimala prestanda vid körning av Image Serving för alla program. Även om Image Server kan bearbeta alla källfilsformat som godkänts av IC har Dynamic Media inte stöd för sådana användningsområden.

När du använder PTIFF-filer kan följande reglage hjälpa dig att fastställa utrymmeskrav.

*`total_space`* (byte) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* Den genomsnittliga pixelstorleken (bredd x höjd) för alla ursprungliga källbilder. Om originalbilderna till exempel är ungefär 2 000 × 2 000 pixlar blir detta 4 MB.
* *`avg_num_components`* Beroende på vilken typ av bilder det är. För de flesta RGB-bilder är det 3, för de flesta CMYK- och RGBA-bilder är det 4. Använd 3.5 om hälften av bilderna är RGB och den andra hälften är RGBA.
* *`p_factor`* Beroende på den komprimeringstyp och kvalitet som anges när bilderna konverteras med IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF-komprimering</b> </th> 
   <th class="entry"> <b><i>p_faktor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Okomprimerad </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0,75, beroende på bilden </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG-komprimering </p> </td> 
   <td> <p> 1 (normalt för JPEG-kvalitet 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Denna uppskattning tar inte hänsyn till filsystemets belastning. Det faktiska diskutrymmet kan vara betydligt större.

**Exempel**

Vid en driftsättning av Image Serving förväntas 30 000 äldre bilder med låg upplösning och en genomsnittlig storlek på 500 × 500 RGB-pixlar användas. Nya bilddata med utskriftskvalitet förväntas läggas till med en hastighet på 10 000 per år. Den typiska CMYK-bildstorleken är 4 x 6 kB. Alla data komprimeras med JPEG-komprimering av hög kvalitet. Den totala mängden diskutrymme efter 3 års användning beräknas enligt följande:

*`total_space`* = 30 000 x (2 kB + 0,5 kB x 0,5 kB x 3 x 0,1) + 3 x 10 000 x (2 kB + 4 k x 6 kB x 4 x 0,1) = 2,2 G + 268 GB = ungefär 270 GB

För garanterad bästa kvalitet kan dekomprimering (zip) användas. Om du utgår från *`p_factor`* på 0,4 är den totala mängden diskutrymme som krävs ungefär 4 gånger större. I detta fall något mer än 1 TB.
