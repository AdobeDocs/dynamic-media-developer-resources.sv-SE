---
description: Image Serving implementerar en enkel funktion för visuell vattenstämpel.
solution: Experience Manager
title: Vattenstämplar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Vattenstämplar{#watermarks}

Image Serving implementerar en enkel funktion för visuell vattenstämpel.

En vattenstämpel är vanligtvis en halvgenomskinlig bild, men det kan vara text eller en mer komplex sammansatt bild i flera lager. Servern lagrar vattenstämpeln över svarsbilden efter alla visningsattribut ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) har tillämpats.

Vattenstämplar aktiveras genom inställning `attribute::Watermark` till en giltig katalogpost som skulle innehålla vattenstämpelbilden eller mallen. If `attribute::Watermark` anges i en namngiven katalog lägger servern till vattenstämpeln i alla bildbegäranden som refererar till katalog-ID:t i URL:en för begäran. If `default::Watermark` är inställt (i standardkatalogen, [!DNL default.ini]) används vattenstämpeln på alla bildbegäranden oavsett om de refererar till en katalog eller inte.

Vattenstämplar används inte på bilder som returneras som svar på miniatyrbildsförfrågningar ( `req=tmb`) och vissa önskemål från Dynamic Media.

## Skalning och justering {#section-89ef9e5926ae438abbd8e70332749b76}

När en vattenstämpel anges genererar servern först den sammansatta bilden (den *målbild*) som vattenstämpeln ska användas på (innan vyomformningarna tillämpas). Servern genererar sedan den sammansatta bilden för vattenstämpeln precis som andra bilder (den *vattenstämpelbild*).

Till skillnad från standardbilder `sizeN=` kan anges för layer=0 eller layer=comp för vattenstämpelbilden. Det gör att vattenstämpelbilden kan skalas i förhållande till målbilden. If `sizeN=` om inget anges behåller vattenstämpelbilden sin pixelstorlek när den sammanfogas med målbilden.

Begär kommandon (t.ex. `fmt=`) och visa kommandon (som `wid=`) ignoreras i vattenstämpelposter, med undantag för `align=`. `align=` kan användas för att placera vattenstämpelbilden i förhållande till vattenstämpelbilden i förhållande till målbilden. Det gör att vattenstämpeln kan placeras i förhållande till ett hörn eller en kant på målbilden.

Efter skalning och justering lagrar servern vattenstämpelbilden över målbilden med `blendMode=` och `opac=` värden som anges för `layer=0` eller `layer=comp` av vattenstämpelbilden. Slutligen används kommandona för att begära och visa som angetts för målbilden för att skapa svarsbilden.

Observera att vattenstämpelbilden aldrig sträcker sig över ett tomt utrymme som läggs till i svarsbilden av `wid=` och `hei=` kommandon.

## Exempel {#section-0408c977d7324d4cb0e76a91cdfa2acd}

En vanlig vattenstämpel kan bestå av en enkel RGBA-bild som innehåller en logotyp eller ett copyrightmeddelande. Vi skapar en post i bildkatalogen (eller standardkatalogen) med `catalog::Id` ange till `watermark` och ange vattenstämpelbildfilen i `catalog::Path`. Vi vill tänja ut vattenstämpeln så att den passar in i visningsbilden (utan att vattenstämpeln förvrängs) samtidigt som vi lämnar lite extra marginal och minskar opaciteten till 20 % av den ursprungliga vattenstämpeln, så vi ställer in `catalog::Modifier` till `sizeN=0.9,0.9&opac=20`. Aktivera vattenstämpel genom att ange `attribute::Watermark` &quot;watermark&quot; i det här exemplet på vattenstämpelkatalogens ID. Vi kanske vill experimentera med olika `blendMode=` för olika vattenstämplingseffekter.

## Se även {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
