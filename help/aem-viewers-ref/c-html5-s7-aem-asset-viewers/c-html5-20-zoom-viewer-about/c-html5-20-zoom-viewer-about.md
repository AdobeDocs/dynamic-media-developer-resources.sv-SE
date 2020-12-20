---
description: Zoom Viewer är ett bildvisningsprogram som visar en zoombar bild. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den har zoomverktyg, helskärmsstöd, färgrutor och en valfri stängningsknapp. Den är utformad för att fungera på stationära datorer och mobila enheter.
keywords: responsive
seo-description: Zoom Viewer är ett bildvisningsprogram som visar en zoombar bild. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den har zoomverktyg, helskärmsstöd, färgrutor och en valfri stängningsknapp. Den är utformad för att fungera på stationära datorer och mobila enheter.
seo-title: Zooma
solution: Experience Manager
title: Zooma
topic: Dynamic media
uuid: ec2a91e2-ce2c-48b1-a2b2-8671524288c7
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2460'
ht-degree: 0%

---


# Zooma{#zoom}

Zoom Viewer är ett bildvisningsprogram som visar en zoombar bild. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den har zoomverktyg, helskärmsstöd, färgrutor och en valfri stängningsknapp. Den är utformad för att fungera på stationära datorer och mobila enheter.

>[!NOTE]
>
>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet.

Visningstyp 502.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Använda Zoom Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Zoom Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-fil innehåller alla Viewer SDK-komponenter som används av det här visningsprogrammet, resurser, CSS) som hämtats av visningsprogrammet under körning.

Du kan använda Zoom Viewer i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer eller i inbäddat läge, där den integreras med målwebbsidan med dokumenterat API.

Konfigurationen och skalningen liknar den för andra visningsprogram. All skalning görs med anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med Zoom Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Zoom Viewer stöder följande pekgester som är vanliga i andra mobilprogram. När visningsprogrammet inte kan bearbeta användarens svepningsgest vidarebefordrar det händelsen till webbläsaren för att utföra den inbyggda sidrullningen. Den här typen av funktioner gör att användaren kan navigera på sidan även om användaren upptar större delen av enhetens skärmområde.

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
   <td colname="col2"> <p> Väljer ny miniatyrbild i färgrutor. I huvudvyn döljs eller visas element i användargränssnittet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dubbelknacka </p> </td> 
   <td colname="col2"> <p> Zoomar in en nivå tills maximal förstoring nås. Nästa dubbelknackningsgest återställer visningsprogrammet till det inledande visningsläget. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Knipning </p> </td> 
   <td colname="col2"> <p>Zoomar in eller ut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vågrät dragning eller snärtning </p> </td> 
   <td colname="col2"> <p> Bläddrar igenom listan med färgrutor i färgrutefältet. </p> <p> Om bilden är i ett återställningsläge och <span class="codeph">-bildruteövergångsparametern </span> är inställd på bildruta, ändras resursen med bildruteanimeringen. För andra <span class="codeph">-bildruteövergångslägen </span> utför gesten intern sidbläddring. </p> <p> Om bilden zoomas in flyttas den vågrätt. Om bilden flyttas till vykanten och en svepning utförs i samma riktning, utför gesten intern sidbläddring. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lodrät dragning </p> </td> 
   <td colname="col2"> <p> Om bilden är i ett återställningsläge utför gesten intern sidbläddring. </p> <p> När bilden har zoomats in flyttas den vertikalt. Om bilden flyttas till vykanten och en svepning utförs i samma riktning, utför gesten den inbyggda sidrullningen. </p> <p> Om gesten görs i färgruteområdet utförs en inbyggd sidrullning. </p> </td> 
  </tr> 
 </tbody> 
</table>

Visningsprogrammet stöder både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Visningsprogrammet är fullt åtkomligt via tangentbordet.

Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in Zoom Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en länk som, när användaren klickar på den, öppnar visningsprogrammet i ett separat webbläsarfönster. I andra fall måste du bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk layout, eller använda responsiv design som visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup-fönster, inbäddning i fast storlek och responsiv designinbäddning.

