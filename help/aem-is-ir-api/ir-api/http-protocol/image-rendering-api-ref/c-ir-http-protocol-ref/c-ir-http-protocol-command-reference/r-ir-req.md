---
description: Typ av begäran. Anger vilken typ av data som begärs.
seo-description: Typ av begäran. Anger vilken typ av data som begärs.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dd13338-3457-477f-96e7-3ace7266d0ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 0%

---


# req{#req}

Typ av begäran. Anger vilken typ av data som begärs.

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> debug  </span> </p> </td> 
  <td class="stentry"> <p>Kör kommandon i felsökningsläge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> innehåll  </span> </p> </td> 
  <td class="stentry"> <p>Returnera information om objekten i vinjetteringen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img  </span> </p> </td> 
  <td class="stentry"> <p>Kör kommandon och returnera den återgivna bilden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops  </span> </p> </td> 
  <td class="stentry"> <p>Returnerar egenskaper för den angivna vinjetteringen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> map  </span> </p> </td> 
  <td class="stentry"> <p>Returnerar data för bildscheman som är inbäddade i vinjetteringen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object  </span> </p> </td> 
  <td class="stentry"> <p>Kör kommandon och returnera den återgivna bilden som maskerats till den aktuella objektmarkeringen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> proppar  </span> </p> </td> 
  <td class="stentry"> <p>Kör kommandon och returnera egenskaper för svarsbilden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> användardata  </span> </p> </td> 
  <td class="stentry"> <p>Returnerar innehållet i <span class="codeph">-vinjett::UserData </span>. </p> </td> 
 </tr> 
</table>

Om inget annat anges i de detaljerade beskrivningarna returnerar servern textsvar med MIME-typen &lt;text/plain>.

`debug`

Kör de angivna kommandona och returnerar den återgivna bilden. Om ett fel inträffar returneras felinformation och felsökningsinformation i stället för felbilden ( `attribute::ErrorImagePath`).

`contents`

Returnerar en XML-representation av objekthierarkin i vinjetteringen, inklusive valda objektattribut. Andra kommandon i begäran ignoreras.

`img`

Kör de angivna kommandona och returnerar den återgivna bilden. Svarsdatans format och svarstyp bestäms av `fmt=`.

`imageprops`

