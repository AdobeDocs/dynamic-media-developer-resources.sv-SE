---
description: Jobbtyp som tillåter auktoriserad export av tidigare överförda filer.
seo-description: Jobbtyp som tillåter auktoriserad export av tidigare överförda filer.
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---


# ExportJob{#exportjob}

Jobbtyp som tillåter auktoriserad export av tidigare överförda filer.

ExportJob stöder inte följande resurstyper:

* Bilduppsättningar
* Återgivningsuppsättningar
* Snurra uppsättningar
* Medieuppsättningar
* Uppsättningar med flera bithastigheter
* Videouppsättningar
* eCatalogs
* Erbjudandeuppsättningar

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> typer:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Lista med <span class="codeph"> assetHandle</span> som måste exporteras. Se <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng  </span> </p> </td> 
   <td colname="col3"> <p>Anger typen <span class="codeph"> export.Möjliga värden</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Om <span class="codeph"> fmt=orig</span> exporteras resurserna som original </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Om <span class="codeph"> fmt=convert</span> konverteras resurserna till det format som anges i <span class="codeph"> is_modifer</span> eller <span class="codeph"> macro</span> indataparametrar </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng  </span> </p> </td> 
   <td colname="col3"> <p>Anger <span class="codeph"> ImageServer</span>-återgivnings-URL-strängen, som bifogas till begäran om konvertering<span class="codeph"> för ExportJob &lt;a2/&gt;.</span> </p> <p>Mer information om hur du skickar IS-modifierare finns i <a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> IS-dokumentationen</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> makro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng  </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng  </span> </p> </td> 
   <td colname="col3"> <p>Val av e-postinställning. Möjliga värden: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> Alla</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Fel</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> Jobbslutförande</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> Ingen</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng  </span> </p> </td> 
   <td colname="col3"> <p>Anger IP-adressen till den klient eller kund som initierade exportbegäran. </p> <p> <p>Obs!  den här parametern är för närvarande inte aktivt ifylld och är endast reserverad för framtida användning. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

För ExportJob-begäranden där `fmt=convert` och både `is_modifier` och `macro` anges, respekterar målfilen formatet som anges i `macro`. Exempel:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

