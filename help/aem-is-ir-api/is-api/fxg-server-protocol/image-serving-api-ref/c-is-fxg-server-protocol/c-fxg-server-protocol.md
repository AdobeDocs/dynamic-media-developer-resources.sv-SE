---
description: Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.
solution: Experience Manager
title: FXG-serverprotokoll
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# FXG-serverprotokoll{#fxg-server-protocol}

Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.

Med referenspunkter kan du rotera, skala eller ändra storlek på en bild i förhållande till en viss referenspunkt. Referenspunkterna är `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` och `southeast`. Om du till exempel använder mittreferenspunkten kan du rotera en bild 45 grader i mitten. Den här bilden visar var referenspunkterna finns, en bild, bilden roterades 20 grader från referenspunkten `northWest` och bilden roterades 20 grader från referenspunkten `east`.

![](assets/wp_ref_points.png)

* S. Referenspunktens platser
* B. En bild
* C. Bilden roterades 20 grader från referenspunkten `northWest`
* D. Bilden roterades 20 grader från referenspunkten `east`

Syntaxen är:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Standardvärdet är none. Värdet `inherit` skickar `s7:referencePoint`-värdet, förutsatt att det inte är `none`, från sidans eller gruppnivåns överkant till alla underordnade. Inställningen `none` betyder att det inte finns någon referenspunkt för objektet och att FXG-koordinatsystemet används.

>[!NOTE]
>
>Om du vill använda en referenspunkt och inte ha någon förskjutning i objektet efter att det har manipulerats uppdaterar du objektets x- och y-värden när du har manipulerat det.

När ett värde från `s7:referencePoint` används med grupper (eller banor, linjeelement eller element som inte har explicita definitioner för bredd och höjd), gäller värdet gruppens kumulativa begränsningsram. Den övre vänstra punkten i begränsningsramen för alla objekt i gruppen fungerar som referenspunkt `northWest` för gruppen. den nedre högra punkten fungerar som referenspunkt för `southEast`.

