---
title: FXG-serverprotokoll
description: Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# FXG-serverprotokoll{#fxg-server-protocol}

Om du vill ändra en bild kan du använda referenspunkter som liknar kompaspunkter.

Med referenspunkter kan du rotera, skala eller ändra storlek på en bild i förhållande till en viss referenspunkt. Referenspunkterna är `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`och `southeast`. Om du till exempel använder mittreferenspunkten kan du rotera en bild 45° i mitten. I följande bild visas var referenspunkterna finns, en bild, bilden roterad 20° från sin `northWest` referenspunkt och bilden har roterats 20° från sin `east` referenspunkt.

![Referenspunktsbild](assets/wp_ref_points.png)

* S. Referenspunktens platser
* B. En bild
* C. Bilden roterades 20° från sin `northWest` referenspunkt
* D. Bilden roterades 20° från sin `east` referenspunkt

Syntaxen är:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Standardvärdet är none. The `inherit` värdet skickar `s7:referencePoint` värde, förutsatt att det inte `none`, från överkanten av sidan eller gruppnivån till alla underordnade. The `none` -inställning betyder att det inte finns någon referenspunkt för objektet och att FXG-koordinatsystemet används.

>[!NOTE]
>
>Om du vill använda en referenspunkt och inte ha någon förskjutning i objektet efter att det har manipulerats uppdaterar du objektets x- och y-värden när du har manipulerat det.

När ett värde från `s7:referencePoint` används med grupper (eller banor, linjeelement eller element som inte har någon explicit definition av bredd och höjd), används värdet för den kumulativa begränsningsramen för gruppen. Den övre vänstra punkten i begränsningsramen för alla objekt i gruppen fungerar som den `northWest` gruppens referenspunkt, den nedre högra punkten fungerar som `southEast` referenspunkt.
