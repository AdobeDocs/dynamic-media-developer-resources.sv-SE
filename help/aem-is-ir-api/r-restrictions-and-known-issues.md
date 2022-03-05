---
description: Det finns vissa begränsningar och kända fel som bör beaktas när du använder Dynamic Media Image Serving.
solution: Experience Manager
title: Begränsningar och kända fel
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1229'
ht-degree: 0%

---

# Begränsningar och kända fel{#restrictions-and-known-issues}

Det finns vissa begränsningar och kända fel som bör beaktas när du använder Dynamic Media Image Serving.

## Dokumentationsfel {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Antalet rader kommer inte att överskrida maxvärdet för `\copyfitmaxlines` inställning och antalet explicita rader i textinmatningen.
* Matchande klammerparenteser och parenteser krävs i bilduppsättningar. Om klammerparenteser och parenteser inte matchar varandra måste de vara URL-kodade.
* Varningen för global svarstid på serversidan innehåller felsvar.
* The `id=` -kommandot är för närvarande obligatoriskt när du använder `rect=` med en bild- eller maskbegäran.

## Kända skillnader textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Syntetisk kursiv renderas mindre lutande än när du använder `text=`.
* Understrykning är lite lägre och tunnare än när du använder `text=`.
* `\expnd` och `\expndtw` om du använder höga negativa värden placeras tecken framför varandra när du använder `text=`.

* `\charscaley` skalförändras annorlunda än när du använder `text=` men påverkar inte radhöjden.

* Om den sista textraden inte får plats tas hela raden bort i stället för att visas som utfall.
* `\slmult` och `\sl` fungerar annorlunda än MS Word och `text=`används de bara för de aktuella och efterföljande styckena.

* `\sb` gäller för det första stycket för både MS Word och `text=`, Adobe InDesign och Photoshop gör inte detta.

* `\sa` gäller för det sista stycket för både MS Word och `text=`, Adobe InDesign och Photoshop gör inte detta.

## Bakåtkompatibilitet {#section-a76842f751944f4fb664af296d064122}

* Escaping the underscore character ( `\_`) i en RTF-sträng fungerar inte med alla teckensnitt som använder `textPs=`

* Stöder inte skiftlägeskänslig makrohantering.
* Katalogcachen har reducerats från 60 sekunder till 10 sekunder.
* Omdirigeringsfunktionen för fel dirigerar nu bara om begäranden om skadade bilder, teckensnitt, färgprofiler och bilder som publiceras i en katalog, men inte finns på disken.
* `posN=`, `anchor=`, `anchorN=`, `origin=`och `originN=` returnerar nu ett tolkningsfel om något av modifieringsvärdena är större än 2147483648.

* Kodning av kapslade begäranden stöds inte. Övergång till det nya beteendet och avkoda eventuella kapslade begärandavärden som hittas i URL-begäranden på din webbplats och i företagets kataloger.
* DefaultImage använder nu miniatyrattribut när du använder `req=tmb`.
* I tidigare versioner med `flip=`placerades bilden aldrig om oavsett vad ankarpunkten var.

## Begränsningar för bibliotek från tredje part {#section-79768b96bf634e44ab672c5b893f343d}

Digimarc-biblioteket vägrar att använda en Digimarc-vattenstämpel på en bild om en sådan redan upptäcks. Om en primär bild redigeras tillräckligt mycket kan Digimarc-biblioteket fortfarande känna igen att vattenstämpeln har använts. Det kanske inte går att läsa den informationen. Detta resulterar i en ny bild där den ursprungliga Digimarc-informationen som tillämpades på originalbilden inte kan hämtas. Image Serving kan nu använda den Digimarc-vattenstämpel som definierats i företagskatalogen.

## Begränsningar som gäller både för bildvisning och bildåtergivning {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Bildredigering och bildåtergivning kanske inte utnyttjar alla processorer fullt ut när det finns fler än 4 processorer. Simulera trafiken på dessa datorer för att se hur fördelaktig den är med fler än 4 processorer.
* Fjärr-URL:er som returnerar en omdirigering (HTTP-status 301, 302 eller 303) nekas.
* Vid konfigurering `errorRedirect.rootUrl` IP-adressen som definieras i den här egenskapen måste inkluderas i regeluppsättningen `<addressfilter>` på den servern.

   *Exempel*:

   Server A har definierats `errorRedirect.rootUrl=10.10.10.10` .

   Server B, som har IP-adressen 10.10.10.10, anger `<addressfilter>` i regeluppsättningsfilen så att den innehåller IP-adressen (10.10.10.10).

* Punkttext och textbana med positionering kan visa urklipp.
* `text=` gäller endast `\sa` och `\sb` till hela textblocket och inte per stycke.

