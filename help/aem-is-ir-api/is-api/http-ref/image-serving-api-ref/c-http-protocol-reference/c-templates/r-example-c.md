---
description: Skapa ett"pappersprogram".
seo-description: Skapa ett"pappersprogram".
seo-title: Exempel C
solution: Experience Manager
title: Exempel C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Exempel C{#example-c}

Skapa ett&quot;pappersprogram&quot;.

En bakgrundsbild innehåller fotot av en modell eller mannequin. Ytterligare poster i bildkatalogen innehåller olika kläder och tillbehör, som fotograferats för att passa skyltdockan i form och storlek.

Alla kläder-/tillbehörsfoton maskeras och beskärs till markeringsramen för masken för att minimera bildstorlekarna. Fästpunkter och upplösningar styrs noga för att bibehålla justeringen mellan lagren och bakgrundsbilden, och alla bilder läggs till i en bildkatalog med rätt värden lagrade i `catalog::Resolution` och `catalog::Anchor`.

Förutom lagerhantering vill vi också ändra färgen för markerade objekt. Posterna för dessa objekt förbearbetas för att ta bort den ursprungliga färgen och justera intensiteten och kontrasten på ett sätt som passar kommandot för färgläggning. Den här förbearbetningen kan göras offline med ett bildredigeringsverktyg som Photoshop, eller så kan den göras trivialt genom att lägga till `op_brightness=` och `op_contrast=` till `catalog::Modifier`fältet.

Det här programmet kräver ingen separat mall eftersom alla objekt redan är korrekt justerade med sina bildsankarpunkter ( `catalog::Anchor`) och skalade ( `catalog::Resolution`). Vi överlåter det till kunden för att säkerställa lämplig lagerordning.

En vanlig begäran kan se ut så här:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Endast höjden anges. Detta gör att den returnerade bilden kan variera i bredd beroende på mannequin-bildens proportioner, utan att marginalerna fylls med bakgrundsfärgen.

Det spelar ingen roll vilken upplösning som anges för varje lager, så länge de är desamma. Den här versionen kanske inte tillåter vyer att vara större än de sammansatta bilderna. Om du anger ett stort upplösningsvärde undviker du problem som beror på den här begränsningen. All bearbetning och sammansättning sker med den optimala upplösningen för den begärda bildstorleken, för att uppnå bästa prestanda och utdatakvalitet.

Kommandona `res=` kan utelämnas om alla källbilder har samma upplösning i full skala (vilket troligen är fallet för den här typen av program).

Du måste ange `rootId` värdet för alla `src=` kommandon, även om de är samma som det `rootId` som anges i URL-sökvägen.

Om ingen bildkatalog ska användas går det inte att använda en upplösningsbaserad skalningsmetod. I det här fallet måste explicita skalfaktorer beräknas för varje lagerobjekt, baserat på förhållandet mellan `catalog::Resolution` värdena för varje lager och `catalog::Resolution` värdet för bakgrundslagret. Sammansättningsbegäran (med färre lager) kan därför se ut så här:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

