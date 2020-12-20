---
description: Omsamplingsläge. Väljer den omsamplings- och/eller interpoleringsalgoritm som ska användas för skalning av bilddata. Gäller även för rotation av textlager och storleksändring av sammansatta bilder under vyomformningen.
seo-description: Omsamplingsläge. Väljer den omsamplings- och/eller interpoleringsalgoritm som ska användas för skalning av bilddata. Gäller även för rotation av textlager och storleksändring av sammansatta bilder under vyomformningen.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# resMode{#resmode}

Omsamplingsläge. Väljer den omsamplings- och/eller interpoleringsalgoritm som ska användas för skalning av bilddata. Gäller även för rotation av textlager och storleksändring av sammansatta bilder under vyomformningen.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Väljer bilinjär standardinterpolation. Snabbaste omsamplingsmetod. vissa aliaseringsartefakter kan bli märkbara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bikub  </span> </p> </td> 
   <td colname="col2"> <p>Väljer bikubisk interpolation. Processorintensivare än bilinjär interpolation, men ger skarpare bilder med mindre framträdande aliasartefakter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> skarp2  </span> </p> </td> 
   <td colname="col2"> <p>Väljer en modifierad Lanczos Window-funktion som en interpoleringsalgoritm. Kan ge något tydligare resultat än bikubisk till en högre CPU-kostnad. <span class="codeph"> sharp  </span> har ersatts med  <span class="codeph"> sharp2  </span>som har en mindre sannolikhet att orsaka aliasing-artefakter (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Väljer Photoshop standardomsampling för att minska bildstorleken, som kallas"bikubisk skarpare" i Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-a171bacf4ddf43c782e46b86a16d443e}

Begär attribut. Gäller alla skalningsåtgärder som ingår i skapandet av den slutliga svarsbilden, inklusive all lagerskalning.

## Standard {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exempel {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Hämta en rendering av ett lager med bästa kvalitet som lagras i en bildkatalog. Bilden kan innehålla text. Vi räknar med att kunna fortsätta bearbeta bilden i ett bildredigeringsprogram och därför begära en alfakanal tillsammans med bilden.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Se även {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
