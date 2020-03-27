---
description: Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.
seo-description: Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.
seo-title: FXG-serverprotokoll
solution: Experience Manager
title: FXG-serverprotokoll
topic: Scene7 Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# FXG-serverprotokoll{#fxg-server-protocol}

Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.

Med referenspunkter kan du rotera, skala eller ändra storlek på en bild i förhållande till en viss referenspunkt. Referenspunkterna är `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`och `southeast`. Om du till exempel använder mittreferenspunkten kan du rotera en bild 45 grader i mitten. Den här bilden visar var referenspunkterna finns, en bild, bilden roterades 20 grader från sin `northWest` referenspunkt och bilden roterades 20 grader från sin `east` referenspunkt.

![](assets/wp_ref_points.png)

* S. Referenspunktens platser
* B. En bild
* C. Bilden roterades 20 grader från sin `northWest` referenspunkt
* D. Bilden roterades 20 grader från sin `east` referenspunkt

Syntaxen är:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Standardvärdet är none. Värdet `inherit` skickar `s7:referencePoint` värdet, förutsatt att det inte gör det, `none`från sidans eller gruppnivåens överkant till alla underordnade. Inställningen `none` innebär att det inte finns någon referenspunkt för objektet och att FXG-koordinatsystemet används.

>[!NOTE]
>
>Om du vill använda en referenspunkt och inte ha någon förskjutning i objektet efter att det har manipulerats uppdaterar du objektets x- och y-värden när du har manipulerat det.

När ett värde från `s7:referencePoint` används med grupper (eller banor, linjeelement eller element som inte har explicita definitioner för bredd och höjd), gäller värdet gruppens kumulativa begränsningsram. Den övre vänstra punkten i begränsningsramen för alla objekt i gruppen fungerar som `northWest` referenspunkt för gruppen. den nedre högra punkten fungerar som `southEast` referenspunkt.

