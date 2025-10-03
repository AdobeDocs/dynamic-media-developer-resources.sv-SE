---
title: Panoramavisningsprogram
description: HTML5 Panoramavy Viewer är ett bildvisningsprogram som visar en panoramabild. Syftet med det här visningsprogrammet är att visa ett sfäriskt panorama, även kallat ekvirektangulär bild. Det har stöd för automatisk panorering och panorering med gyroskopisk rörelse. Den är utformad för att fungera på stationära datorer och mobila enheter. Visningsläget Virtuell verklighet är tillgängligt på mobila enheter med stöd för detta.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '1916'
ht-degree: 0%

---

# Panorama{#panoramic}

HTML5 Panoramavy Viewer är ett bildvisningsprogram som visar en panoramabild. Syftet med det här visningsprogrammet är att visa ett sfäriskt panorama, även kallat ekvirektangulär bild. Det har stöd för automatisk panorering och panorering med gyroskopisk rörelse. Den är utformad för att fungera på stationära datorer och mobila enheter. Visningsläget Virtuell verklighet är tillgängligt på mobila enheter med stöd för detta.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Visningstyp 514.

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)
-->

## Använda panoramavisningsprogram {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramavy Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler som hämtats av visningsprogrammet under körning. Hjälpfilerna är en enda JavaScript-uppsättning med alla HTML5 Viewer SDK-komponenter som används av just detta visningsprogram, resurser, CSS.
HTML5 Panoramavy Viewer kan användas både i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer eller i inbäddat läge, där den integreras med målwebbsidan med dokumenterat API.
Konfigurationen och skalningen liknar den för andra visningsprogram i HTML5. All skalning kan göras med anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med HTML5 Panoramic Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramic Viewer har stöd för automatisk panorering och navigering genom att dra eller gyroskopisk rörelse.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navigering </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Skrivbord </p> </td> 
   <td colname="col2"> <p>Navigera genom att panorera och dra automatiskt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pekenhet </p> </td> 
   <td colname="col2"> <p>Panorera och dra automatiskt för att navigera som standard. Navigera genom gyroskopisk rörelse i VR-renderingsläge (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

Visningsprogrammet har stöd för både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.
Panoramaviseringsprogrammet kan återge panoramabilder i VR-läge (Virtual Reality) genom att ange renderingsmodifieraren. När återgivning är aktiverat visas en panoramabild i delade skärmar. Ett vanligt användningsexempel är att placera bilden i en mobiltelefon som är monterad i ett virtuellt verklighetshuvud och ger separata bilder för varje öga. Visningsprogrammet svarar på huvudets gyroskopiska rörelser och navigerar genom bilden.

## Bädda in HTML5 Panoramavisningsprogram {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland ger en webbsida en länk. Om du väljer den länken öppnas visningsprogrammet i ett separat webbläsarfönster. I andra fall kan det vara nödvändigt att bädda in visningsprogrammet på värdsidan. I det senare fallet kan webbsidan ha en statisk layout eller vara&quot;responsiv&quot; och visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup, inbäddning med fast storlek och responsiv inbäddning.

**Om popup-läge**

I popup-läget öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändras eller om enhetens orientering ändras.

Det här läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med `window.open()` JavaScript-anrop, ett korrekt konfigurerat HTML-element eller något annat lämpligt sätt.

Vi rekommenderar att du använder en färdig HTML-sida för popup-läge. Den kallas [!DNL PanoramicViewer.html] och finns under undermappen [!DNL html5/] i din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

Visuell anpassning kan uppnås genom att använda anpassad CSS.

Här är ett exempel på HTML-kod som öppnar visningsprogrammet i det nya fönstret:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt inbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet upptar normalt bara en del av webbsidans fastigheter.

De viktigaste användningsområdena är webbsidor som är inriktade på datorer eller surfplattor, och även responsiva webbsidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Den här metoden är det bästa alternativet för webbsidor med statisk layout.

Responsiv inbäddning förutsätter att visningsprogrammet måste ändra storlek vid körning som svar på storleksändringen för dess behållar-DIV. Det vanligaste användningsområdet är att lägga till visningsprogram på en webbsida som använder flexibel layout.

I svarsläge beter sig visningsprogrammet olika beroende på hur webbsidan ändrar dess behållar-DIV. Om webbsidan bara anger bredden på behållar-DIV, och dess höjd inte begränsas, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den använda resursen. Den här metoden ser till att resursen passar in perfekt i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor som använder responsiva layoutramverk som Bootstrap, Foundation och liknande.

Om webbsidan ställer in både bredd och höjd för visningsprogrammets behållar-DIV fyller visningsprogrammet i området och följer den storlek som anges i webbsidans layout. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till visningsprogrammets JavaScript-fil på webbsidan.
1. Definierar behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till visningsprogrammets JavaScript-fil på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i HTML head. Innan du kan använda visningsprogrammets API måste du ta med [!DNL PanoramicViewer.js]. Filen [!DNL PanoramicViewer.js] finns under undermappen [!DNL html5/js/] i din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Relativ sökväg ser ut så här:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Referera bara till JavaScript `include`-huvudvisningsfilen på din sida. Referera inte till några andra JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körning. Referera inte direkt till HTML5 SDK `Utils.js`-biblioteket som läses in av visningsprogrammet från `/s7viewers`-kontextsökvägen (så kallad konsoliderad SDK `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversioner. Adobe sparar inte äldre versioner av det sekundära visningsprogrammet `includes` på servern.
>
>
>Det innebär att om du skickar en direkt referens till eventuella sekundära JavaScript `include` som används av visningsprogrammet på sidan så bryts visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API. DIV har den storlek som anges via CSS.

   Platshållarens DIV är ett placerat element, vilket innebär att CSS-egenskapen `position` är inställd på `relative` eller `absolute`.


   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att antingen deklarera den för CSS-klassen `.s7panoramicviewer` på den översta nivån i absoluta enheter eller genom att använda modifieraren `stagesize`.

   Storleksändring i CSS kan placeras direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som senare tilldelas en förinställningspost för visningsprogrammet i AOD eller skickas explicit med formatkommando. Mer information om hur du formaterar visningsprogrammet med CSS finns i Anpassa visningsprogrammet. Nedan visas ett exempel på hur du definierar statisk visningsstorlek på HTML-sidan:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize`-modifieraren kan skickas explicit med visarinitieringskoden med parametersamlingen eller som ett API-anrop enligt beskrivningen i kommandoreferensavsnittet, så här:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av klassen `s7viewers.PanoramicViewer`, skickar all konfigurationsinformation till konstruktorn och anropar metoden `init(` i en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet ska åtminstone ha fältet containerId som innehåller namnet på visningsbehållar-ID och kapslade parametrar-JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet. I det här fallet måste parameterobjektet ha minst en URL för bildservrar som skickas som egenskapen `serverUrl` och den ursprungliga resursparametern. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet anropar du metoden `init()` precis före den avslutande `BODY` -taggen eller på body `onload()` -händelsen.

   Samtidigt behöver behållarelementet inte nödvändigtvis vara en del av webbsidans layout ännu. Den kan till exempel vara dold med formatet `display:none` som tilldelats den. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När den här åtgärden utförs återtas visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar nödvändiga minimikonfigurationsalternativ till konstruktorn och anropar metoden `init()`. I det här exemplet antas `panoramicViewer` vara visningsprograminstansen, `s7viewer` är namnet på platshållaren `DIV`, [!DNL http://s7d1.scene7.com/is/image/] är URL:en för bildvisning och [!DNL Scene7SharedAssets/PanoramicImage-Sample] är resursen.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in panoramavisningsprogrammet med fast storlek:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**Responsiv designinbäddning med obegränsad höjd**

Med den responsiva inbäddningen har webbsidan vanligtvis någon typ av flexibel layout som bestämmer körningsstorleken för visningsprogrammets behållar-DIV. I det här exemplet antar vi att webbsidan tillåter att visningsprogrammets behållare-DIV tar 80 % av webbläsarens fönsterstorlek och låter dess höjd vara obegränsad. Webbsidan med HTML-koden kan se ut så här:

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

Att lägga till visningsprogrammet på en sådan sida liknar inbäddningen av fast storlek, med den enda skillnaden att du inte behöver definiera visningsprogrammets storlek explicit:

1. Lägga till visningsprogrammets JavaScript-fil på webbsidan.
1. Definierar behållar-DIV.
1. Skapa och initiera visningsprogrammet.

Alla steg ovan är desamma som med inbäddning med fast storlek. Behållar-DIV bör läggas till i den befintliga DIV:n för &quot;hållare&quot;. Följande kod är ett fullständigt exempel på hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

Följande exempelsida visar hur responsiv designinbäddning med obegränsad höjd används i verkligheten:

[Live-demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

-->

**Responsiv designinbäddning med bredd och höjd definierad**

Om det finns responsiv designinbäddning med bredd och höjd definierad, är webbsidans format annorlunda. Det ger både storlekar för &quot; hållaren&quot; `DIV` och centrerar den i webbläsarfönstret. Webbsidan anger också storleken på elementen `HTML` och `BODY` till 100 %:

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

Resten av inbäddningsstegen är identiska med responsiv inbäddning med obegränsad höjd. Resultatet är

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Inbäddning med Setter-baserat API**

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Med detta API tar konstruktorn inga parametrar och konfigurationsparametrar anges med API-metoderna `setContainerId()`, `setParam()` och `setAsset()` med separata JavaScript-anrop.

I följande exempel visas inbäddning med fast storlek med set-based API:

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
    width: 1024;
    height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