* När du använder ett företag som definierats i URL:en och ett annat företag som definierats för `src=` eller `mask=` modifierare, du måste prefix a forward slash to the company defined for `src=` eller `mask=` för den här typen av begäran.

   *Exempel*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   I stället för: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Tiff- eller vinjettbegäranden som inte är Pyramided skapar ett liknande felmeddelande som

   *&quot;Bild `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` har ingen giltig DSF, och området 2,25MPixel överskrider maxvärdet för 2MPixel&quot;* .

   Bästa sättet är att använda pyramiderade slipsar och vinjetteringar. Om du behöver använda icke-pyramidade vinjetter eller vinjetter följer du instruktionerna nedan för att öka storleksgränsen.

   *Arbeta runt*:

   För bildåtergivning av icke-pyramidade vinjetter ökar du egenskapsvärdet för IrMaxNonPyrVignetteSize i dialogrutan [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] konfigurationsfil.

   Öka egenskapsvärdet för Bildservning av icke-pyramidat TIFF för `MaxNonDsfSize` i [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] konfigurationsfil.

* Adobe Photoshop CS3 sparar inte PSD-filer med lager som standard som en sammansatt bild.

   *Symtom*:

   Adobe Photoshop CS3-filen PSD i lager visas som svart med texten &quot;Denna Photoshop-fil i lager har inte sparats med en sammansatt bild&quot;. för svarsbilden Image Serving eller i IPS.

   *Tillfällig lösning*:

   Spara Adobe Photoshop CS3-filen med maximal kompatibilitet aktiverat.

* Om du tilldelar en ICC-profil till en CMYK/JPEG-svarsbild blir färgerna inverterade i vissa webbläsare.*Arbeta runt*:

   Ändra svarsbildens format med `fmt=`

* Storleken på HTTP-svarsbildens data-after-komprimering, inklusive filhuvudet, är begränsad till 16 MB.
* &quot; ..&quot; tillåts inte i något sökvägselement i HTTP-begäranden.
* Avinstallationen kan ta bort en fil som skapats eller ändrats av användaren från *[!DNL install_root]* eller en undermapp. Kopiera sådana filer till en annan plats innan du avinstallerar.

## Begränsningar som endast gäller för bildvisning {#section-b08ad535e4454265b8157dec244c4faf}

* Förgrundsfärger i RTF ( `\cf`) stöds inte för PhotoFont-text.
* Syntetisering av fet, kursiv och fet/kursiv nekas som ett fel för PhotoFont-text.
* Lodrätt textflöde stöds inte för PhotoFont-text.
* PNG-bilder med 16 bitar per kanal stöds inte för PhotoFont-text.
* Färgkorrigeringar för PNG-bilder med inbäddade färgprofiler använder hårdkodade alternativ. Återgivningsmetoden är relativ kolorimetrisk och svartpunktskompensation är aktiverat för PhotoFont-text.
* Filbaserad sökning stöds inte när språköversättning är aktiverat i företaget [!DNL ini] -fil.
* Image Serving skriver inte oavslutade Photoshop-sökvägar korrekt.
* Image Serving stöder för närvarande inte bearbetning av TIFF-filer som exporterats med Adobe Media Encoder 4.0.1 eller tidigare. Adobe Media Encoder ingår i Premiere Pro CS4, After Effects CS4 och Creative Suite 4 Production Premium.
* Använda `text=` med självskalande lager stöder inte RTF-strängar som använder mer än en inställning för linjejustering.

   *Exempel*

   RTF-strängen kan inte använda både vänster och höger radjustering för ett textlager som ändrar storlek automatiskt.

* SVG har en egen egenskap för teckensnittssökvägen för refererade teckensnitt som inte är inbäddade i SVG-filen.

   *Symtom*

   Återgivna SVG-bilder som innehåller teckensnittsdefinitioner använder fel teckensnitt.

   *Tillfällig lösning*

   Ange egenskapen `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Beskärning använder för närvarande `bgColor=` i stället för `color=` för att fylla i nya utökade områden.

* Färgkonverteringen är kanske inte korrekt när `bgColor=` matchar inte basfärgrymden som innehåller färgprofiler.
* Yttre lagereffekter återges inte om lagret inte har någon mask- eller alfakata.

## Begränsningar som endast gäller för bildåtergivning {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Dekaler och väggmaterial kan inte avlägsnas.
* Storleken på texturer är begränsad i förhållande till vinjetteringsvyns storlek. I sällsynta fall kan standardgränsen på 425 % av visningsstorleken störa ett program som använder mycket stora icke-repeterbara texturer. Om det inte går att ändra programmet eller innehållet så att det fungerar inom de fördefinierade begränsningarna kan procentandelen ökas enligt följande. Öppna med en textredigerare [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], söka `IrMaxTextureSizeFactor` och ange ett nytt procentvärde. Ändringen börjar gälla omedelbart utan att du behöver starta om Image Server.

* JavaScript-motorer i Netscape och Opera cache-svarsdata även om nocache-huvudet är inställt. Detta stör en korrekt funktion för tillståndskänsliga begäranden.

   *Tillfällig lösning*

   Lägg till en tidsstämpel eller annan unik identifierare i begärandesträngen, till exempel `"&.ts=currentTime`.

## Begränsningar som endast gäller för allmännyttiga tjänster {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`ibland kraschar med ett segmenteringsfel när det stoppas med en `control-c`.
