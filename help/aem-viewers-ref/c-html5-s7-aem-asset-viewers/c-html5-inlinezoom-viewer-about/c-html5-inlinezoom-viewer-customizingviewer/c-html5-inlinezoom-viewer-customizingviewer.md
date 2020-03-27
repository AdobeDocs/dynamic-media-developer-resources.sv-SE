---
description: 'null'
keywords: responsive
seo-description: 'null'
seo-title: Anpassa visningsprogrammet för intern zoomning
solution: Experience Manager
title: Anpassa visningsprogrammet för intern zoomning
topic: Dynamic media
uuid: c9203ea7-47dc-40f6-add8-04e4258da7c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Anpassa visningsprogrammet för intern zoomning{#customizing-inline-zoom-viewer}

All visuell anpassning och de flesta beteendeanpassningar görs genom att en anpassad CSS skapas.

Det föreslagna arbetsflödet är att ta standard-CSS-filen för rätt visningsprogram, kopiera den till en annan plats, anpassa den och ange platsen för den anpassade filen i `style=` kommandot.

CSS-standardfiler finns på följande plats:

`<s7_viewers_root>/html5/InlineZoomViewer.css`

Anpassad CSS-fil måste innehålla samma klassdeklarationer som standardklassdeklarationerna. Om en klassdeklaration utelämnas fungerar visningsprogrammet inte korrekt eftersom det inte innehåller inbyggda standardformat för elementen i användargränssnittet.

Det är också viktigt att bevara följande CSS-deklaration från CSS för standardvisningsprogrammet, eftersom den behövs för inline-zoomningsfunktioner:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 width: 100%; 
 height: 100%; 
 left: 0; 
 top: 0; 
 border: none; 
 z-index:999; 
}
```

Ett annat sätt att tillhandahålla anpassade CSS-regler är att använda inbäddade format direkt på webbsidan eller i någon av de länkade externa CSS-reglerna.

När du skapar anpassad CSS bör du tänka på att visningsprogrammet tilldelar `.s7flyoutviewer` klassen till dess behållar-DOM-element. Om du använder en extern CSS-fil som skickas med `style=` kommandot använder du `.s7flyoutviewer` klassen som överordnad klass i den underordnade väljaren för dina CSS-regler. Om du gör inbäddade format på webbsidan kan du även kvalificera den här väljaren med ett ID för behållar-DOM-elementet enligt följande:

`#<containerId>.s7flyoutviewer`

## Skapa responsiv CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Det är möjligt att rikta in sig på olika enheter och inbäddningsstorlekar i CSS så att innehållet visas på olika sätt, beroende på användarens enhet eller en viss webbsideslayout. Detta omfattar, men är inte begränsat till, olika webbsideslayouter, elementstorlekar i användargränssnittet och bildupplösning.

Visningsprogrammet har stöd för två metoder för att skapa responsiv CSS: CSS-markörer och vanliga CSS-mediefrågor. Du kan använda dessa metoder oberoende av varandra eller tillsammans.

**CSS-markörer**

För att det ska vara lättare att skapa responsiv designad CSS har visningsprogrammet stöd för CSS-markörer som har särskilda CSS-klasser som dynamiskt tilldelas till visningsprogrambehållarelementet på den översta nivån baserat på visningsprogrammets storlek vid körning och den indatatyp som används på den aktuella enheten.

Den första gruppen med CSS-markörer innehåller `.s7size_large`, `.s7size_medium`och `.s7size_small` klasser. De tillämpas baserat på visningsprogrambehållarens körningsområde. Det vill säga om visningsområdet är lika med eller större än storleken på en vanlig skrivbordsskärm `.s7size_large` används. om området är nästan lika stort som en vanlig surfplatta `.s7size_medium` tilldelas. För områden som liknar mobiltelefonskärmar `.s7size_small` anges. Det främsta syftet med dessa CSS-markörer är att skapa olika användargränssnittslayouter för olika skärmar och visningsstorlekar.

Den andra gruppen med CSS-markörer innehåller `.s7mouseinput` och `.s7touchinput`. `.s7touchinput` är inställt om den aktuella enheten har funktioner för pekrörelser, i annat fall `.s7mouseinput` används. Dessa markörer är avsedda att skapa indataelement i användargränssnittet med olika skärmstorlekar för olika indatatyper, eftersom större element normalt krävs för pekrörelser. Om enheten har både musindata- och pekfunktioner ställs `.s7touchinput` in och visningsprogrammet återger ett pekvänligt användargränssnitt.

Följande exempel på CSS anger storleken på inzoomningsknappen till 28 x 28 pixlar på system med musindata och 56 x 56 pixlar på enheter med pekskärm. Dessutom döljs knappen helt om visningsprogrammets storlek blir riktigt liten:

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

