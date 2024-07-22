---
title: Vinjetter
description: Vinjetter är bilder som har skapats med Dynamic Media Image Authoring och som kan användas med Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Vinjetter{#vignettes}

Vinjetter är bilder som har skapats med Dynamic Media Image Authoring och som kan användas med Image Rendering.

IR har stöd för två grundläggande typer av vinjetter: *2D* och *3D*. Rumsscener är vanligtvis 3D-vinjetteringar som kan återge reflektioner, medan de flesta andra scener, som kläder eller möbelklädsel, vanligtvis är 2D-vinjetteringar som inte kan återge reflektionen.

Vinjetter innehåller en *vy* och en hierarki med *objekt*.

Vyn är behållaren för huvudbilden, delade belysningskartor, delade reflektionskartor och andra data som är kopplade till hela bilden.

Objekthierarkin består av *objektgrupper*, *standardobjekt* och *överlappande objekt*.

Varje standardobjekt styr ett område i visningsbilden, definierat med en gråskalemask på *mask*. Standardobjektens masker överlappar aldrig. Standardobjekt kan inte döljas direkt, men de kan täckas helt eller delvis av överlappande objekt. De flesta eller alla objekt i en typisk vinjettering är standardobjekt.

Överlappa objektlager ovanpå visningsbilden och varandra. Överlappningens ordning definieras av ett z-värde som tilldelats objektet. Överlappande objekt är användbara när delar av en scen måste visas eller döljas dynamiskt.

Flera typer av objekt stöds (både standard och överlappning), med olika syften:

* **Plana objekt** (i 3D-vinjetteringar) och **platta objekt** (i 2D-vinjetteringar) accepterar repeterbara texturmaterial. De används vanligtvis för golv, motdatorer och andra platta ytor som bara kräver perspektivmappning.
* **Flödeslinjeobjekt** mappar mjukt formade böjda ytor som möbelklädsel och används ibland även för kläder. De kan användas i både 2D- och 3D-vinjetteringar och, om de är helt redigerade, deltar i reflektionsåtergivning.
* **Objekt som inte kan struktureras** tillåter bara färgändringar. De är tillåtna i både 2D- och 3D-vinjetter. De är antingen i sig icke-texturerbara eller kan vara ett planar- eller flödesobjekt med en särskild flagguppsättning &quot;Ingen textur&quot;. Den här metoden är användbar i 3D-vinjetteringar så att objekt kan delta i reflektionsåtergivning, även om objektet bara accepterar heltäckande färgmaterial.
* **Skissobjekt** används bäst för typobjekt med vikningar och veck, till exempel kläder. Precis som flödeslinjeobjekt kan de användas i 2D- och 3D-vinjetteringar, även om användningen i 3D-vinjetteringar är begränsad.
* **Väggobjekt** liknar planära objekt och stöds bara i 3D-vinjetter. De har särskild layoutinformation som medger användning av två olika väggslut (övre och nedre) och upp till tre material för väggkanter. När materialet används på väggar på rätt sätt flyter det korrekt och smidigt mellan närliggande väggar, vilket ger realistiska kanter för tapeter/väggar. Väggobjekt stöder inte texturrotation.
* **Kabinettobjekt** tillåts endast i 3D-vinjetter. De används för att skapa köks- och badskåp med komplexa layoutkrav. Kabinettobjekt accepterar repeterbara texturer och särskilt skapade *kabinettformatfiler* som innehåller bilder för skåppanelen som kan storleksändras.

Förutom de grundläggande objekttyperna stöds två särskilda typer av överlappningsobjekt:

* **Statiska överlappningsobjekt** är objekt som inte kan hantera material. De är tillåtna i både 2D- och 3D-vinjetter. De är användbara för borttagbara tillbehör i rumsscener, för skuggor bakom återgivningsbara överlappningsobjekt och liknande program.
* **Fönster som omfattar ramobjekt** innehåller placeringsinformation för att tillämpa formatfiler för fönsteromslag, som har skapats oberoende av vinjetteringen och kan delas mellan vinjetter.

Objekt samlas in i *objektgrupper*, ungefär som ett filsystem. Grupperingen baseras vanligtvis på strukturen för de fysiska objekt som de representerar (t.ex. kan gruppen Alla skåp innehålla Baskåp och Väggskåp). Ett valfritt antal gruppnivåer tillåts. Gruppering stöder användning av material på flera liknande objekt.

* [Scenkoordinater](c-ir-scene-coordinates.md)
* [Materialupplösning](c-ir-material-resolution.md)
