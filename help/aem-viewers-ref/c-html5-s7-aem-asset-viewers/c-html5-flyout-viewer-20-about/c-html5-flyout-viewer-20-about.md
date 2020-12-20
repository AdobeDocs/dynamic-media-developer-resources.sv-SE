---
description: Utfällbar visningsprogram är ett bildvisningsprogram. Den visar en statisk bild med den zoomade versionen som visas i den utfällbara vyn som en användare aktiverar. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den är utformad för att fungera på stationära datorer och mobila enheter.
keywords: responsive
seo-description: Utfällbar visningsprogram är ett bildvisningsprogram. Den visar en statisk bild med den zoomade versionen som visas i den utfällbara vyn som en användare aktiverar. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den är utformad för att fungera på stationära datorer och mobila enheter.
seo-title: Utfällbar
solution: Experience Manager
title: Utfällbar
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---


# Flyout{#flyout}

Utfällbar visningsprogram är ett bildvisningsprogram. Den visar en statisk bild med den zoomade versionen som visas i den utfällbara vyn som en användare aktiverar. Visningsprogrammet fungerar med bilduppsättningar och navigeringen görs med hjälp av färgrutor. Den är utformad för att fungera på stationära datorer och mobila enheter.

>[!NOTE]
>
>Bilder som använder IR (Image Rendering) eller UGC (User-Generated Content) stöds inte av det här visningsprogrammet.

Visningstypen är 504.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Använda utfällbar visningsprogram {#section-f21ac23d3f6449ad9765588d69584772}

Visningsprogrammet för utfällbara menyer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-uppsättning innehåller alla SDK-komponenter för visningsprogrammet som används av det här visningsprogrammet, resurser, CSS) som hämtats av visningsprogrammet under körning

Utfällbar visningsprogram är endast avsett för inbäddad användning, vilket betyder att det är integrerat i webbsidan med dokumenterad API. Det finns ingen produktionsklar webbsida för visningsprogrammet.

Konfigurationen och skalningen liknar den för andra visningsprogram. Du kan använda anpassad CSS för att använda skalning.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med visningsprogrammet för utfällbara appar {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Utfällbar visningsprogram har stöd för enkelberörings- och flerberöringsgester som är vanliga i andra mobilprogram.

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
   <td colname="col2"> <p> Aktiverar den utfällbara vyn eller ändringar mellan den primära och sekundära zoomnivån. </p> </td> 
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

## Bädda in utfällbar visningsprogram {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Webbsidan kan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter, eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för två primära åtgärdslägen: inbäddning i fast storlek och responsiv designinbäddning.

Inbäddningsläget med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här alternativet passar bäst för webbsidor som har en statisk sidlayout.

Inbäddningsläget för responsiv design förutsätter att visningsprogrammet kan behöva ändra storlek under körning som svar på storleksändringen för dess behållare `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

När du använder responsivt designinbäddningsläge med visningsprogrammet för utfällbara menyer måste du ange explicita brytpunkter för huvudvisningsbilden med parametern `imagereload`. Bäst är att du matchar brytpunkterna med brytpunkterna för visningsprogrammets bredd enligt CSS-reglerna för webbsidor.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur en webbsida ändrar sin behållare `DIV`. Om webbsidan bara anger bredden på behållaren `DIV`, och dess höjd inte begränsas, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den resurs som används. Det innebär att resursen passar in perfekt i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor där responsiva designlayoutramverk som Bootstrap, Foundation och så vidare används.

Om webbsidan ställer in både bredd och höjd för visningsprogrammets behållare `DIV` fyller visningsprogrammet bara det området och följer den storlek som anges i webbsidans layout. Ett bra exempel på hur du kan använda det här är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i HTML-huvudet. Innan du kan använda visningsprogrammets API måste du ta med `FlyoutViewer.js`. `FlyoutViewer.js` finns i följande  [!DNL html5/js/] undermapp i din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Scene7-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Scene7-servrarna som har IS-Viewer installerat.

En relativ sökväg ser ut så här:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Du bör bara referera till JavaScript-filen `include` för huvudvisningsprogrammet på sidan. Du bör inte referera till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körningen. Referera inte direkt till HTML5 SDK `Utils.js`-biblioteket som läses in av visningsprogrammet från kontextsökvägen `/s7viewers` (s.k. konsoliderad SDK `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversioner. Adobe sparar inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att om du skickar en direkt referens till ett sekundärt JavaScript `include` som används av visningsprogrammet på sidan så bryts visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID senare skickas till visningsprogrammets API.

   Platshållarens DIV är ett positionerat element, vilket innebär att CSS-egenskapen `position` är inställd på `relative` eller `absolute`.

   Det är webbsidans ansvar att ange rätt `z-index` för platshållarens DIV-element. Om du gör det ser du till att visningsprogrammets utfällbara del visas ovanpå de andra webbsidelementen.

   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Anger visningsprogrammets storlek.

   I det här visningsprogrammet visas miniatyrer när du arbetar med uppsättningar med flera objekt. På stationära datorer placeras miniatyrbilder under huvudvyn. Samtidigt tillåter visningsprogrammet växling av huvudresursen under körning med hjälp av API:t `setAsset()`. Som utvecklare har du kontroll över hur visningsprogrammet hanterar miniatyrbildsområdet i det nedre området när den nya resursen bara har ett objekt. Det går att behålla den yttre visningsstorleken intakt och låta huvudvyn öka höjden och uppta miniatyrområdet. Eller så kan du hålla storleken på huvudvyn statisk och komprimera det yttre visningsområdet, vilket gör att webbsidans innehåll kan flyttas upp och sedan använda det lediga utrymmet från miniatyrbilderna.

   Om du vill behålla de yttre gränserna för visningsprogrammet intakt definierar du storleken för den översta CSS-klassen `.s7flyoutviewer` i absoluta enheter. Storleksändring i CSS kan placeras direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som senare tilldelas en förinställningspost för visningsprogrammet i Scene7 Publishing System, eller skickas explicit med style-kommando.

   Mer information om hur du formaterar visningsprogrammet med CSS finns i [Anpassa visningsprogrammet för utfällbara användare](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451).

   Följande är ett exempel på hur du definierar den statiska storleken på det yttre visningsprogrammet på en HTML-sida:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Du kan se beteendet med ett fast yttre visningsområde på följande exempelsida. Observera att storleken på det yttre visningsprogrammet inte ändras när du växlar mellan uppsättningar:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   Om du vill göra huvudvyns dimensioner statiska definierar du visningsstorleken i absoluta enheter för den inre `Container` SDK-komponenten med hjälp av CSS-väljaren `.s7flyoutviewer .s7container`. Dessutom bör du åsidosätta den fasta storlek som är definierad för CSS-klassen `.s7flyoutviewer` på den översta nivån i standardvisningsprogrammets CSS genom att ange den till `auto`.

   Följande är ett exempel på hur du definierar visningsstorleken för den inre SDK-komponenten `Container` så att huvudvisningsområdet inte ändrar dess storlek när du byter resurs:

   ```
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

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Observera också att CSS för standardvisningsprogrammet har en fast storlek för det yttre området som är färdigt att användas.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av klassen `s7viewers.FlyoutViewer`, skickar all konfigurationsinformation till konstruktorn och anropar metoden `init()` för en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet ska åtminstone ha fältet `containerId` som innehåller namnet på visningsbehållar-ID och kapslat JSON-objekt `params` med konfigurationsparametrar som visningsprogrammet stöder. I det här fallet måste `params`-objektet ha minst den URL för bildservrar som skickas som `serverUrl`-egenskap och den ursprungliga resursen som `asset`-parameter. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet anropar du metoden `init()` precis före den avslutande `BODY`-taggen eller på body-händelsen `onload()`.

   Samtidigt bör behållarelementet inte nödvändigtvis vara en del av webbsidans layout just nu. Det kan till exempel vara dolt med `display:none`-format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När detta inträffar återgår visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar metoden `init()`. Exemplet förutsätter att `flyoutViewer` är visningsprograminstansen; `s7viewer` är namnet på platshållaren `DIV`; `http://s7d1.scene7.com/is/image/` är webbadressen för bildservrar; och `Scene7SharedAssets/ImageSet-Views-Sample` är resursen:

   ```
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in visningsprogrammet med fast storlek:

   ```
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
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
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

## Responsiv designinbäddning med obegränsad höjd {#section-056cb574713c4d07be6d07cf3c598839}

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

Att lägga till visningsprogrammet på en sådan sida liknar stegen för inbäddning med fast storlek. Den enda skillnaden är att du måste åsidosätta den fasta storleken från CSS för standardvisningsprogrammet med den storlek som anges i relativa enheter.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

Alla stegen ovan är desamma som med inbäddning med fast storlek med följande tre undantag:

* lägg till behållaren `DIV` i den befintliga &quot;hållaren&quot; `DIV`;
* lade till parametern `imagereload` med explicita brytpunkter;
* I stället för att ange en fast visningsstorlek med absoluta enheter används CSS som anger visningsprogrammets bredd och höjd till 100 % enligt följande:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```
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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Flexibel storleksinbäddning med definierad bredd och höjd {#section-0a329016f9414d199039776645c693de}

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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Inbäddning med Setter-baserad API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Om du använder den här API-konstruktorn används inga parametrar och konfigurationsparametrar anges med API-metoderna `setContainerId()`, `setParam()` och `setAsset()` med separata JavaScript-anrop.

I följande exempel visas hur du använder inbäddning med fast storlek med set-based API:

```
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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

