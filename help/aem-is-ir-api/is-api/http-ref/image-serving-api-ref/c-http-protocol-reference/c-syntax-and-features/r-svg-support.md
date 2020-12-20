---
description: Image Serving stöder SVG-filer (Scalable Vector Graphics) som källdata. Överensstämmelse med SVG 1.1 krävs.
seo-description: Image Serving stöder SVG-filer (Scalable Vector Graphics) som källdata. Överensstämmelse med SVG 1.1 krävs.
seo-title: SVG-stöd
solution: Experience Manager
title: SVG-stöd
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# SVG-stöd{#svg-support}

Image Serving stöder SVG-filer (Scalable Vector Graphics) som källdata. Överensstämmelse med SVG 1.1 krävs.

Image Serving känner bara igen statiskt SVG-innehåll; animeringar, skript och annat interaktivt innehåll stöds inte.

SVG kan anges där bildfiler tillåts (URL-sökväg, `src=` och `mask=`). När innehållet i SVG-filen har rastrerats hanteras det precis som en bild.

På samma sätt som bilder kan SVG-filer anges som bildkatalogposter eller som relativa filsökvägar.

## Ersättningsvariabler {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` substitutionsvariabler kan inkluderas i SVG-filen i  `<text>` värdesträngselementen och i alla elementattribut.

Viktiga variabler i frågedelen i inbäddade Image Serving-begäranden ersätts inte direkt. I stället läggs alla tillgängliga variabeldefinitioner till i begäran, vilket gör att Image Serving kan ersätta variabler när begäran analyseras.

Mer information finns i [Ersättningsvariabler](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a).

## Bildreferenser {#section-a7680f9e6aca4b1a83560637cc9fac66}

Bilder kan infogas i SVG med elementet `<image>`. Bilder som `xlink::href`-attributet för `<image>`-elementet refererar till måste vara giltiga avbildningsbegäranden som skickas. Externa URL:er tillåts inte.

Ange antingen en fullständig Image Serving-begäran, som börjar med `http://`, eller en relativ URL, som börjar med `/is/image`. Om en fullständig HTTP-sökväg anges tas domännamnet bort från sökvägen och konverteras till det relativa formatet. Det kan vara en fördel att använda en fullständig HTTP-sökväg eftersom den kan förhandsgranskas med en SVG-renderare från en annan tillverkare.

>[!NOTE]
>
>Stödet för bildåtergivning i den här versionen av Image Serving är begränsat. Referenser till bilder från SVG bör endast användas i situationer där traditionella bildserverlager och mallfunktioner inte räcker till för att uppnå det önskade resultatet. SVG får under inga omständigheter användas för att generera sammansatta bilder i flera bilder.

>[!NOTE]
>
>Bilder som är inbäddade i SVG ändrar för närvarande inte automatiskt storlek. Kontrollera att alla bildreferenser innehåller de bildserverskommandon som behövs för att ställa in önskad bildstorlek (t.ex. `wid=`). Om bildstorleken inte anges uttryckligen används `attribute::DefaultPix`.

## Färghantering {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Alla färgvärden som är inbäddade i SVG-filer och skickas till SVG-mallar via ersättningsvariabler antas finnas i färgmodellen `sRgb`.

Ingen färgkonvertering utförs när bilder bäddas in i SVG-filen. För att säkerställa färgåtergivning måste du ange `icc=sRgb` för alla inbäddade bildbegäranden.

Efter rastreringen deltar SVG-bilden i färghanteringen på samma sätt som andra bilder.

## Exempel {#section-036cdd45abd449849ee00a8f21788c28}

Följande SVG-mall visar bildreferenser och användning av variabler.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Den här SVG-mallen kan användas på följande sätt:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Begränsningar {#section-daa5eccd07204aaf993be41e87822d54}

SVG-filer måste vara fristående och får inte referera till några sekundära filer eller resurser, med undantag för externa bilder som refereras till i Image Serving- eller Image Rendering-begäranden (se ovan).

Endast statiskt innehåll återges. Animering, interaktiva funktioner som knappar osv. kan finnas men kan inte återges som förväntat.

ICC-profilbaserade färgspecifikationer stöds för närvarande inte.

`<script>` kan finnas men ignoreras alltid.

## Se även {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [SVG 1.1-specifikation](http://www.w3.org/TR/SVG11/)
