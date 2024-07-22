---
title: FXG-serverprotokoll
description: Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# FXG-serverprotokoll{#fxg-server-protocol}

Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.

Med referenspunkter kan du rotera, skala eller ändra storlek på en bild i förhållande till en viss referenspunkt. Referenspunkterna är `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` och `southeast`. Om du till exempel använder mittreferenspunkten kan du rotera en bild 45° i mitten. Följande bild visar var referenspunkterna finns, en bild, bilden roterades 20 grader från referenspunkten `northWest` och bilden roterades 20 grader från referenspunkten `east`.

![Referenspunktsbild](assets/wp_ref_points.png)

* A. Platser för referenspunkter
* B. En bild
* C. Bilden roterades 20° från referenspunkten `northWest`
* D. Grafiken roterades 20° från referenspunkten `east`

Syntaxen:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Standardvärdet är none. Värdet `inherit` skickar värdet `s7:referencePoint`, förutsatt att det inte är `none`, från sidans eller gruppnivåns överkant till alla underordnade. Inställningen `none` innebär att det inte finns någon referenspunkt för objektet och att FXG-koordinatsystemet används.

>[!NOTE]
>
>Om du vill använda en referenspunkt och inte ha någon förskjutning i objektet efter att det har manipulerats, uppdaterar du objektets x- och y-värden när du har manipulerat det.

När ett värde från `s7:referencePoint` används med grupper (eller sökvägar, linjeelement eller element som inte har explicita bredd- och höjddefinitioner), gäller värdet för den kumulativa begränsningsramen för gruppen. Den övre vänstra punkten i begränsningsramen för alla objekt i gruppen fungerar som `northWest`-referenspunkt för gruppen. Den nedre högra punkten fungerar som `southEast`-referenspunkt.
