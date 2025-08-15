---
title: Anpassa Basic Zoom Viewer
description: All visuell anpassning och de flesta beteendeanpassningar för den grundläggande zoomningsvisningsprogrammet görs genom att en anpassad CSS skapas.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9cbce980-83fd-40a7-8bcd-f9bc4dd477a8
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '1339'
ht-degree: 0%

---

# Anpassa Basic Zoom Viewer{#customizing-basic-zoom-viewer}

All visuell anpassning och de flesta beteendeanpassningar för den grundläggande zoomningsvisningsprogrammet görs genom att en anpassad CSS skapas.

Det föreslagna arbetsflödet är att ta standard-CSS-filen för rätt visningsprogram, kopiera den till en annan plats, anpassa den och ange platsen för den anpassade filen i kommandot `style=`.

CSS-standardfiler finns på följande plats:

`<s7_viewers_root>/html5/BasicZoomViewer_light.css`

Visningsprogrammet levereras med två färdiga CSS-filer, för&quot;ljust&quot; och&quot;mörkt&quot; färgschema. Den&quot;ljusa&quot; versionen används som standard, men du kan växla till den&quot;mörka&quot; versionen med följande standard-CSS:

`<s7_viewers_root>/html5/BasicZoomViewer_dark.css`

Anpassad CSS-fil måste innehålla samma klassdeklarationer som standard. Om en klassdeklaration utelämnas fungerar visningsprogrammet inte korrekt eftersom det inte innehåller inbyggda standardformat för elementen i användargränssnittet.

Ett annat sätt att tillhandahålla anpassade CSS-regler är att använda inbäddade format direkt på webbsidan eller i någon av de länkade externa CSS-reglerna.

När du skapar anpassad CSS bör du tänka på att visningsprogrammet tilldelar klassen `.s7basiczoomviewer` till dess behållar-DOM-element. Om du använder en extern CSS-fil som skickas med kommandot `style=` ska du använda klassen `.s7basiczoomviewer` som överordnad klass i den underordnade väljaren för dina CSS-regler. Om du gör inbäddade format på webbsidan kvalificerar du även den här väljaren med ett ID för behållar-DOM-elementet enligt följande:

`#<containerId>.s7basiczoomviewer`

## Bygga CSS för responsiv design {#section-0bb49aca42d242d9b01879d5ba59d33b}

Det är möjligt att rikta in sig på olika enheter och inbäddningsstorlekar i CSS så att innehållet visas på olika sätt beroende på användarens enhet eller en viss webbsideslayout. Den här målgruppen omfattar, men är inte begränsad till, olika layouter, elementstorlekar i användargränssnittet och bildupplösning.

Visningsprogrammet har stöd för två sätt att skapa responsiv designad CSS: CSS-markörer och vanliga CSS-mediefrågor. Du kan använda dessa mekanismer oberoende av varandra eller tillsammans.

**CSS-markörer**

Visningsprogrammet har stöd för CSS-markörer, vilket är till hjälp när det gäller att skapa responsiv CSS-kod. Dessa markörer är speciella CSS-klasser. De tilldelas dynamiskt till visningsprogrambehållarelementet på den översta nivån baserat på visningsprogrammets storlek vid körning och den indatatyp som används på den aktuella enheten.

Den första gruppen med CSS-markörer innehåller klasserna `.s7size_large`, `.s7size_medium` och `.s7size_small`. De tillämpas baserat på visningsbehållarens körningsområde. Om visningsområdet är lika stort eller större än storleken på en vanlig skrivbordsskärm används `.s7size_large`. Om området är nära en gemensam surfplatteenhet tilldelas `.s7size_medium`. För områden som liknar mobiltelefonskärmar är `.s7size_small` inställt. Det främsta syftet med dessa CSS-markörer är att skapa olika användargränssnittslayouter för olika skärmar och visningsstorlekar.

Den andra gruppen med CSS-markörer innehåller `.s7mouseinput` och `.s7touchinput`. Markören `.s7touchinput` anges om den aktuella enheten har funktioner för pekrörelser. Annars används `.s7mouseinput`. Dessa markörer är främst avsedda att skapa indataelement i användargränssnittet med olika skärmstorlekar för olika indatatyper, eftersom pekrörelser normalt kräver större element. Om enheten har både musindata- och pekfunktioner är `.s7touchinput` inställt och visningsprogrammet återger ett pekvänligt användargränssnitt.

Följande exempel på CSS anger storleken på inzoomningsknappen till 28 x 28 pixlar på system med musindata och till 56 x 56 pixlar på enheter med pekskärm. Dessutom döljs knappen helt om visningsprogrammets storlek blir liten:

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7basiczoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7basiczoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Om du vill använda enheter med olika pixeldensitet som mål måste du använda CSS-mediefrågor. Följande mediefrågeblock skulle innehålla CSS som är specifikt för skärmar med hög densitet:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Att använda CSS-markörer är det mest flexibla sättet att bygga CSS för responsiv design. Orsaken är att den gör att du inte bara kan ange enhetens skärmstorlek som mål, utan även den faktiska visningsstorleken, vilket är användbart för layouter med responsiv design.

