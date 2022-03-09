---
title: Textbunden zoom
description: Inline Zoom Viewer är ett bildvisningsprogram. Den visar en statisk bild där den zoomade versionen visas över den statiska bilden när en användare rullar över eller vidrör huvudvyn. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den är utformad för att fungera på stationära datorer och mobila enheter.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2385'
ht-degree: 0%

---

# Textbunden zoom{#inline-zoom}

Inline Zoom Viewer är ett bildvisningsprogram. Den visar en statisk bild där den zoomade versionen visas över den statiska bilden när en användare rullar över eller vidrör huvudvyn. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den är utformad för att fungera på stationära datorer och mobila enheter.

>[!NOTE]
>
>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet.

Visningstypen är 504.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Använda Inline Zoom Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Inline Zoom Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (ett enda JavaScript-skript innehåller alla SDK-komponenter för visningsprogrammet som används av det här visningsprogrammet, resurser och CSS) som hämtats av visningsprogrammet vid körning.

Inline Zoom Viewer kan användas både i popup-läge med en produktionsklar HTML-sida som finns i Image Serving Viewer eller i inbäddat läge där den är integrerad i en målwebbsida med hjälp av dokumenterad API.

Konfigurationen och skalningen liknar den för andra visningsprogram. Du kan använda anpassad CSS för att använda skalning.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med Inline Zoom Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Inline Zoom Viewer stöder enkelberörings- och flerberöringsgester som är vanliga i andra mobilprogram.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesture </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Enkeltryckning </p> </td> 
   <td colname="col2"> <p> Aktiverar den utfällbara vyn eller ändringar mellan den primära och sekundära zoomnivån i färgrutor, markerar en ny miniatyrbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vågrät dragning eller snärtning </p> </td> 
   <td colname="col2"> <p> Bläddrar igenom listan med färgrutor i färgrutefältet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lodrät dragning </p> </td> 
   <td colname="col2"> <p>Om gesten görs i färgruteområdet utförs en inbyggd sidrullning. </p> </td> 
  </tr> 
 </tbody> 
</table>

Visningsprogrammet har också stöd för både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Visningsprogrammet är fullt åtkomligt via tangentbordet.

Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in Inline Zoom Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en klickbar länk som öppnar visningsprogrammet i ett separat webbläsarfönster. I andra fall kan det vara nödvändigt att bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter, eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup-fönster, inbäddning i fast storlek och responsiv inbäddning.

**Popup**

I popup-läget öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras när webbläsarfönstret ändras eller när enhetens orientering ändras.

Det här läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med `window.open()` JavaScript-anrop, korrekt konfigurerat `A` HTML-element eller något annat lämpligt sätt.

Vi rekommenderar att du använder den färdiga HTML-sidan för popup-läget som kallas `FlyoutViewer.html`. Den finns under [!DNL html5/] undermapp till din standarddistribution av Image Serving-Viewers:

`<s7viewers_root>/html5/FlyoutViewer.html`

Det är också nödvändigt att ha komponenten FlyoutZoomView konfigurerad för att fungera i inline-zoomläget. Vi rekommenderar att du använder `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` förinställning för visningsprogrammet för textbunden zoomning, eller en anpassad förinställning som härleds från det. Visuell anpassning kan uppnås genom att använda anpassad CSS.

Följande är ett exempel på HTML-kod som öppnar visningsprogrammet i ett nytt fönster:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Inbäddning med fast storlek och responsiv inbäddning**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet upptar normalt bara en del av webbsidans fastigheter.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva webbsidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddningsläget med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här alternativet passar bäst för webbsidor som har en statisk sidlayout.