Om du vill använda enheter med en annan pixeldensitet som mål använder du CSS-mediefrågor. Följande mediefrågeblock skulle innehålla CSS som är specifikt för skärmar med hög densitet:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Att använda CSS-markörer är det mest flexibla sättet att skapa responsiv CSS som gör att du inte bara kan rikta in dig på enhetens skärmstorlek utan även på den faktiska visningsstorleken, vilket kan vara användbart för responsiva designade webbsideslayouter.

**CSS-mediefrågor**

Enhetsavkänning kan även göras med rena CSS-mediefrågor. Allt som omges av ett visst mediefrågeblock tillämpas bara när det körs på en motsvarande enhet.

Använd fyra CSS-mediefrågor som definieras i CSS i följande ordning när de används i mobilvisningsprogram:

1. Innehåller endast regler som är specifika för alla beröringsenheter.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

## CSS-fragment {#section-b0af39db1af74561aea9fddcc8cdc2c7}

Många visningsgränssnittselement är formaterade med bitmappsbilder och har mer än ett tydligt visuellt läge. Ett bra exempel är en knapp som normalt har minst tre olika lägen: &quot;up&quot;, &quot;over&quot; och &quot;down&quot;. För varje läge krävs en egen bitmappsbild.

Med en klassisk metod för formatering skulle CSS ha en separat referens till enskilda bildfiler på servern för varje läge i användargränssnittselementet. Här följer ett exempel på CSS för att formatera en rullningsknapp:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

Nackdelen med detta är att slutanvändaren får flimmer eller fördröjt svar i användargränssnittet när elementet interagerar med det för första gången. Den här åtgärden inträffar eftersom bildgrafiken för det nya elementläget inte har hämtats ännu. Den här metoden kan också ha en liten negativ inverkan på prestanda på grund av ett ökat antal HTTP-anrop till servern.

CSS-sprites är en annan metod där bilder för alla elementlägen kombineras till en enda PNG-fil som kallas&quot;sprite&quot;. En sådan&quot;sprite&quot; har alla visuella lägen för det angivna elementet placerade efter varandra. När du formaterar ett element i användargränssnittet med fragment refereras samma sprite-bild till för alla olika lägen i CSS. Dessutom används egenskapen för varje läge för att ange vilken del av&quot;sprite&quot;-bilden som ska användas `background-position` . Du kan strukturera en&quot;sprite&quot;-bild på ett lämpligt sätt. Visningsprogram har normalt en lodrät stapling. Nedan visas ett&quot;sprite&quot;-baserat exempel på hur du formaterar samma rullningsknapp ovan:

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## Allmän formatinformation och råd {#section-95855dccbbc444e79970f1aaa3260b7b}

* När du anpassar visningsprogrammets användargränssnitt med CSS stöds inte användningen av `!IMPORTANT` regeln för att formatera visningsprogramelement. Regeln ska framför allt inte användas för att åsidosätta standardformat eller körningsformat som tillhandahålls av visningsprogrammet eller visaren-SDK. `!IMPORTANT` Orsaken är att det kan påverka beteendet för rätt komponenter. I stället bör du använda CSS-väljare med rätt specificitet för att ange CSS-egenskaper som dokumenteras i den här referenshandboken.
* Alla sökvägar till externa resurser i CSS matchas mot CSS-platsen, inte mot visningsprogrammets HTML-sidplats. Tänk på den här regeln när du kopierar standard-CSS till en annan plats. Kopiera även standardresurserna eller uppdatera sökvägarna i den anpassade CSS-koden.
* Det format du föredrar för bitmappsbilder är PNG.
* Bitmappsgrafik tilldelas till element i användargränssnittet med egenskapen `background-image` .
* Egenskaperna `width` och `height` egenskaperna för ett användargränssnittselement definierar dess logiska storlek. Storleken på bitmappen som skickas till `background-image` påverkar inte den logiska storleken.
* Om du vill använda hög pixeldensitet för högupplösta skärmar som Retina anger du bitmappsbilder som är dubbelt så stora som elementstorleken för det logiska användargränssnittet. Sedan använder du egenskapen för att skala ned bakgrunden till den logiska storleken på elementet i användargränssnittet. `-webkit-background-size:contain`
* Om du vill ta bort en knapp från användargränssnittet lägger du till `display:none` i CSS-klassen.
* Du kan använda olika format för färgvärden som stöds i CSS. Använd formatet om du behöver genomskinlighet `rgba(R,G,B,A)`. I annat fall kan du använda formatet `#RRGGBB`.

## Element i gemensamt användargränssnitt {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Följande är referensdokumentation för användargränssnittselement som gäller för visningsprogrammet för utfällbara foton:
