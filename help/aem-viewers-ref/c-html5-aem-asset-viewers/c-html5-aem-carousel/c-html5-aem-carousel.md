---
title: Carousel
description: Carousel Viewer är ett visningsprogram som visar en karusell med icke-zoombara banderollbilder med klickbara hotspot-områden. Det här visningsprogrammet kan hjälpa dig att implementera en shoppingupplevelse där användarna kan välja en hotspot eller ett område över banderollbilden. De kan omdirigeras till en Quickview- eller produktinformationssida på kundens webbplats. Den är utformad för att fungera på stationära datorer och mobila enheter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1888'
ht-degree: 0%

---

# Carousel{#carousel}

Carousel Viewer är ett visningsprogram som visar en karusell med icke-zoombara banderollbilder med klickbara hotspot-områden. Det här visningsprogrammet kan hjälpa dig att implementera en shoppingupplevelse där användarna kan välja en hotspot eller ett område över banderollbilden. De kan omdirigeras till en Quickview- eller produktinformationssida på kundens webbplats. Den är utformad för att fungera på stationära datorer och mobila enheter.

>[!NOTE]
>
>Bilder som använder bildåtergivning eller användargenererat innehåll (UGC) stöds inte av det här visningsprogrammet.

Visningstypen är 511.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html)

## Systemkrav {#section-b7270cc4290043399681dc504f043609}

Se [Systemkrav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Använda Carousel Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Carousel Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-fil innehåller alla SDK-komponenter för visningsprogrammet som används av det här visningsprogrammet, resurser, CSS) som hämtats av visningsprogrammet under körning.

Carousel Viewer kan användas både i popup-läge med en produktionsklar HTML-sida som finns i IS Viewer, eller i inbäddat läge där den integreras med målwebbsidan med hjälp av dokumenterad API.

Konfigurationen och skalningen liknar den för andra visningsprogram som beskrivs i den här hjälpen. All skalning görs med anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med Carousel Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Du kan navigera genom karuselluppsättningen genom att svepa vågrätt över huvudvyn eller genom att använda två pilknappar på den stationära datorn. Ange indikatorpunkter visar den aktuella positionen inom uppsättningen.

Visningsprogrammet kan återge aktiveringspunkter eller områden ovanpå banderollbilden för att indikera det interaktiva området i produkten.

Om du klickar eller trycker på en hotspot eller ett område utlöses en åtgärd som är kopplad till den under redigeringstiden. Åtgärden kan omdirigeras till en annan sida på webbplatsen eller skickas tillbaka produktinformation till webbsidans logik, som i sin tur kan utlösa en snabbvy med relaterat produktinnehåll.

Visningsprogrammet är fullt åtkomligt via tangentbordet.

Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in Carousel Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

**Om popup-läge**

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändrar storlek eller om en mobilenhets orientering ändras.

Popup-läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med `window.open()` JavaScript-anrop, korrekt konfigurerat `A` HTML-element eller någon annan lämplig metod.

Vi rekommenderar att du använder en färdig HTML-sida för popup-läge. I det här fallet anropas den `CarouselViewer.html` och finns i `html5/` undermapp till din standarddistribution av IS-Viewer:

`<s7viewers_root>/html5/CarouselViewer.html`

Du kan anpassa visuellt genom att använda anpassad CSS.

Här följer ett exempel på HTML som öppnar visningsprogrammet i ett nytt fönster:

```html {.line-numbers}
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan. Den här webbsidan kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet upptar normalt bara en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och responsiva designade sidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Den här metoden är det bästa alternativet för webbsidor med en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet måste ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`, utan att begränsa höjden, väljer visningsprogrammet automatiskt höjden enligt proportionerna för resursen som används. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor med flexibla ramverk för webbdesign som Bootstrap och Foundation.