**Om popup-läge**

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändras eller om enhetens orientering ändras.

Det här läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med hjälp av JavaScript-anrop (`window.open()`), korrekt konfigurerat HTML-element (`A`) eller någon annan lämplig metod.

Vi rekommenderar att du använder en körklar HTML-sida för popup-åtgärdsläget. HTML-sidan som är klar att användas kallas `ZoomViewer.html` och finns under undermappen `html5/` i din standarddistribution av IS-Viewer enligt följande:

`<s7viewers_root>/html5/ZoomViewer.html`

Använd anpassad CSS för att få ett anpassat utseende på sidan.

Följande är ett exempel på HTML-kod som öppnar visningsprogrammet i det nya fönstret:

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet upptar normalt bara en del av webbsidans fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designade sidor som justerar layouten automatiskt, beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här alternativet är det bästa alternativet för webbsidor med en statisk layout.

Inbäddningsläget för responsiv design förutsätter att det krävs en storleksändring av visningsprogrammet under körningen på grund av storleksändringen av dess behållare `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel layout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger bredden på behållaren `DIV`, och dess höjd inte begränsas, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den resurs som används. Den här logiken gör att resursen passar in perfekt i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor som använder responsiva layoutramverk som Bootstrap, Foundation och så vidare.

Om webbsidan anger både bredd och höjd för visningsprogrammets behållare `DIV` fyller visningsprogrammet det området och följer den storlek som webbsidan ger. Om du till exempel bäddar in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

## Inbäddning med fast storlek {#section-44f365e6c0dd40709467a459afa82a7f}

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i HTML-huvudet. Innan du kan använda visningsprogrammets API måste du ta med [!DNL ZoomViewer.js]. Filen [!DNL ZoomViewer.js] finns under undermappen [!DNL html5/js/] i din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>Du bör bara referera till JavaScript-filen `include` för huvudvisningsprogrammet på sidan. Du bör inte referera till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körningen. Referera inte direkt till HTML5 SDK `Utils.js`-biblioteket som läses in av visningsprogrammet från kontextsökvägen `/s7viewers` (s.k. konsoliderad SDK `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversioner. Adobe sparar inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att om du skickar en direkt referens till ett sekundärt JavaScript `include` som används av visningsprogrammet på sidan så bryts visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API.

   Platshållarens DIV är ett positionerat element, vilket innebär att CSS-egenskapen `position` är inställd på `relative` eller `absolute`.

   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Anger visningsprogrammets storlek.

   I det här visningsprogrammet visas miniatyrbilder när du arbetar med uppsättningar med flera objekt. Miniatyrbilder för skrivbordssystem placeras under huvudvyn. Samtidigt tillåter visningsprogrammet växling av huvudresursen i körningsmiljön med hjälp av API:t `setAsset()`. Som utvecklare har du kontroll över hur visningsprogrammet hanterar miniatyrbildsområdet längst ned när den nya resursen bara har ett objekt. Det går att behålla den yttre visningsstorleken intakt och låta huvudvyn öka höjden och ta upp miniatyrbildområdet. Eller så kan du hålla storleken på huvudvyn statisk och komprimera det yttre visningsområdet, låta webbsidans innehåll röra sig uppåt och använda friskärmsutrymme från miniatyrbilderna.

   Om du vill behålla de yttre visningsprogramgränserna intakta definierar du storleken för den översta CSS-klassen `.s7zoomviewer` i absoluta enheter. Storleksändring i CSS kan placeras direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som senare tilldelas en förinställningspost för visningsprogrammet i Scene7 Publishing System eller skickas explicit med ett formatkommando.

   Mer information om hur du formaterar visningsprogrammet med CSS finns i [Anpassa zoomvisningsprogrammet](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Följande är ett exempel på hur du definierar en statisk storlek för ett externt visningsprogram på HTML-sidan:

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Du kan se beteendet med ett fast yttre visningsprogram i följande exempel. Observera att storleken på det yttre visningsprogrammet inte ändras när du växlar mellan uppsättningar:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   Om du vill göra huvudvyns dimensioner statiska definierar du visningsstorleken i absoluta enheter för den inre SDK-komponenten `Container` `.s7zoomviewer` CSS-väljaren eller genom att använda modifieraren `.s7container`.`stagesize`

   Följande är ett exempel på hur du definierar visningsstorleken för den inre SDK-komponenten `Container` så att huvudvisningsområdet inte ändrar dess storlek när du byter resurs:

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   På följande demosida visas visningsprogrammets beteende med en fast storlek för huvudvyn. Observera att när du växlar mellan uppsättningar förblir huvudvyn statisk och webbsidans innehåll flyttas lodrätt.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   Du kan ställa in modifieraren `stagesize` antingen i visningsprogrammets förinställningspost i Scene7 Publishing System, eller så kan du skicka den explicit med startkoden för visningsprogrammet med samlingen `params` eller som ett API-anrop enligt beskrivningen i kommandoreferensavsnittet i den här hjälpen, som i följande exempel:

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av klassen `s7viewers.ZoomViewer`, skickar all konfigurationsinformation till konstruktorn och anropar metoden `init()` för en visningsprograminstans.

   Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet ska åtminstone ha ett `containerId`-fält som innehåller namnet på visningsbehållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som visningsprogrammet stöder. I det här fallet måste `params`-objektet ha minst den URL för bildservrar som skickas som `serverUrl`-egenskap och den ursprungliga resursen som `asset`-parameter. Med det JSON-baserade initierings-API:t kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet anropar du metoden `init()` precis före den avslutande `BODY`-taggen eller på body-händelsen `onload()`.

   Samtidigt bör behållarelementet inte nödvändigtvis vara en del av webbsidans layout just nu. Det kan till exempel vara dolt med `display:none`-format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de lägsta nödvändiga konfigurationsalternativen till konstruktorn och anropar metoden `init()`. I det här exemplet antas `zoomViewer` vara visningsprograminstansen, `s7viewer` är namnet på platshållarens DIV, `http://s7d1.scene7.com/is/image/` är URL-adressen för bildservern och `Scene7SharedAssets/ImageSet-Views-Sample` är resursen.

   ```
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in Video Viewer med fast storlek:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsiv designinbäddning med obegränsad höjd {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets körningsstorlek `DIV`. I följande exempel antar du att webbsidan tillåter att visningsprogrammets behållare `DIV` tar 40 % av webbläsarfönstrets storlek, och låter dess höjd vara obegränsad. HTML-koden för webbsidan ser ut så här:

```
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

Att lägga till visningsprogrammet på en sådan sida liknar stegen för inbäddning med fast storlek. Den enda skillnaden är att du inte behöver definiera visningsprogrammets storlek explicit.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Skapa och initiera visningsprogrammet.

Alla steg ovan är desamma som med inbäddning med fast storlek. Lägg till behållar-DIV i befintlig `"holder"`-DIV. Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Bädda in i flexibel storlek med angiven bredd och höjd {#section-3674e6c032594441a6576b7fb1de6e64}

Vid flexibel inbäddning med bredd och höjd är webbsidans format annorlunda. Den ger båda storlekarna till DIV:n `"holder"` och centrerar den i webbläsarfönstret. Dessutom anger webbsidan storleken på elementen `HTML` och `BODY` till 100 procent.

```
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

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## Bädda in med set-based API {#section-44e014925f24418b900696003855c0a9}

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Om du använder den här API-konstruktorn används inga parametrar och konfigurationsparametrar anges med API-metoderna `setContainerId()`, `setParam()` och `setAsset()` med separata JavaScript-anrop.

I följande exempel visas hur du använder inbäddning med fast storlek med set-based API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```

