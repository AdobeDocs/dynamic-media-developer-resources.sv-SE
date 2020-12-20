---
description: Image Serving implementerar en enkel funktion för visuell vattenstämpel.
seo-description: Image Serving implementerar en enkel funktion för visuell vattenstämpel.
seo-title: Vattenstämplar
solution: Experience Manager
title: Vattenstämplar
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Vattenstämplar{#watermarks}

Image Serving implementerar en enkel funktion för visuell vattenstämpel.

En vattenstämpel är vanligtvis en halvgenomskinlig bild, men det kan vara text eller en mer komplex sammansatt bild i flera lager. Servern lagrar vattenstämpeln över svarsbilden när alla visningsattribut ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) har tillämpats.

Vattenstämplar aktiveras genom att `attribute::Watermark` ställs in på en giltig katalogpost som skulle innehålla vattenstämpelbilden eller mallen. Om `attribute::Watermark` anges i en namngiven katalog kommer servern att lägga till vattenstämpeln i alla bildbegäranden som refererar till katalog-ID:t i begärande-URL:en. Om `default::Watermark` är inställt (i standardkatalogen [!DNL default.ini]) används vattenstämpeln på alla bildbegäranden oavsett om de refererar till en katalog eller inte.

Vattenstämplar tillämpas inte på bilder som returneras som svar på miniatyrbildsbegäranden ( `req=tmb`) och vissa begäranden från Scene7-visningsprogram.

## Skalning och justering {#section-89ef9e5926ae438abbd8e70332749b76}

När en vattenstämpel har angetts genererar servern först den sammansatta bilden (målbilden **) som vattenstämpeln ska användas på (innan vyomformningarna används). Servern genererar sedan den sammansatta bilden för vattenstämpeln precis som andra bilder (vattenstämpelbilden *a1/>).*

Till skillnad från standardbilder kan `sizeN=` anges för layer=0 eller layer=comp för vattenstämpelbilden. Det gör att vattenstämpelbilden kan skalas i förhållande till målbilden. Om `sizeN=` inte anges behåller vattenstämpelbilden sin pixelstorlek när den sammanfogas med målbilden.

Begärankommandon (till exempel `fmt=`) och visningskommandon (till exempel `wid=`) ignoreras i vattenstämpelposter, med undantag för `align=`. `align=` kan användas för att placera vattenstämpelbilden i förhållande till vattenstämpelbilden i förhållande till målbilden. Det gör att vattenstämpeln kan placeras i förhållande till ett hörn eller en kant på målbilden.

Efter skalning och justering kommer servern att placera vattenstämpelbilden över målbilden med `blendMode=`- och `opac=`-värdena som anges för `layer=0` eller `layer=comp` för vattenstämpelbilden. Slutligen används kommandona för att begära och visa som angetts för målbilden för att skapa svarsbilden.

Observera att vattenstämpelbilden aldrig sträcker sig över ett tomt utrymme som har lagts till i svarsbilden med kommandona `wid=` och `hei=`.

## Exempel {#section-0408c977d7324d4cb0e76a91cdfa2acd}

En vanlig vattenstämpel kan bestå av en enkel RGBA-bild som innehåller en logotyp eller ett copyrightmeddelande. Vi skapar en post i bildkatalogen (eller standardkatalogen) med `catalog::Id` inställt på `watermark` och anger vattenstämpelbildfilen i `catalog::Path`. Vi vill sträcka ut vattenstämpeln så att den passar visningsbilden (utan att vattenstämpeln förvrängs) samtidigt som vi lämnar lite extra marginal, och minska opaciteten till 20 % av den ursprungliga vattenstämpeln, så vi ställer in `catalog::Modifier` på `sizeN=0.9,0.9&opac=20`. Om du vill aktivera vattenstämplar anger du `attribute::Watermark` som id för vattenstämpelkatalogposten, &quot;watermark&quot; i det här exemplet. Vi kanske vill experimentera med olika `blendMode=`-alternativ för att få olika vattenstämplingseffekter.

## Se även {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
