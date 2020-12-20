---
description: 'null'
keywords: responsive
seo-description: 'null'
seo-title: Anpassa Video Viewer
solution: Experience Manager
title: Anpassa Video Viewer
topic: Dynamic media
uuid: e18fdf8b-5834-4c99-b8a3-90d1f8310dc1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1258'
ht-degree: 0%

---


# Anpassa Video Viewer{#customizing-video-viewer}

All visuell anpassning och de flesta beteendeanpassningar görs genom att en anpassad CSS skapas.

Det föreslagna arbetsflödet är att ta standard-CSS-filen för rätt visningsprogram, kopiera den till en annan plats, anpassa den och ange platsen för den anpassade filen i kommandot `style=`.

CSS-standardfiler finns på följande plats:

`<s7_viewers_root>/html5/VideoViewer.css`

Anpassad CSS-fil måste innehålla samma klassdeklarationer som standardklassdeklarationerna. Om en klassdeklaration utelämnas fungerar visningsprogrammet inte korrekt eftersom det inte innehåller inbyggda standardformat för elementen i användargränssnittet.

Ett annat sätt att tillhandahålla anpassade CSS-regler är att använda inbäddade format direkt på webbsidan eller i någon av de länkade externa CSS-reglerna.

När du skapar anpassad CSS måste du komma ihåg att visningsprogrammet tilldelar klassen `.s7videoviewer` till dess behållar-DOM-element. Om du använder en extern CSS-fil som skickas med kommandot `style=` ska du använda klassen `.s7videoviewer` som överordnad klass i den underordnade väljaren för dina CSS-regler. Om du bäddar in format på webbsidan kan du även kvalificera väljaren med ett ID för behållar-DOM-elementet enligt följande:

`#<containerId>.s7videoviewer`

## Skapar responsiv CSS {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

Det går att rikta in sig på olika enheter i CSS för att visa innehållet på olika sätt beroende på användarens enhet. Den här målgruppen omfattar, men är inte begränsad till, olika elementstorlekar i användargränssnittet och bildupplösning.

Visningsprogrammet har stöd för två sätt att skapa responsiv CSS: CSS-markörer och vanliga CSS-mediefrågor. Du kan använda dessa separat eller tillsammans.

**CSS-markörer**

För att det ska vara lättare att skapa responsiv designad CSS har visningsprogrammet stöd för CSS-markörer som har särskilda CSS-klasser som dynamiskt tilldelas till visningsprogrambehållarelementet på den översta nivån baserat på visningsprogrammets storlek vid körning och den indatatyp som används på den aktuella enheten.

Den första gruppen med CSS-markörer innehåller klasserna `.s7size_large`, `.s7size_medium` och `.s7size_small`. De tillämpas baserat på visningsprogrambehållarens körningsområde. Det vill säga om visningsområdet är lika med eller större än storleken på en vanlig skrivbordsskärm `.s7size_large` används, om området är nästan lika stort som en vanlig surfplatteenhet `.s7size_medium` har tilldelats. För områden som liknar mobiltelefonskärmar är `.s7size_small` inställt. Det främsta syftet med dessa CSS-markörer är att skapa olika användargränssnittslayouter för olika skärmar och visningsstorlekar.

Den andra gruppen CSS-markörer innehåller `.s7mouseinput` och `.s7touchinput`. `.s7touchinput` är inställt om den aktuella enheten har funktioner för pekrörelser, i annat fall  `.s7mouseinput` används. Dessa markörer är avsedda att skapa indataelement i användargränssnittet med olika skärmstorlekar för olika indatatyper, eftersom större element normalt krävs för pekrörelser. Om enheten har både musindata- och pekfunktioner är `.s7touchinput` inställt och visningsprogrammet återger ett pekvänligt användargränssnitt.

I följande exempel på CSS anges storleken på uppspelnings-/pausknappen till 28 x 28 pixlar på system med musindata och 56 x 56 pixlar på pekenheter. Dessutom döljs knappen helt om visningsprogrammets storlek blir riktigt liten:

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Om du vill använda enheter med en annan pixeldensitet som mål använder du CSS-mediefrågor. Följande mediefrågeblock skulle innehålla CSS som är specifikt för skärmar med hög densitet:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Att använda CSS-markörer är det mest flexibla sättet att skapa responsiv CSS eftersom det gör att du inte bara kan rikta in dig på enhetens skärmstorlek utan även på den faktiska visningsstorleken, vilket kan vara användbart för responsiva layouter.

Använd CSS-standardfilen för visningsprogrammet som ett exempel på en CSS-markörmetod.

**CSS-mediefrågor**

