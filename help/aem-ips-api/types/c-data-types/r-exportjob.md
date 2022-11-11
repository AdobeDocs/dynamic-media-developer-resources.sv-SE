---
description: Jobbtyp som tillåter auktoriserad export av tidigare överförda filer.
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# [!DNL ExportJob]{#exportjob}

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> typer:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Lista över <span class="codeph"> assetHandle</span> som måste exporteras. Se <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL fmt]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng </span> </p> </td> 
   <td colname="col3"> <p>Anger typ av <span class="codeph"> export.Möjliga värden</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">If <span class="codeph"> fmt=orig</span>, exporteras resurserna som original </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">If <span class="codeph"> fmt=convert</span>konverteras resurserna till det format som anges i <span class="codeph"> is_modifer</span> eller <span class="codeph"> makro</span> indataparametrar </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL is_modifier]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng </span> </p> </td> 
   <td colname="col3"> <p>Anger <span class="codeph"> ImageServer</span> återgivnings-URL-sträng som bifogas till ExportJob <span class="codeph"> konvertera</span> begäran. </p> <p>Se <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/homeisir.html" scope="external" format="html"> IS-dokumentation</a> om du vill ha information om hur du skickar IS-modifierare. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL macro]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL clientId]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng </span> </p> </td> 
   <td colname="col3"> <p>Anger IP-adressen till den klient eller kund som initierade exportbegäran. </p> <p> <p>Obs! den här parametern är för närvarande inte aktivt ifylld och är endast reserverad för framtida användning. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

För ExportJob-begäranden där `fmt=convert` och både `is_modifier` och `macro` anges, målfilen uppfyller det format som anges i `macro`. Exempel:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
