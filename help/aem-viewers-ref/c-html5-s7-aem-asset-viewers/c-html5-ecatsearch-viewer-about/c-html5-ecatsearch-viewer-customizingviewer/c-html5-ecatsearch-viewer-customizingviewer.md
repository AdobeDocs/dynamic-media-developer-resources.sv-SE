---
description: All visuell anpassning och de flesta beteendeanpassningar för visningsprogrammet för eCatalog-sökning görs genom att en anpassad CSS skapas.
keywords: responsiv
solution: Experience Manager
title: Anpassa visningsprogrammet för eCatalog Search
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---

# Anpassa visningsprogrammet för eCatalog Search{#customizing-ecatalog-search-viewer}

All visuell anpassning och de flesta beteendeanpassningar för visningsprogrammet för eCatalog-sökning görs genom att en anpassad CSS skapas.

Det föreslagna arbetsflödet är att ta standard-CSS-filen för rätt visningsprogram, kopiera den till en annan plats, anpassa den och ange platsen för den anpassade filen i kommandot `style=`.

CSS-standardfiler finns på följande plats:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Den anpassade CSS-filen måste innehålla samma klassdeklarationer som standardklassdeklarationerna. Om en klassdeklaration utelämnas fungerar visningsprogrammet inte korrekt eftersom det inte innehåller inbyggda standardformat för elementen i användargränssnittet.

Ett annat sätt att tillhandahålla anpassade CSS-regler är att använda inbäddade format direkt på webbsidan eller i någon av de länkade externa CSS-reglerna.

När du skapar anpassad CSS bör du tänka på att visningsprogrammet tilldelar klassen `.s7ecatalogsearchviewer` till dess behållar-DOM-element. Om du använder en extern CSS-fil som skickas med kommandot `style=` ska du använda klassen `.s7ecatalogsearchviewer` som överordnad klass i den underordnade väljaren för dina CSS-regler. Om du gör inbäddade format på webbsidan kan du även kvalificera den här väljaren med ett ID för behållar-DOM-elementet enligt följande:

`#<containerId>.s7ecatalogsearchviewer`

## Skapa responsiv CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Det är möjligt att rikta in sig på olika enheter och inbäddningsstorlekar i CSS så att innehållet visas på olika sätt, beroende på användarens enhet eller en viss webbsideslayout. Detta omfattar, men är inte begränsat till, olika webbsideslayouter, elementstorlekar i användargränssnittet och bildupplösning.

Visningsprogrammet har stöd för två metoder för att skapa responsiv CSS: CSS-markörer och vanliga CSS-mediefrågor. Du kan använda dessa metoder oberoende av varandra eller tillsammans.

**CSS-markörer**

För att det ska vara lättare att skapa responsiv designad CSS har visningsprogrammet stöd för CSS-markörer som har särskilda CSS-klasser som dynamiskt tilldelas till visningsprogrambehållarelementet på den översta nivån baserat på visningsprogrammets storlek vid körning och den indatatyp som används på den aktuella enheten.

Den första gruppen med CSS-markörer innehåller klasserna `.s7size_large`, `.s7size_medium` och `.s7size_small`. De tillämpas baserat på visningsprogrambehållarens körningsområde. Det vill säga om visningsområdet är lika med eller större än storleken på en vanlig skrivbordsskärm `.s7size_large` används, om området är nästan lika stort som en vanlig surfplatteenhet `.s7size_medium` har tilldelats. För områden som liknar mobiltelefonskärmar är `.s7size_small` inställt. Det främsta syftet med dessa CSS-markörer är att skapa olika användargränssnittslayouter för olika skärmar och visningsstorlekar.

Den andra gruppen med CSS-markörer innehåller `.s7mouseinput` och `.s7touchinput`. `.s7touchinput` är inställt om den aktuella enheten har funktioner för pekrörelser, i annat fall  `.s7mouseinput` används. Dessa markörer är avsedda att skapa indataelement i användargränssnittet med olika skärmstorlekar för olika indatatyper, eftersom större element normalt krävs för pekrörelser. Om enheten har både musindata- och pekfunktioner är `.s7touchinput` inställt och visningsprogrammet återger ett pekvänligt användargränssnitt.

Följande exempel på CSS anger storleken på inzoomningsknappen till 28 x 28 pixlar på system med musindata och 56 x 56 pixlar på enheter med pekskärm. Dessutom döljs knappen helt om visningsprogrammets storlek blir riktigt liten:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Om du vill använda enheter med en annan pixeldensitet som mål använder du CSS-mediefrågor. Följande mediefrågeblock skulle innehålla CSS som är specifikt för skärmar med hög densitet:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Att använda CSS-markörer är det mest flexibla sättet att skapa responsiv CSS eftersom det gör att du inte bara kan rikta in dig på enhetens skärmstorlek utan även på den faktiska visningsstorleken, vilket kan vara användbart för responsiva designade sidlayouter.

Använd CSS-standardfilen för visningsprogrammet som ett exempel på en CSS-markörmetod.

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

## CSS-fragment {#section-9d570f95eb2443aca74c1b02f6e89aff}

Många visningsgränssnittselement är formaterade med bitmappsbilder och har mer än ett tydligt visuellt läge. Ett bra exempel är en knapp som normalt har minst tre olika lägen: &quot;up&quot;, &quot;over&quot; och &quot;down&quot;. För varje läge krävs en egen bitmappsbild.

Med en klassisk metod för formatering skulle CSS ha en separat referens till enskilda bildfiler på servern för varje läge i användargränssnittselementet. Här följer ett exempel på CSS för att formatera en inzoomningsknapp:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Nackdelen med detta är att slutanvändaren får flimmer eller fördröjt svar i användargränssnittet när elementet interagerar med det för första gången. Den här åtgärden inträffar eftersom bildgrafiken för det nya elementläget inte har hämtats ännu. Den här metoden kan också ha en liten negativ inverkan på prestanda på grund av ett ökat antal HTTP-anrop till servern.

CSS-sprites är en annan metod där bilder för alla elementlägen kombineras till en enda PNG-fil som kallas&quot;sprite&quot;. En sådan&quot;sprite&quot; har alla visuella lägen för det angivna elementet placerade efter varandra. När du formaterar ett element i användargränssnittet med fragment refereras samma sprite-bild till för alla olika lägen i CSS. Dessutom används egenskapen `background-position` för varje läge för att ange vilken del av Sprite-bilden som ska användas. Du kan strukturera en&quot;sprite&quot;-bild på ett lämpligt sätt. Visningsprogram har normalt en lodrät stapling. Nedan visas ett&quot;sprite&quot;-baserat exempel på hur du formaterar samma inzoomningsknapp ovan:

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Allmän formatinformation och råd {#section-95855dccbbc444e79970f1aaa3260b7b}

* När du anpassar visningsprogrammets användargränssnitt med CSS stöds inte användningen av regeln `!IMPORTANT` för att formatera visningsprogramelement. I synnerhet ska `!IMPORTANT`-regeln inte användas för att åsidosätta standardformat eller körningsformat som tillhandahålls av visningsprogrammet eller visaren-SDK:n. Orsaken är att det kan påverka beteendet för rätt komponenter. I stället bör du använda CSS-väljare med rätt specificitet för att ange CSS-egenskaper som dokumenteras i den här referenshandboken.
* Alla sökvägar till externa resurser i CSS matchas mot CSS-platsen, inte mot visningsprogrammets HTML-sidplats. Tänk på den här regeln när du kopierar standard-CSS till en annan plats. Kopiera även standardresurserna eller uppdatera sökvägarna i den anpassade CSS-koden.
* Det format du föredrar för bitmappsbilder är PNG.
* Bitmappsgrafik tilldelas till element i användargränssnittet med egenskapen `background-image`.
* Egenskaperna `width` och `height` för ett användargränssnittselement definierar dess logiska storlek. Storleken på bitmappen som skickas till `background-image` påverkar inte den logiska storleken.
* Om du vill använda hög pixeldensitet för högupplösta skärmar som Retina anger du bitmappsbilder som är dubbelt så stora som elementstorleken för det logiska användargränssnittet. Använd sedan egenskapen `-webkit-background-size:contain` för att skala bakgrunden ned till elementstorleken för det logiska användargränssnittet.
* Om du vill ta bort en knapp från användargränssnittet lägger du till `display:none` i CSS-klassen.
* Du kan använda olika format för färgvärden som stöds i CSS. Använd formatet `rgba(R,G,B,A)` om du behöver genomskinlighet. Annars kan du använda formatet `#RRGGBB`.

## Element i gemensamt användargränssnitt {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Nedan följer referensdokumentation för användargränssnittselement som gäller eCatalog Search Viewer:

* [Knappen Lägg till favorit](r-html5-ecatsearch-customize-addfavorite.md)
* [Knappen Stäng](r-html5-ecatsearch-customize-closebutton.md)
* [Hämta](r-html5-ecatsearch-customize-download.md)
* [E-postresurs](r-html5-ecatsearch-customize-emailshare.md)
* [Bädda in resurs](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Favoriter, effekt](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Favoriter-menyn](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Vyn Favoriter](r-html5-ecatsearch-customize-favoritesview.md)
* [Knappen Första sidan](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Fokusmarkering](r-html5-ecatsearch-customize-focushighlight.md)
* [Helskärmsknapp](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Ikoneffekt](r-html5-ecatsearch-customize-iconeffect.md)
* [Popup för panelen Info](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Bildschemaeffekt](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Knappen Stor nästa sida](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Knappen Stor föregående sida](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Knappen Sista sidan](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Länkresurs](r-html5-ecatsearch-customize-linkshare.md)
* [Huvudkontrollfält](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Huvudvisningsområde](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Knappen Nästa sida](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Sidindikator](r-html5-ecatsearch-customize-pageindicator.md)
* [Sidvy](r-html5-ecatsearch-customize-pageview.md)
* [Knappen Föregående sida](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Skriv ut](r-html5-ecatsearch-customize-print.md)
* [Knappen Ta bort favorit](r-html5-ecatsearch-customize-removefavorite.md)
* [Sökknapp](r-html5-ecatsearch-customize-searchbutton.md)
* [Sökeffekt](r-html5-ecatsearch-customize-searcheffect.md)
* [Sökresultatpanel](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Sekundärt kontrollfält](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Social andel](r-html5-ecatsearch-customize-socialshare.md)
* [Innehållsförteckning](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniatyrbilder](r-html5-ecatsearch-customize-thumbnails.md)
* [Knappen Miniatyrbilder](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Verktygstips](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Knappen Visa alla favoriter](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Knappen Zooma in](r-html5-ecatsearch-customize-zoominbutton.md)
* [Knappen Zooma ut](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Knappen Zoomåterställning](r-html5-ecatsearch-customize-zoomresetbutton.md)