Inbäddningsläget för responsiv design förutsätter att visningsprogrammet måste ändra storlek under körning som svar på storleksändringen för dess behållare `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

När du använder responsivt designinbäddningsläge med Inline Zoom Viewer måste du ange explicita brytpunkter för huvudvisningsbilden med `imagereload` parameter. Bäst är att du matchar brytpunkterna med brytpunkterna för visningsprogrammets bredd enligt CSS-reglerna för webbsidor.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur en webbsidbehållare fungerar `DIV` har samma storlek. Om webbsidan bara anger behållarens bredd `DIV`, utan att begränsa höjden väljer visningsprogrammet automatiskt höjden enligt proportionerna för den resurs som används. Den här funktionen innebär att resursen passar in perfekt i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor som använder responsiva designlayoutramverk som Bootstrap eller Foundation.

Om webbsidan i annat fall anger både bredd och höjd för visningsprogrammets behållare `DIV`, fyller visningsprogrammet bara det området och följer den storlek som anges i webbsidans layout. Ett bra exempel på hur du kan använda det här är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definiera behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i huvudet HTML. Innan du kan använda visningsprogrammets API måste du se till att du inkluderar `FlyoutViewer.js`. `FlyoutViewer.js` finns i följande [!DNL html5/js/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media-servrarna som har IS-Viewer installerat.

En relativ sökväg ser ut så här:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Referera endast till JavaScript för huvudvisningsprogrammet `include` på sidan. Referera inte till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körning. Ange särskilt inte direkt HTML5 SDK `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökväg (s.k. konsoliderad SDK) `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversionerna. Adobe har inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att du skickar en direkt referens till valfritt sekundärt JavaScript `include` som används av visningsprogrammet på sidan avbryter visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID senare skickas till visningsprogrammets API.

   Platshållarens DIV är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   Det är webbsidans ansvar att ange rätt `z-index` för platshållarens DIV-element. Om du gör det ser du till att visningsprogrammets utfällbara del visas ovanpå de andra webbsidelementen.

   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Anger visningsprogrammets storlek.

   I det här visningsprogrammet visas miniatyrer när du arbetar med uppsättningar med flera objekt. På stationära datorer placeras miniatyrbilder under huvudvyn. Samtidigt tillåter visningsprogrammet att huvudresursen byts ut under körning med `setAsset()` API. Som utvecklare har du kontroll över hur visningsprogrammet hanterar miniatyrbildsområdet i det nedre området när den nya resursen bara har ett objekt. Det går att behålla den yttre visningsstorleken intakt och låta huvudvyn öka höjden och uppta miniatyrområdet. Eller så kan du hålla storleken på huvudvyn statisk och komprimera det yttre visningsområdet så att webbsidans innehåll kan flyttas uppåt och sedan använda den lediga sidan från miniatyrbilderna.

   Om du vill behålla de yttre gränserna för visningsprogrammet definierar du storleken för `.s7flyoutviewer` CSS-klass på översta nivån i absoluta enheter. Storleksändring i CSS kan placeras direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, och senare tilldelas en post för visningsförinställningar i Dynamic Media Classic, eller skickas explicit med kommandot style.

   Se [Anpassa visningsprogrammet för intern zoomning](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) om du vill ha mer information om hur du formaterar visningsprogrammet med CSS.

   Följande är ett exempel på hur du definierar den statiska storleken på det yttre visningsprogrammet på en HTML-sida:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Du kan se beteendet med ett fast yttre visningsområde på följande exempelsida. Observera att storleken på det yttre visningsprogrammet inte ändras när du växlar mellan uppsättningar:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   Om du vill göra huvudvyns dimensioner statiska definierar du visningsprogrammets storlek i absoluta enheter för den inre `Container` SDK-komponent använda `.s7flyoutviewer .s7container` CSS-väljare. Dessutom bör du åsidosätta den fasta storlek som är definierad för `.s7flyoutviewer` CSS-klassen på den översta nivån i standardvisningsprogrammets CSS genom att ställa in den på `auto`.

   Följande är ett exempel på hur du definierar visningsstorleken för den inre `Container` SDK-komponenten så att huvudvisningsområdet inte ändrar storlek när du byter resurs:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Följande exempelsida visar visningsprogrammets beteende med en fast storlek för huvudvyn. Observera att när du växlar mellan uppsättningar förblir huvudvyn statisk och webbsidans innehåll flyttas lodrätt:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   CSS för standardvisningsprogrammet har också en fast storlek för det yttre området som är utanför rutan.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.FlyoutViewer` -klass, skicka all konfigurationsinformation till konstruktorn och anropa `init()` -metod i en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Objektet bör åtminstone ha `containerId` fält som innehåller namnet på visningsprogrammets behållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som visningsprogrammet stöder. I det här fallet `params` objektet måste ha minst URL för bildserver som skickas som `serverUrl` egendom, den ursprungliga tillgången som `asset` parameter, bassökväg för inläsning av CSS som `contentUrl` parameter och förinställningsnamn som `config` parameter. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet, ring `init()` metod precis före stängning `BODY` eller på brödtexten `onload()` -händelse.

   Samtidigt behöver behållarelementet inte nödvändigtvis vara en del av webbsidans layout ännu. Den kan till exempel vara dold med `display:none` format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När den här åtgärden utförs återtas visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar `init()` -metod. Exemplet förutsätter `inlineZoomViewer` är visningsprograminstansen, `s7viewer` är namnet på platshållaren `DIV`; `http://s7d1.scene7.com/is/image/` är webbadressen till bildservern, och `Scene7SharedAssets/ImageSet-Views-Sample` är tillgången:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in visningsprogrammet för infogad zoomning med fast storlek:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsiv designinbäddning med obegränsad höjd {#section-056cb574713c4d07be6d07cf3c598839}

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets körningsstorlek `DIV`. I följande exempel antar du att webbsidan tillåter visningsprogrammets behållare `DIV` för att ta 40 % av webbläsarens fönsterstorlek och låta dess höjd vara obegränsad. Webbsidans HTML-kod ser ut så här:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Att lägga till visningsprogrammet på en sådan sida liknar stegen för inbäddning med fast storlek. Den enda skillnaden är att du måste åsidosätta den fasta storleken från CSS för standardvisningsprogrammet med den angivna storleken i relativa enheter.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definiera behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

Alla stegen ovan är desamma som med inbäddning med fast storlek med följande tre undantag:

* lägg till behållaren `DIV` till den befintliga innehavaren `DIV`;
* tillagd `imagereload` parameter med explicita brytpunkter,
* i stället för att ställa in en fast visningsstorlek med absoluta enheter används CSS som ställer in visningsprogrammet `width` och `height` till 100 % som i följande:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[Direktdemonstrationer](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativ demoplats](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Flexibel storleksinbäddning med definierad bredd och höjd {#section-0a329016f9414d199039776645c693de}

Om det finns inbäddning i flexibel storlek med angiven bredd och höjd är webbsidans format annorlunda. Det ger båda storlekarna till `"holder"` DIV och centrerar det i webbläsarfönstret. Dessutom anger webbsidan storleken på `HTML` och `BODY` -element till 100 procent.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Resten av inbäddningsstegen är identiska med stegen som används för responsiv designinbäddning med obegränsad höjd. Följande exempel visas:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Bädda in med Setter-baserat API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Den här API-konstruktorn tar inga parametrar och konfigurationsparametrar anges med `setContainerId()`, `setParam()`och `setAsset()` API-metoder, med separata JavaScript-anrop.

I följande exempel visas hur du använder inbäddning med fast storlek med set-based API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
