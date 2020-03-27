---
description: Materialfil. Anger materialdata, antingen i form av en enstaka materialkatalogreferens eller som en eller två bild- eller materialdatafiler avgränsade med kommatecken.
seo-description: Materialfil. Anger materialdata, antingen i form av en enstaka materialkatalogreferens eller som en eller två bild- eller materialdatafiler avgränsade med kommatecken.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# src{#src}

Materialfil. Anger materialdata, antingen i form av en enstaka materialkatalogreferens eller som en eller två bild- eller materialdatafiler avgränsade med kommatecken.

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileembeddedRequestFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">{'is{'<span class="varname"> isReq</span>'}}|{'ir{'<span class="varname"> irReq</span>'}'|{'{'<span class="varname"> foreignReq</span>'}'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID för materialkatalog (<span class="codeph"> attribute::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Materialkatalogpost (<span class="codeph"> katalog::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Materialformatfil (<span class="filepath"> .vnc</span> eller <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Bilddatafil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Begär bildvisning. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Begäran om bildåtergivning. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Begär till en extern server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Namnet på ett inbäddat material. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>0-baserat indexnummer för ett inbäddat material. </p></td> 
 </tr> 
</table>

Repeterbart textur-, dekal- och skrivbordsmaterial kräver en enda bild, som kan anges som en fil eller inbäddad begäran.

Kabinettmaterial kräver en kabinettformatfil ( [!DNL .vnc]), som inte kan anges som en kapslad begäran. En texturbildfil är valfri för skåp, och om den anges kan den vara antingen en fil eller en inbäddad begäran.

Fönsteromslagsmaterial kräver en fönsteromslagsformatfil ( [!DNL .vnw]), som inte kan anges som en kapslad begäran. En texturfil är valfri och om den anges kan den vara antingen en fil eller en inbäddad begäran.

Vid bildåtergivning används samma regler som för bildservrar när du söker efter materialkataloger, katalogposter och datafiler. Mer information finns i beskrivningen av *`object`* datatypen i dokumentationen för bildservrar.

*`materialFile`* är en sökväg som är relativ till `attribute::RootPath`.

*`foreignReq`* kan antingen vara en relativ URL-adress `attribute::RootUrl`eller en absolut URL-adress om `attribute::AllowDirectUrls` har angetts.

Om *`catId`* inte anges används sessionskatalogen.

`srcE=` och `srcN=` ge tillgång till material som är inbäddat i vinjetteringen.

## Filformat som stöds {#section-f2186d3eef834fc8bbecb2bc68daacad}

Bildåtergivning stöder samma källbildformat som Scene7 Image Serving.

Program som kräver bilddata i flera olika upplösningar fungerar bäst när du använder det flerupplösta formatet Scene7-pyramid TIFF (PTIFF). Image Serving innehåller verktyget Image Converter (IC) som skapar PTIFF-bilder i alla format som stöds.

Se beskrivningen av verktyget IC i dokumentationen för Image Serving för en fullständig lista över filformat som stöds.

## Egenskaper {#section-e68d03788d534e2184147987d51dfd0f}

Materialattribut. Krävs för alla material utom enfärgade (tillåts inte för enfärgade material). Alla strängar är skiftlägeskänsliga. *`index`* måste vara 0 eller större.

## Standard {#section-dde549c1917540dc8f9555962202da3c}

Ingen.

## Exempel {#section-675865444f8a4d35b9fc6e58b36e3438}

En MSS för ett färgat skåp med en separat upprepningsbar textur:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

Samma material kan finnas i en materialkatalog `'cat`i posten `12-3-2`:

`…&obj=cabinets&src=cat/12-3-2&…`

En kapslad begäran till Image Serving om att få en texturbild:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Se även {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Materialkataloger](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attribut::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribut::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
