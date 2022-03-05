---
description: Omsamplingsläge. Väljer den omsamplings- och/eller interpoleringsalgoritm som ska användas för skalning av bilddata. Gäller även för rotation av textlager och storleksändring av sammansatta bilder under vyomformningen.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# resMode{#resmode}

Omsamplingsläge. Väljer den omsamplings- och/eller interpoleringsalgoritm som ska användas för skalning av bilddata. Gäller även för rotation av textlager och storleksändring av sammansatta bilder under vyomformningen.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Väljer bilinjär standardinterpolation. Snabbaste omsamplingsmetod. vissa aliaseringsartefakter är märkbara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bikub </span> </p> </td> 
   <td colname="col2"> <p>Väljer bikubisk interpolation. Processorintensivare än bilinjär interpolation, men ger skarpare bilder med mindre framträdande aliasartefakter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> skarp2 </span> </p> </td> 
   <td colname="col2"> <p>Väljer en modifierad Lanczos Window-funktion som en interpoleringsalgoritm. Kan ge något tydligare resultat än bikubisk till en högre processorkostnad. <span class="codeph"> skarp </span> har ersatts med <span class="codeph"> skarp2 </span>, vilket är mindre sannolikt att orsaka aliasing-artefakter (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Väljer Photoshop standardomsampling för att minska bildstorleken, som kallas"bikubisk skarpare" i Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Bevara bildens proportioner när du använder båda `resMode=bisharp` och `fit=stretch`är det bäst att använda parametern width eller height. Om båda parametrarna måste definieras kan du kapsla in dem i ett annat lager, vilket visas i följande exempel:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Egenskaper {#section-a171bacf4ddf43c782e46b86a16d443e}

Begär attribut. Gäller alla skalningsåtgärder som ingår i skapandet av den slutliga svarsbilden, inklusive all lagerskalning.

## Standard {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exempel {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Hämta en rendering av ett lager med bästa kvalitet som lagras i en bildkatalog. Bilden kan innehålla text. Bilden bearbetas vidare i ett bildredigeringsprogram och begär därför en alfakanal tillsammans med bilden.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Se även {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