Returnerar markerade egenskaper för den vinjettfil eller katalogpost som anges i URL-sökvägen. I [Egenskaper](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) finns en beskrivning av MIME-typen för svarssyntax och svar. Andra kommandon i begäran ignoreras. Följande egenskaper returneras:

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration  </span> </p> </td> 
   <td colname="col2"> <p>Dubbel </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Expiration  </span> or the default time to live. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td colname="col2"> <p>Heltal </p> </td> 
   <td colname="col3"> <p>Höjd med full upplösning i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Sträng </p> </td> 
   <td colname="col3"> <p>namn/beskrivning av profilen som är associerad med den här vinjetteringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile  </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 om den associerade profilen är inbäddad i vinjetteringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths  </span> </p> </td> 
   <td colname="col2"> <p>Boolean </p> </td> 
   <td colname="col3"> <p>1 om vinjetteringen bäddar in bandata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier  </span> </p> </td> 
   <td colname="col2"> <p>Sträng </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Modifier  </span> or empty if not a catalog entry. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>Svarsbildens pixeltyp. kan vara CMYK, RGB eller BW (för gråskalebilder). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Standardutskriftsupplösning i dpi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Sträng </p> </td> 
   <td colname="col3"> <p>Ändringsdatum/tid (från <span class="codeph">-katalog::TimeStamp </span> eller vinjettfilen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td colname="col2"> <p>Heltal </p> </td> 
   <td colname="col3"> <p>Full upplösningsbredd i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name  </span> </p> </td> 
   <td colname="col2"> <p>Sträng </p> </td> 
   <td colname="col3"> <p>Vinjettnamn (namnsträng för rotvinjetteringsobjektet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Maximal objektupplösning i <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materialupplösning </a> enheter (vanligen pixlar/tum). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Genomsnittlig objektupplösning i <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materialupplösning </a> enheter (vanligen pixlar/inc <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materialupplösning </a>h). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min  </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>Lägsta objektupplösning i <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> materialupplösning </a> enheter (vanligen pixlar/tum). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version  </span> </p> </td> 
   <td colname="col2"> <p>Heltal </p> </td> 
   <td colname="col3"> <p>Versionsnummer för vinjettfil. </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

Returnerar bildmappsdata som ingår i vinjetteringen. Som standard returneras kartdata för alla yttersta grupper. Kartdata för alla innersta grupper kan hämtas med

`req=map&groupLevel=-1`

Kartdata skalas inte till `wid=` eller `hei=` eller ändras inte på något annat sätt. MIME-typen för svar är `<text/xml>`.

Svarsdata består av ett `<map>`-element som innehåller en uppsättning `<area>`-element som liknar HTML-taggen `<AREA>`.

Varje `<area>`-element innehåller standardattributen `type=` och `coord=` samt ett `name=`-attribut som anger namn eller sökväg för vinjetteringsgruppen. Flera `<area>`-element med samma namn finns om maskerna för motsvarande objektgrupp har icke-kontinuerliga regioner.

Förutom standardattributen kan vinjetter definiera ytterligare attribut om de är skapade på det sättet. Sådana anpassade attribut definieras som objektgruppsattribut. Namnen på anpassade attribut måste börja med `map`. som ska inkluderas i `<area>`-elementen. Om gruppattributen till exempel innehåller `map.href=http://www.scene7.com` kommer motsvarande `<area>`-element att innehålla `href="http://www.scene7.com"`.

Ett XML-dokument med ett tomt `<map>`-element returneras om vinjetteringen inte innehåller mappningsdata.

`object`

Kör de angivna kommandona och returnerar den återgivna bilden som maskeras av markeringen för det kvarvarande objektet (gruppen eller objektet som markerats med det sista `sel=`- eller `obj=`-kommandot i begäran). Används vanligtvis tillsammans med ett bildformat som stöder alfa (se [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)). Om du använder ett bildformat som inte har stöd för alfa, blir områdena utanför masken svarta.

`props`

Kör de angivna kommandona och returnerar vinjettegenskaper och grupp- eller objektegenskaper i stället för den återgivna bilden. I [Egenskaper](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) finns en beskrivning av svarssyntaxen och MIME-svarstypen. Standardvalet gäller om inte `obj=` eller `sel=` också anges (se [ `obj=` ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)).

Följande egenskaper kan ingå i svaret:

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Egenskap </p> </th> 
   <th class="entry"> <p> Typ </p> </th> 
   <th class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> Sträng </p> </td> 
   <td> <p> Svarsbildens bakgrundsfärg. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p>Heltal </p> </td> 
   <td> <p> Svarets bildhöjd i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p>True if the ICC profile will be embedded in the reply image (see <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> Sträng </p> </td> 
   <td> <p> Kortkommandonamn för profilen som är associerad med svarsbilden (se <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True om svarsbilden innehåller alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> Boolean </p> </td> 
   <td> <p> True if the reply image includes path data (see <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> Sträng </p> </td> 
   <td> <p> Svarsbildtyp, kan vara CMYK, RGB eller BW (för gråskalebilder) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> Utskriftsupplösning (dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p>Heltal, boolesk </p> </td> 
   <td> <p> JPEG-kvalitet och chroma-flagga (se <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> Sträng </p> </td> 
   <td> <p> Mime-typ för svarsbilden (se <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p> Svarsbildens bredd i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes  </span> </p> </td> 
   <td> <p> Sträng </p> </td> 
   <td> <p> Attributsträng för den aktuella markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p> Antal objekt i den aktuella markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p> Dra in värdet för den aktuella markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> select  <span class="codeph"> selection.attributes  </span>ion.name  </span> </p> </td> 
   <td> <p> Sträng </p> </td> 
   <td> <p> Den fullständiga namnsökvägen för den aktuella objektmarkeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> markering.överlappande  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p> antalet överlappande objekt i den aktuella markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p>Antal återgivningsbara objekt i den aktuella markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p> Antal texturerbara objekt i den aktuella markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> markering.visible  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p> Aktuell status för att visa/dölja den aktuella markeringen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder  </span> </p> </td> 
   <td> <p> Heltal </p> </td> 
   <td> <p> Z-ordningsvärdet för det första överlappningsobjektet i den aktuella markeringen. </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

Returnerar innehållet i `vignette::UserData`. Servern ersätter alla förekomster av `'??'` i `vignette::UserData` med radavslutningar ( `<cr><lf>`). Svaret formateras som textdata med MIME-svarstypen inställd på &lt;text/plain>.

Om det objekt som anges i URL-sökvägen inte kan tolkas som en giltig post för vinjetteringsschema, eller om `vignette::UserData` är tom, innehåller svaret bara en radavslutning ( `CR/LF`).

Alla andra kommandon i begärandesträngen ignoreras.

## Egenskaper {#section-e44092e190ff4f6380583e8ed6ea5b0b}

Begär kommando. Kan förekomma var som helst i begärandesträngen.

## Standard {#section-00c593cbf1af4364b6b78812e6b93c64}

Om URL:en inte innehåller någon bildsökväg eller modifierare:

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Annars `req=img`

## Se även {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ,  [attribute::ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0),  [vignette::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85),  [Properties](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
