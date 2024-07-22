---
title: Krav och rekommendationer för diskutrymme
description: Förutom det utrymme som krävs för att installera programmet har Image Serving följande krav på diskutrymme.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Krav och rekommendationer för diskutrymme{#disk-space-requirements-and-recommendations}

Förutom det utrymme som krävs för att installera programmet har Image Serving följande krav på diskutrymme:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Beskrivning/Standardplats/Ange med</b> </th> 
   <th class="entry"> <b>Beräkning/rekommendation</b> </th> 
   <th class="entry"> <b>Kommentarer</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Source-bilder, teckensnitt, ICC-profiler</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varierar; se kommentarerna nedan. </p> </td> 
   <td> <p>Endast måste vara tillgänglig för Image Server; servrarna ändrar aldrig data. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP-svarsdatacache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; minst 2 GB rekommenderas. </p> </td> 
   <td> <p>Det här cacheminnet lagrar även kapslade/inbäddade data och externa källbilder. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Datacache för bildkatalog</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Tillåt att katalogmappen använder 1,5 gånger utrymmet. </p> </td> 
   <td> <p>Fylls i när kataloger läses in från början. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Loggdata</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 MB eller mer. </p> </td> 
   <td> <p>Det varierar beroende på loggningskonfigurationen och serveranvändningen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Tillfälliga filer för Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MB räcker för de flesta användningsområden. </p> </td> 
   <td> <p>Kortlivade data; kan behövas för andra källbilder än PTIFF och vissa svarsbildformat. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Krav på diskutrymme för källbilder {#section-317da75099ad480d9a461c7e706d4f1c}

Adobe rekommenderar att du konverterar alla källbilder till PTIFF-formatet (pyramid TIFF) med kommandoradsverktyget Bildkonverterare (IC). Den här konverteringen ger optimala prestanda vid körning av Image Serving för alla program. Även om Image Server kan bearbeta alla källfilsformat som godkänts av IC, stöder inte Dynamic Media sådan användning.

När du använder PTIFF-filer kan följande reglage hjälpa dig att fastställa utrymmeskrav.

*`total_space`* (byte) = *`number_of_images`* × (2000 + *`avg_pixel_count`* x *`avg_num_components`* × *`p_factor`*)

* *`avg_pixel_count`* Den genomsnittliga pixelstorleken (bredd x höjd) för alla ursprungliga källbilder. Om originalbilderna till exempel är ungefär 2 000 × 2 000 pixlar är det 4 megapixlar.
* *`avg_num_components`* beror på vilken typ av bilder det är. För bilder i RGB är det 3 och för de flesta CMYK- och RGBA-bilder är det 4. Använd 3.5 om halva bilden är RGB och den andra hälften är RGBA.
* *`p_factor`* beror på den komprimeringstyp och kvalitet som anges när bilderna konverteras med IC.

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
   <td> <p> 1 (typiskt för JPEG-kvalitet 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Denna uppskattning tar inte hänsyn till filsystemets belastning. Det faktiska utrymmet på disken kan vara betydligt större.

**Exempel**

Vid en driftsättning av Image Serving förväntas 30 000 lågupplösta äldre bilder användas, med en genomsnittlig storlek på 500 × 500 RGB. Nya bilddata med utskriftskvalitet läggs till med en hastighet på 10 000 per år. Den typiska CMYK-bildstorleken är 4k × 6k byte. Alla data komprimeras JPEG med hög kvalitet. Den totala mängden diskutrymme efter tre års användning beräknas enligt följande:

*`total_space`* = 30 000 × (2k + 0,5k × 0,5k × 3 × 0.1) + 3 × 10 000 × (2k + 4k × 6k × 4 × 0.1) = 2,2 G + 268 GB = cirka 270 GB

För bästa möjliga kvalitet kan komprimering som zip användas. Om *`p_factor`* är 0,4 är den totala mängden diskutrymme som krävs ungefär fyra gånger större. I det här fallet, något mer än 1 terabyte.
