---
description: Source Object Specifier. Bild-, SVG- och ICC-profilobjekt kan anges som bildkatalogsposter eller relativa filsökvägar
solution: Experience Manager
title: object
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# object{#object}

Source Object Specifier. Bild-, SVG- och ICC-profilobjekt kan anges som bildkatalogsposter eller relativa filsökvägar

`*`object`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>bildkatalogens namn ( <span class="codeph"> attribut::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID för bild-, SVG-, mall- eller ICC-profilposten i angiven, huvud- eller standardbildkatalog </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>relativa filsökvägar och namn för bild, mask eller ICC-profil </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>kan förekomma antingen i huvud-URL-sökvägen eller i ett <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> eller <span class="codeph"> icc= </span> -kommando </p> </td> 
 </tr> 
</table>

*`rootId`* identifierar en bildkatalog. (Mer information finns i [Bildkatalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3).) Om *`rootId`* anges i URL-sökvägen blir den katalogen *huvudkatalog* för den här begäran. Annars används standardkatalogen som huvudkatalog. Flera olika bildkataloger kan användas i samma begäran.

Servern antar inledningsvis att *`rootId`* utelämnas i kommandona `src=`, `mask=` och `icc=` och försöker hitta en katalogpost i huvudkatalogen. I praktiken försöker servern använda hela strängen *`object`* som *`objId.`*

Om en katalogpost hittas används den, annars försöker servern matcha *`rootId`* för en bildkatalog. Om en katalog identifieras söks den efter *`objId`*. Om och post hittas används den.

Annars antas *`object`* vara en explicit filsökväg. Om `attribute::FullMatch` anges i huvudkatalogen ignoreras katalogen för det här objektet och standardkatalogen används i stället. Om `attribute::FullMatch` inte anges används huvudkatalogen för vidare bearbetning.

Både *`rootId`* och *`objId`* är skiftlägeskänsliga. *`path`* är endast skiftlägeskänslig på UNIX.

Om ett radavstånd `/` anges genomsöks standardkatalogen i stället för huvudkatalogen. Detta är i första hand användbart när en explicit sökväg kräver `default::RootPath` i stället för huvudkatalogens `attribute::RootPath`, men det kan också användas för att få åtkomst till poster i standardkatalogen som annars skulle åsidosättas av poster i huvudkatalogen.

Mer information om hur *`path`* översätts till en fysisk filsökväg finns i *Hantera innehåll* i *Konfigurationshandboken för servern*.

>[!NOTE]
>
>Kommatecken &#39;,&#39; tillåts inte i *`object.`*

## Bildfilformat som stöds {#section-12c85aead78e4f759856ca9ff10637d7}

Se beskrivningen av verktyget IC (Image Converter) för en fullständig lista över filformat som stöds.

Program som kräver bilddata i flera olika upplösningar fungerar bäst när du använder flerupplösningsformatet Dynamic Media pyramid TIFF (PTIF). IC-verktyget används för att skapa PTIF-bilder från alla bildformat som stöds.

## Exempel {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Åtkomst till en bild och en ICC-profil i två olika bildkataloger**

Hämta bilden [!DNL myImage] i bildkatalogen som identifieras som [!DNL myCatalog] och koppla ICC-profilen [!DNL sRGB] som finns i bildkatalogen med namnet [!DNL myProfiles]:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Använda en enda bildkatalog med lager

**Skapa en enkel sammansatt bild som består av tre lager, som alla hämtas från [!DNL myCatalog]:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Åtkomst till bildfiler direkt när en katalog används för att tillhandahålla attribut**

Åtkomst till [!DNL my/image/path/myImage.tif] med de standardattribut för jpg som konfigurerats i `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Se även {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