Om webbsidan i annat fall anger både bredd och höjd för visningsprogrammets behållare `DIV`fyller visningsprogrammet bara det området. Den har också samma storlek som webbsidans layout. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definiera behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i huvudet HTML. Innan du kan använda visningsprogrammets API måste du se till att du inkluderar [!DNL CarouselViewer.js]. The [!DNL CarouselViewer.js] filen finns under [!DNL html5/js/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>Referera endast till JavaScript för huvudvisningsprogrammet `include` på sidan. Referera inte till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körning. Ange särskilt inte direkt HTML5 SDK `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökväg (s.k. konsoliderad SDK) `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversionerna. Adobe har inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att du skickar en direkt referens till valfritt sekundärt JavaScript `include` som används av visningsprogrammet på sidan avbryter visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definiera behållaren `DIV`.

   Lägg till en tom `DIV` -element till sidan där du vill att visningsprogrammet ska visas. The `DIV` -elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API. DIV har den storlek som anges via CSS.

   Platshållaren `DIV` är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   Följande är ett exempel på en definierad platshållare `DIV` element:

   ```CSS {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att deklarera det för `.s7carouselviewer` CSS-klass på översta nivån i absoluta enheter, eller med `stagesize` modifierare.

   Du kan ange storlek i CSS direkt på HTML-sidan. Du kan också lägga in storleksändring i en anpassad CSS-fil för visningsprogrammet, som sedan tilldelas till en post för visningsförinställningar i AEM Assets - On demand, eller skickas explicit med `style` -kommando.

   Se [Anpassa Carousel Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) om du vill ha mer information om hur du formaterar visningsprogrammet med CSS.

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på HTML-sidan:

   ```CSS {.line-numbers}
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Du kan skicka `stagesize` modifierare med visarens initieringskod med `params` -samling eller som ett API-anrop enligt beskrivningen i avsnittet Kommandoreferens, så här:

   ```CSS {.line-numbers}
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.CarouselViewer` -klass, skicka all konfigurationsinformation till konstruktorn och anropa `init()` -metod i en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Objektet bör åtminstone ha `containerId` fält som innehåller namnet på visningsprogrammets behållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet. I det här fallet `params` objektet måste ha minst URL för bildserver som skickas som `serverUrl` och den ursprungliga tillgången som `asset` parameter. Med det JSON-baserade initierings-API:t kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet, ring `init()` metod precis före stängning `BODY` eller på brödtexten `onload()` -händelse.

   Samtidigt behöver behållarelementet inte nödvändigtvis vara en del av webbsidans layout ännu. Den kan till exempel vara dold med `display:none` format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När den här funktionaliteten inträffar återgår visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar nödvändiga minimikonfigurationsalternativ till konstruktorn och anropar `init()` -metod. Exemplet förutsätter `carouselViewer` är visningsprograminstansen, `s7viewer` är namnet på platshållaren `DIV`; `https://adobedemo62-h.assetsadobe.com/is/image` är webbadressen för bildvisning, och `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` är tillgången:

   ```javascript {.line-numbers}
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in Carousel Viewer med fast storlek:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsiv designinbäddning med obegränsad höjd**

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets körningsstorlek `DIV`. I följande exempel antar du att webbsidan tillåter visningsprogrammets behållare `DIV` för att ta 40 % av webbläsarens fönsterstorlek. Och höjden är obegränsad. Webbsidans HTML-kod ser ut så här:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Att lägga till visningsprogrammet på en sådan sida liknar stegen för inbäddning med fast storlek. Den enda skillnaden är att du inte behöver definiera visningsprogrammets storlek explicit.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definiera behållaren `DIV`.
1. Skapa och initiera visningsprogrammet.

Alla steg ovan är desamma som med inbäddning med fast storlek. Lägg till behållaren `DIV` till befintlig `"holder"` `DIV`. Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html)

**Flexibel storlek för inbäddning med definierad bredd och höjd**

Vid inbäddning i flexibel storlek med definierad bredd och höjd är webbsidans format annorlunda. Det ger båda storlekarna till `"holder"` DIV och centrera det i webbläsarfönstret. Dessutom anger webbsidan storleken på `HTML` och `BODY` -element till 100 procent.

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

Resten av inbäddningsstegen är identiska med stegen som används för responsiv inbäddning med obegränsad höjd. Följande exempel visas:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Bädda in med Setter-baserat API**

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Den här API-konstruktorn tar inga parametrar och konfigurationsparametrar anges med `setContainerId()`, `setParam()`och `setAsset()` API-metoder med separata JavaScript-anrop.

I följande exempel visas hur du använder inbäddning med fast storlek med det inställningsbaserade API:t:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```