Du kan använda CSS-standardfilen för visningsprogram som ett exempel på en CSS-markörmetod.

**CSS-mediefrågor**

Du kan också utföra enhetssensning med rena CSS-mediefrågor. Allt som omges av ett visst mediefrågeblock tillämpas bara när det körs på en motsvarande enhet.

När det används i mobilvisningsprogram används fyra CSS-mediefrågor, som definieras i CSS, i den ordning som anges nedan:

1. Innehåller endast regler som är specifika för alla beröringsenheter.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Innehåller endast regler som är specifika för surfplattor med högupplösta skärmar.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Innehåller endast regler som är specifika för alla mobiltelefoner.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Innehåller endast regler som är specifika för mobiltelefoner med högupplösta skärmar.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Med en mediefrågemetod bör du organisera CSS med enhetsavkänning enligt följande:

* För det första definierar det skrivbordsspecifika avsnittet alla egenskaper som är skrivbordsspecifika eller gemensamma för alla skärmar.
* För det andra följer de fyra mediefrågorna den ordning som definieras ovan och innehåller CSS-regler som är specifika för motsvarande enhetstyp.

Du behöver inte duplicera hela CSS för visningsprogram i varje mediefråga. Endast egenskaper som är specifika för vissa enheter omdefinieras i en mediefråga.

## CSS-fragment {#section-9b6d8d601cb441d08214dada7bb4eddc}

Många visningsgränssnittselement är formaterade med bitmappsbilder och har mer än ett tydligt visuellt läge. Ett bra exempel är en knapp som normalt har minst tre olika lägen: &quot;upp&quot;, &quot;över&quot; och &quot;ned&quot;. För varje läge krävs en egen bitmappsbild.

Med en klassisk metod för formatering skulle CSS ha en separat referens till enskilda bildfiler på servern för varje läge i användargränssnittselementet. Här följer ett exempel på CSS för att formatera inzoomningsknappen:

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Nackdelen med detta är att slutanvändaren får flimmer eller fördröjt svar i användargränssnittet när elementet interagerar med det för första gången. Den här åtgärden inträffar eftersom bildgrafiken för det nya elementläget inte har hämtats ännu. Den här metoden kan också ha en liten negativ inverkan på prestanda på grund av ett ökat antal HTTP-anrop till servern.

CSS-sprites är en annan metod där bilder för alla elementlägen kombineras till en enda PNG-fil som kallas&quot;sprite&quot;. En sådan&quot;sprite&quot; har alla visuella lägen för det angivna elementet placerade efter varandra. När du formaterar ett element i användargränssnittet med sprites refereras samma sprite-bild till för alla olika lägen i CSS. Dessutom används egenskapen `background-position` för varje läge för att ange vilken del av sprite-bilden som ska användas. Du kan strukturera en&quot;sprite&quot;-bild på ett lämpligt sätt. Visningsprogram har normalt en lodrät stapling. Nedan visas ett&quot;sprite&quot;-baserat exempel på hur du formaterar samma inzoomningsknapp ovan:

```
.s7basiczoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Allmän formatinformation och råd {#section-95855dccbbc444e79970f1aaa3260b7b}

* När du anpassar visningsprogrammets användargränssnitt med CSS stöds inte regeln `!IMPORTANT` för att formatera visningsprogramelement. Regeln `!IMPORTANT` ska inte användas för att åsidosätta standardformat eller körningsformat som tillhandahålls av visningsprogrammet eller visningsprogrammets SDK. Orsaken är att det kan påverka beteendet för rätt komponenter. I stället bör du använda CSS-väljare med rätt specificitet för att ange CSS-egenskaper som dokumenteras i den här referenshandboken.
* Alla sökvägar till externa resurser i CSS matchas mot CSS-platsen, inte mot visningsprogrammets HTML-sidplats. Tänk på den här regeln när du kopierar standard-CSS till en annan plats. Kopiera även standardresurserna eller uppdatera sökvägarna i den anpassade CSS-koden.
* Det format du föredrar för bitmappsbilder är PNG.
* Bitmappsgrafik tilldelas element i användargränssnittet med egenskapen `background-image`.
* Egenskaperna `width` och `height` för ett användargränssnittselement definierar dess logiska storlek. Storleken på bitmappen som skickas till `background-image` påverkar inte den logiska storleken.
* Om du vill använda hög pixeldensitet för högupplösta skärmar som Retina anger du bitmappsbilder som är dubbelt så stora som elementstorleken för det logiska användargränssnittet. Använd sedan egenskapen `-webkit-background-size:contain` för att skala ned bakgrunden till elementstorleken för det logiska användargränssnittet.
* Om du vill ta bort en knapp från användargränssnittet lägger du till `display:none` i CSS-klassen.
* Du kan använda olika format för färgvärden som stöds i CSS. Använd formatet `rgba(R,G,B,A)` om du behöver genomskinlighet. Annars kan du använda formatet `#RRGGBB`.

## Element i gemensamt användargränssnitt {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Nedan följer referensdokumentation för användargränssnittselement som gäller för Basic Zoom Viewer:
