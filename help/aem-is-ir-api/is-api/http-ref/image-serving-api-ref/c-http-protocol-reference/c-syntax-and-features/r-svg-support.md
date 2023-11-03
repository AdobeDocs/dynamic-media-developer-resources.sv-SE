---
description: Image Serving stöder Scalable Vector Graphics-filer (SVG) som källdata. Överensstämmelse med SVG 1.1 krävs.
solution: Experience Manager
title: Stöd för SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Stöd för SVG{#svg-support}

Image Serving stöder Scalable Vector Graphics-filer (SVG) som källdata. Överensstämmelse med SVG 1.1 krävs.

Image Serving känner bara igen statiskt SVG-innehåll. Animeringar, skript och annat interaktivt innehåll stöds inte.

SVG kan anges där bildfiler tillåts (URL-sökväg, `src=`och `mask=`). När innehållet i filen SVG har rastrerats hanteras det precis som en bild.

På samma sätt som bilder kan du ange SVG-filer som bildkatalogposter eller som relativa filsökvägar.

## Ersättningsvariabler {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` substitutionsvariabler kan inkluderas i värdesträngarna i filen SVG `<text>` element och alla elementattribut.

Viktiga variabler i frågedelen i inbäddade Image Serving-begäranden ersätts inte direkt. I stället läggs alla tillgängliga variabeldefinitioner till i begäran, vilket gör att Image Serving kan ersätta variabler när begäran analyseras.

Se [Ersättningsvariabler](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) om du vill ha mer information.

## Bildreferenser {#section-a7680f9e6aca4b1a83560637cc9fac66}

Bilder kan infogas i SVG med `<image>` -element. Bilder som refereras av `xlink::href` attributet för `<image>` -elementet måste vara en giltig begäran om bildbehandling. Externa URL:er tillåts inte.

Ange antingen en fullständig begäran om bildbehandling, med början `http://`eller en relativ URL-adress, som börjar med `/is/image`. Om en fullständig HTTP-sökväg anges tas domännamnet bort från sökvägen för konvertering till det relativa formatet. Det kan vara en fördel att använda en fullständig HTTP-sökväg eftersom den kan förhandsvisas med en SVG-renderare från tredje part.

>[!NOTE]
>
>Stödet för bildåtergivning i den här versionen av Image Serving är begränsat. Att referera bilder inifrån SVG bör endast användas i situationer där traditionella bildserverlager och mallfunktioner inte räcker till för att uppnå önskat resultat. SVG får under inga omständigheter användas för att generera sammansatta bilder i flera bilder.

>[!NOTE]
>
>Bilder som är inbäddade i SVG ändrar för närvarande inte automatiskt storlek. Kontrollera att alla bildreferenser innehåller de bildserverkommandon som behövs för att ställa in önskad bildstorlek (till exempel `wid=`). Om bildstorleken inte anges explicit `attribute::DefaultPix` används.

## Färghantering {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Alla färgvärden som är inbäddade i SVG-filer och skickas till SVG-mallar som ersättningsvariabler antas finnas i `sRgb` färgrymd.

Ingen färgkonvertering utförs när bilder bäddas in i SVG. Se till att du anger färgåtergivning `icc=sRgb` för alla inbäddade bildbegäranden.

Efter rastreringen deltar SVG-bilden i färghanteringen på samma sätt som andra bilder.

## Exempel {#section-036cdd45abd449849ee00a8f21788c28}

I följande SVG-mall visas bildreferenser och användning av variabler.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Den här SVG-mallen kan användas på följande sätt:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Begränsningar {#section-daa5eccd07204aaf993be41e87822d54}

SVG-filer måste vara fristående och får inte referera till några sekundära filer eller resurser, med undantag för externa bilder som refereras till med Image Serving- eller Image Rendering-begäranden (se ovan).

Endast statiskt innehåll återges. Animering, interaktiva funktioner som knappar och så vidare. kan finnas men kan inte återges som förväntat.

ICC-profilbaserade färgspecifikationer stöds för närvarande inte.

`<script>` kan finnas men ignoreras alltid.

## Se även {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1-specifikation](https://www.w3.org/TR/SVG11/)
