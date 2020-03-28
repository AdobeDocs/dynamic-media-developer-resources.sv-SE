---
description: Källobjektsspecificerare. Bild-, SVG- och ICC-profilobjekt kan anges som bildkatalogsposter eller relativa filsökvägar
seo-description: Källobjektsspecificerare. Bild-, SVG- och ICC-profilobjekt kan anges som bildkatalogsposter eller relativa filsökvägar
seo-title: object
solution: Experience Manager
title: object
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# object{#object}

Källobjektsspecificerare. Bild-, SVG- och ICC-profilobjekt kan anges som bildkatalogsposter eller relativa filsökvägar

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span></span> </p> </td> 
  <td class="stentry"> <p>bildkatalogens namn ( <span class="codeph"> attribut::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span></span> </p> </td> 
  <td class="stentry"> <p>ID för bild-, SVG-, mall- eller ICC-profilposten i den angivna, huvud- eller standardbildkatalogen </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> bana </span></span> </p> </td> 
  <td class="stentry"> <p>relativa filsökvägar och namn för bild, mask eller ICC-profil </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objekt </span></span> </p> </td> 
  <td class="stentry"> <p>kan förekomma antingen i huvud-URL-sökvägen eller i ett <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>, eller <span class="codeph"> icc= </span> -kommando </p> </td> 
 </tr> 
</table>

*`rootId`* används för att identifiera en bildkatalog. (Mer information finns i [Bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) .) Om *`rootId`* anges i URL-sökvägen blir den katalogen *huvudkatalog* för den här begäran. I annat fall används standardkatalogen som huvudkatalog. Flera olika bildkataloger kan användas i samma begäran.

Servern antar inledningsvis att *`rootId`* utelämnas i `src=`, `mask=`och `icc=` kommandon och försöker hitta en katalogpost i huvudkatalogen. I praktiken försöker servern använda hela *`object`* strängen som *`objId.`*

Om en katalogpost hittas används den. I annat fall försöker servern sedan matcha en bildkatalogs utseende *`rootId`* . Om en katalog identifieras söks den efter *`objId`*. Om och post hittas används den.

Annars *`object`* antas vara en explicit filsökväg. I det här fallet, om `attribute::FullMatch` är inställt i huvudkatalogen, ignoreras katalogen för det här objektet och standardkatalogen används i stället. Om `attribute::FullMatch` inte anges används huvudkatalogen för vidare bearbetning.

Både *`rootId`* och *`objId`* är skiftlägeskänsliga. *`path`* är endast skiftlägeskänsligt på UNIX.

Om ett radavstånd (/) anges genomsöks standardkatalogen i stället för huvudkatalogen. Detta är praktiskt när en explicit sökväg kräver `default::RootPath` i stället för huvudkatalogens `attribute::RootPath`, men kan även användas för att få åtkomst till poster i standardkatalogen som annars skulle åsidosättas av poster i huvudkatalogen.

Se *Hantera innehåll* i *Serverkonfigurationsguiden* för mer information om hur *`path`* översätts till en fysisk filsökväg.

>[!NOTE]
>
>Kommatecken &#39;,&#39; får inte användas i *`object.`*

## Bildfilformat som stöds {#section-12c85aead78e4f759856ca9ff10637d7}

Se beskrivningen av verktyget IC (Image Converter) för en fullständig lista över filformat som stöds.

Program som kräver bilddata i flera olika upplösningar fungerar bäst när du använder det flerupplösta formatet Scene7-pyramid TIFF (PTIF). IC-verktyget används för att skapa PTIF-bilder från alla bildformat som stöds.

## Exempel {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Åtkomst till en bild och en ICC-profil i två olika bildkataloger**

Hämta bilden &#39; [!DNL myImage]&#39; i bildkatalogen som identifieras som &#39; [!DNL myCatalog]&#39; och bifoga ICC-profilen &#39; [!DNL sRGB]&#39; som finns i bildkatalogen &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Använda en enda bildkatalog med lager

**Skapa en enkel sammansatt bild som består av tre lager, som alla hämtas från &#39;[!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Få åtkomst till bildfiler direkt medan du fortfarande använder en katalog för att tillhandahålla attribut**

Åtkomst [!DNL my/image/path/myImage.tif]med de standardattribut för jpg som konfigurerats i `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Se även {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribut::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