Enhetsavkänning kan även göras med rena CSS-mediefrågor. Allt som omges av ett visst mediefrågeblock tillämpas bara när det körs på en motsvarande enhet.

Använd fyra CSS-mediefrågor som definieras i CSS i den ordning som anges nedan när de används i mobilvisningsprogram:

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

Med CSS-mediefrågor kan du ordna CSS med enhetsavkänning på följande sätt:

* För det första definierar det skrivbordsspecifika avsnittet alla egenskaper som är skrivbordsspecifika eller gemensamma för alla skärmar.
* För det andra bör de fyra mediefrågorna följa ovanstående definition och innehålla CSS-regler som är specifika för motsvarande enhetstyp.

Du behöver inte duplicera hela CSS för visningsprogram i varje mediefråga. Endast egenskaper som är specifika för vissa enheter omdefinieras i en mediefråga.

## CSS-sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

Många visningsgränssnittselement är formaterade med bitmappsbilder och har mer än ett tydligt visuellt läge. Ett bra exempel är en knapp som normalt har minst tre olika lägen: &quot;up&quot;, &quot;over&quot; och &quot;down&quot;. För varje läge krävs en egen bitmappsbild.

Med en klassisk metod för formatering skulle CSS ha en separat referens till enskilda bildfiler på servern för varje läge i användargränssnittselementet. Här följer ett exempel på CSS för formatering av en helskärmsknapp:

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

Nackdelen med detta är att slutanvändaren får flimmer eller fördröjt svar i användargränssnittet när elementet interagerar med det för första gången. Den här åtgärden inträffar eftersom bildgrafiken för det nya elementläget inte har hämtats ännu. Den här metoden kan också ha en liten negativ inverkan på prestanda på grund av ett ökat antal HTTP-anrop till servern.

CSS-sprites är en annan metod där bilder för alla elementlägen kombineras till en enda PNG-fil som kallas&quot;sprite&quot;. En sådan&quot;sprite&quot; har alla visuella lägen för det angivna elementet placerade efter varandra. När du formaterar ett element i användargränssnittet med fragment refereras samma sprite-bild till för alla olika lägen i CSS. Dessutom används egenskapen `background-position` för varje läge för att ange vilken del av Sprite-bilden som ska användas. Du kan strukturera en&quot;sprite&quot;-bild på ett lämpligt sätt. Visningsprogram har normalt en lodrät stapling. Nedan visas ett&quot;sprite&quot;-baserat exempel på hur du formaterar samma helskärmsknapp från ovan:

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Allmän formatinformation och råd {#section-097418bd618740bba36352629e4d88e1}

* Alla sökvägar till externa resurser i CSS matchas mot CSS-platsen och inte mot platsen för visningsprogrammets HTML-sida. Kom ihåg att ta hänsyn till den här regeln när du kopierar standard-CSS till en annan plats. Kopiera standardresurserna eller uppdateringssökvägarna i den anpassade CSS-koden.
* Det format du föredrar för bitmappsbilder är PNG.
* Bitmappsgrafik tilldelas till element i användargränssnittet med egenskapen `background-image`.
* Egenskaperna `width` och `height` för ett användargränssnittselement definierar dess logiska storlek. Storleken på bitmappen som skickas till `background-image` påverkar inte den logiska storleken.

* Om du vill använda hög pixeldensitet för högupplösta skärmar som Retina anger du bitmappsbilder som är dubbelt så stora som elementstorleken för det logiska användargränssnittet. Använd sedan egenskapen `-webkit-background-size:contain` för att skala bakgrunden ned till elementstorleken för det logiska användargränssnittet.
* Om du vill ta bort en knapp från användargränssnittet lägger du till `display:none` i CSS-klassen.
* Du kan använda olika format för färgvärden som stöds i CSS. Använd formatet `rgba(R,G,B,A)` om du behöver genomskinlighet. Annars kan du använda formatet `#RRGGBB`.

* När du anpassar visningsprogrammets användargränssnitt med CSS stöds inte användningen av regeln `!IMPORTANT` för att formatera visningsprogramelement. I synnerhet ska `!IMPORTANT`-regeln inte användas för att åsidosätta standardformat eller körningsformat som tillhandahålls av visningsprogrammet eller visaren-SDK:n. Orsaken är att det kan påverka beteendet för rätt komponenter. I stället bör du använda CSS-väljare med rätt specificitet för att ange CSS-egenskaper som dokumenteras i den här referenshandboken.

## Element för gemensamt användargränssnitt {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Nedan följer referensdokumentation för användargränssnittselement som gäller för Video Viewer:
