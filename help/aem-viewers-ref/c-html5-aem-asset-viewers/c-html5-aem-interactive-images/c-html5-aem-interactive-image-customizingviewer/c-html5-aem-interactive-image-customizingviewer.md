---
description: All visuell anpassning och de flesta beteendeanpassningar för den interaktiva bildvisningsprogrammet görs genom att en anpassad CSS skapas.
keywords: responsive
seo-description: All visuell anpassning och de flesta beteendeanpassningar för den interaktiva bildvisningsprogrammet görs genom att en anpassad CSS skapas.
seo-title: Anpassa interaktiv bildvisare
solution: Experience Manager
title: Anpassa interaktiv bildvisare
topic: Dynamic media
uuid: 19868e4e-c2c9-41e0-82a6-20884a9454a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Anpassa interaktiv bildvisare{#customizing-interactive-image-viewer}

All visuell anpassning och de flesta beteendeanpassningar för den interaktiva bildvisningsprogrammet görs genom att en anpassad CSS skapas.

Det föreslagna arbetsflödet är att ta standard-CSS-filen för rätt visningsprogram, kopiera den till en annan plats, anpassa den och ange platsen för den anpassade filen i `style=` kommandot.

CSS-standardfiler finns på följande plats:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

Anpassad CSS-fil måste innehålla samma klassdeklarationer som standardklassdeklarationerna. Om en klassdeklaration utelämnas fungerar visningsprogrammet inte korrekt eftersom det inte innehåller inbyggda standardformat för elementen i användargränssnittet.

Ett annat sätt att tillhandahålla anpassade CSS-regler är att använda inbäddade format direkt på webbsidan eller i någon av de länkade externa CSS-reglerna.

När du skapar anpassad CSS bör du tänka på att visningsprogrammet tilldelar `.s7interactiveimage` klassen till dess behållar-DOM-element. Om du använder en extern CSS-fil som skickas med `style=` kommandot använder du `.s7interactiveimage` klassen som överordnad klass i den underordnade väljaren för dina CSS-regler. Om du lägger till inbäddade format på webbsidan kan du även kvalificera den här väljaren med ett ID för behållar-DOM-elementet enligt följande:

`#<containerId>.s7interactiveimage`

## Skapa responsiv CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

Det är möjligt att rikta in sig på olika enheter och inbäddningsstorlekar i CSS så att innehållet visas på olika sätt, beroende på användarens enhet eller en viss webbsideslayout. Detta omfattar, men är inte begränsat till, olika layouter, elementstorlekar i användargränssnittet och bildupplösning.

Visningsprogrammet har stöd för två sätt att skapa responsiv CSS: CSS-markörer och vanliga CSS-mediefrågor. Du kan använda dessa separat eller tillsammans.

**CSS-markörer**

För att det ska vara lättare att skapa responsiv CSS-kod har visningsprogrammet stöd för CSS-markörer. Det här är speciella CSS-klasser som dynamiskt tilldelas till behållarelementet för visningsprogrammet på den översta nivån. De baseras på visningsprogrammets storlek vid körning och den indatatyp som används på den aktuella enheten.

Den första gruppen med CSS-markörer innehåller `.s7size_large`, `.s7size_medium`och `.s7size_small` klasser. De tillämpas baserat på visningsprogrambehållarens körningsområde. Om visningsområdet till exempel är lika stort eller större än storleken på en vanlig skrivbordsskärm använder du `.s7size_large`. Om området ligger nära en gemensam surfplatta tilldelar du `.s7size_medium`. Om du vill använda områden som liknar mobiltelefonskärmar använder du `.s7size_small`. Det främsta syftet med dessa CSS-markörer är att skapa olika användargränssnittslayouter för olika skärmar och visningsstorlekar.

Den andra gruppen med CSS-markörer innehåller `.s7mouseinput` och `.s7touchinput`. CSS-markören `.s7touchinput` anges om den aktuella enheten kan hantera pekrörelser. Annars `.s7mouseinput` används. Dessa markörer är främst avsedda att skapa indataelement i användargränssnittet med olika skärmstorlekar för olika indatatyper, eftersom större element normalt krävs för pekrörelser.

Följande exempel på CSS anger storleken på inzoomningsknappen till 28 x 28 pixlar på system med musindata och till 56 x 56 pixlar på enheter med pekskärmar. Om visningsprogrammets storlek är ännu mindre anges den till 20 x 20 pixlar.

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

Om du vill ange enheter med olika pixeldensitet som mål måste du använda CSS-mediefrågor. Följande mediefrågeblock skulle innehålla CSS som är specifikt för skärmar med hög densitet:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Att använda CSS-markörer är det mest flexibla sättet att skapa responsiv CSS eftersom det gör att du inte bara kan ange enhetens skärmstorlek som mål, utan även den faktiska visningsstorleken, vilket är användbart för responsiva designlayouter.

Du kan använda CSS-standardfilen för visningsprogram som ett exempel på en CSS-markörmetod.

**CSS-mediefrågor**

Du kan också åstadkomma enhetssensning genom att använda rena CSS-mediefrågor. Allt som omges av ett visst mediefrågeblock tillämpas bara när det körs på en motsvarande enhet.

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

Många visningsgränssnittselement är formaterade med bitmappsbilder och har mer än ett tydligt visuellt läge. Ett bra exempel är en knapp som normalt har minst tre olika lägen: `up`, `over`och `down`. För varje läge krävs en egen bitmappsbild.

Med en klassisk metod för formatering skulle CSS ha en separat referens till den enskilda bildfilen på servern för varje läge i användargränssnittselementet. Här följer ett exempel på CSS för att formatera en inzoomningsknapp:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

Nackdelen med detta är att slutanvändaren får flimmer eller fördröjt svar i användargränssnittet när elementet interagerar med det för första gången. Den här åtgärden inträffar eftersom bildgrafiken för det nya elementläget inte har hämtats ännu. Den här metoden kan också ha en liten negativ inverkan på prestanda på grund av ett ökat antal HTTP-anrop till servern.

CSS-sprites är en annan metod där bilder för alla elementlägen kombineras till en enda PNG-fil som kallas&quot;sprite&quot;. En sådan&quot;sprite&quot; har alla visuella lägen för det angivna elementet placerade efter varandra. När du formaterar ett element i användargränssnittet med fragment refereras samma sprite-bild till för alla olika lägen i CSS. Dessutom används egenskapen för varje läge för att ange vilken del av&quot;sprite&quot;-bilden som ska användas `background-position` . Du kan strukturera en&quot;sprite&quot;-bild på ett lämpligt sätt. Visningsprogram har normalt en lodrät stapling.

Nedan följer ett&quot;sprite&quot;-baserat exempel på hur du formaterar samma inzoomningsknapp tidigare:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Allmän formatinformation och råd {#section-95855dccbbc444e79970f1aaa3260b7b}

* När du anpassar visningsprogrammets användargränssnitt med CSS stöds inte användningen av `!IMPORTANT` regeln för att formatera visningsprogramelement. Regeln ska framför allt inte användas för att åsidosätta standardformat eller körningsformat som tillhandahålls av visningsprogrammet eller visaren-SDK. `!IMPORTANT` Orsaken till detta är att det kan påverka beteendet för rätt komponenter. I stället bör du använda CSS-väljare med rätt specificitet för att ange CSS-egenskaper som dokumenteras i den här referenshandboken för visningsprogram.
* Alla sökvägar till externa resurser i CSS matchas mot CSS-platsen, inte mot visningsprogrammets HTML-sidplats. Tänk på den här regeln när du kopierar standard-CSS till en annan plats. Kopiera även standardresurserna eller uppdatera alla sökvägar i den anpassade CSS-koden.
* Det format du föredrar för bitmappsbilder är PNG.
* Bitmappsgrafik tilldelas till element i användargränssnittet med egenskapen `background-image` .
* Egenskaperna `width` och `height` egenskaperna för ett användargränssnittselement definierar dess logiska storlek. Storleken på bitmappen som skickas till `background-image` påverkar inte dess logiska storlek.
* Om du vill använda hög pixeldensitet för högupplösta skärmar som Retina anger du bitmappsbilder som är dubbelt så stora som elementstorleken för det logiska användargränssnittet. Sedan använder du egenskapen för att skala ned bakgrunden till den logiska storleken på elementet i användargränssnittet. `-webkit-background-size:contain`
* Om du vill ta bort en knapp från användargränssnittet lägger du till `display:none` i CSS-klassen.
* Du kan använda olika format för färgvärden som stöds i CSS. Använd formatet om du behöver genomskinlighet `rgba(R,G,B,A)`. I annat fall kan du använda formatet `#RRGGBB`.

## Gemensamma element i användargränssnittet {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Följande är referensdokumentation för användargränssnittselement som gäller för visningsprogrammet för videobilder:
