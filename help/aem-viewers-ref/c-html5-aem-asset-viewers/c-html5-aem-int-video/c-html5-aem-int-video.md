---
title: Interaktiv video
description: Interactive Video Viewer är en videospelare som spelar upp strömmande och progressiv video som är kodad i H.264-format.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 0%

---

# Interaktiv video{#interactive-video}

Interactive Video Viewer är en videospelare som spelar upp strömmande och progressiv video som är kodad i H.264-format.

Visningsprogrammet visar även interaktiva produktfärgrutor bredvid videoinnehållet. Både en video och adaptiva videouppsättningar stöds. Det är utformat för att fungera både på stationära och mobila webbläsare som stöder HTML5-video. Visningsprogrammet har stöd för valfria undertexter som visas ovanpå videoinnehåll, videokapitelnavigering och verktyg för delning via sociala medier. Syftet med det här visningsprogrammet är att hjälpa dig att implementera en videoupplevelse som kan köpas. Det innebär att användare kan välja en färgruta som är kopplad till en viss videotidsregion och omdirigeras till en snabbvy eller produktinformationssida på kundens webbplats.

Visningstypen är 510.

## Demo-URL:er {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

Och

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## Systemkrav {#section-b7270cc4290043399681dc504f043609}

Se [Systemkrav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Använda Interactive Video Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Interactive Video Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler som hämtats av visningsprogrammet under körning. Ett enda JavaScript ingår i alla Viewer SDK-komponenter som används av just detta visningsprogram, resurser och CSS.

Interactive Video Viewer kan användas i popup-läge med en produktionsklar HTML-sida som finns i Image Serving Viewer. Den kan också användas i inbäddat läge, där den integreras med målwebbsidan med det dokumenterade API:t.

Konfigurering och skalning liknar de andra visningsprogrammen som beskrivs i den här handboken. All skalning görs med CSS (Cascading Style Sheets).

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med Interactive Video Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Interactive Video Viewer innehåller en uppsättning standardkontroller för användargränssnitt för videouppspelning, t.ex. en Play/Pause-knapp, videobubblor, tidsbubbla för video, indikator för uppspelningstid/total tid, volymkontroll, helskärmsknapp och växling för stängd bildtext. Alla dessa kontroller grupperas i ett kontrollfält direkt under huvudvyn.

På enheter med pekskärm döljs volymkontrollen från användargränssnittet, eftersom det bara är möjligt att styra volymen med enhetens maskinvaruknappar.

När visningsprogrammet körs i popup-läge är knappen för helskärm inte tillgänglig i användargränssnittet.

Visningsprogrammet visar en panel med interaktiva färgrutor till höger om videovisningsområdet. Listan med färgrutor visas automatiskt när videon spelas upp, så att färgrutor som motsvarar det aktuella videoområdet visas. Om du klickar eller trycker på en färgruta utlöses en åtgärd som var kopplad till den färgrutan under redigeringstiden. Beroende på hur du ställer in den kan utlösaren dirigeras om till en annan sida på webbplatsen. Det kan också skicka produktinformation tillbaka till webbsidans logik, som i sin tur kan utlösa att en snabbvy öppnas som visar relaterat produktinnehåll.

Du kan snabbt navigera i videoinnehållet när videokapitlet är aktiverat. Videokameror visas som markörer i videonavigeringsspåret och kapiteltiteln och beskrivningen visas vid överrullning (eller på pekskärmar). Kunden kan söka efter ett visst kapitel genom att klicka på en kapitelmarkör eller trycka på en kapitelbeskrivningsbubbla.

Visningsprogrammet har också stöd för olika verktyg för delning av sociala medier. De är tillgängliga som en enda knapp i användargränssnittet, som utökas till ett delat verktygsfält när användaren klickar eller trycker på det. Verktygsfältet för delning innehåller en ikon för varje typ av delningskanal som stöds, till exempel Facebook, Twitter, e-postdelning, inbäddning av koddelning och länkdelning. När verktygen för e-postdelning, inbäddning eller länkdelning är aktiverade visas en modal dialogruta med ett motsvarande inmatningsformulär. När Facebook eller Twitter anropas omdirigeras användaren till en standarddelningsdialogruta från en tjänst för sociala medier. Dessutom pausas videouppspelningen automatiskt när ett delningsverktyg aktiveras. Delningsverktygen är inte tillgängliga i helskärmsläge på grund av säkerhetsbegränsningar i webbläsaren.

Visningsprogrammet är fullt åtkomligt via tangentbordet. Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in interaktiv videovisare {#section-6bb5d3c502544ad18a58eafe12a13435}

Interaktiv Video Viewer är inbäddad på värdsidan. En sådan webbsida kan ha en statisk layout eller vara&quot;responsiv&quot; och visas på olika enheter eller för olika webbläsarfönsterstorlekar.

För att tillgodose dessa behov har visningsprogrammet stöd för två primära åtgärdslägen: inbäddning i fast storlek och responsiv inbäddning.

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet tar normalt bara upp en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designade sidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Den här funktionen är det bästa alternativet för webbsidor som har en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet måste ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`, utan att begränsa höjden, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den resurs som används. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor med flexibla ramverk för webbdesign som Bootstrap och Foundation.

I annat fall, om webbsidan anger både bredd och höjd för visningsprogrammets behållare `DIV`, fyller visningsprogrammet bara det området och följer den storlek som webbsidans layout ger. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definiera behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i huvudet HTML. Innan du kan använda visningsprogrammets API måste du se till att du inkluderar [!DNL InterativeVideoViewer.js]. The [!DNL InteractiveVideoViewer.js] filen finns under [!DNL html5/js/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Referera endast till JavaScript för huvudvisningsprogrammet `include` på sidan. Referera inte till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körning. Ange särskilt inte direkt HTML5 SDK `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökväg (så kallad konsoliderad SDK) `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversionerna. Adobe har inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att du skickar en direkt referens till valfritt sekundärt JavaScript `include` som används av visningsprogrammet på sidan avbryter visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definiera behållaren `DIV`.

   Lägg till en tom `DIV` -element till sidan där du vill att visningsprogrammet ska visas. The `DIV` -elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API. DIV har den storlek som anges via CSS.

   Platshållaren `DIV` är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   För att helskärmsfunktionen ska fungera i Internet Explorer måste du kontrollera att det inte finns några andra element i DOM som har en högre staplingsordning än platshållaren `DIV`.

   Följande är ett exempel på en definierad platshållare `DIV` element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att deklarera det för `.s7interactivevideoviewer` CSS-klass på översta nivån i absoluta enheter, eller med `stagesize` modifierare.

   Du kan ange storlek i CSS direkt på HTML-sidan. Eller så kan du lägga in den i en anpassad CSS-fil för visningsprogrammet, som sedan tilldelas till en post för visningsförinställningar i Adobe Experience Manager Assets - On demand, eller skickas explicit med `style` -kommando.

   Se [Anpassa Interactive Video Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) om du vill ha mer information om hur du formaterar visningsprogrammet med CSS.

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på HTML-sidan:

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Du kan ange `stagesize` modifierare i posten för visningsförinställning i Experience Manager Assets - On-demand. Eller så kan du skicka det explicit med visarens initieringskod med `params` samling, eller som ett API-anrop enligt beskrivningen i avsnittet Kommandoreferens, så här:

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.InteractiveVideoViewer` -klass, skicka all konfigurationsinformation till konstruktorn och anropa `init()` -metod i en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Objektet bör åtminstone ha `containerId` fält som innehåller namnet på visningsprogrammets behållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet.

   I det här fallet `params` objektet måste ha minst URL för bildserver som skickas som `serverUrl` och den ursprungliga tillgången som `asset` parameter. Med det JSON-baserade initierings-API:t kan du skapa och starta visningsprogrammet med en enda kodrad, en webbadress för videoservern som skickas som `videoserverurl` egenskap, ursprunglig tillgång som `asset` och interaktiva data som `interactivedata` -egenskap. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet, ring `init()` metod precis före stängning `BODY` eller på brödtexten `onload()` -händelse.

   Dessutom är behållarelementet inte nödvändigtvis en del av webbsidans layout ännu. Den kan till exempel vara dold med `display:none` format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. Det som händer gör att visningsprogrammet laddas igen automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar `init()` -metod. Exemplet förutsätter följande:

   * Visningsprograminstansen är `interactiveVideoViewer`.
   * Platshållarens namn `DIV` är `s7viewer`.
   * URL för bildservrar är `https://aodmarketingna.assetsadobe.com/is/image/`.
   * Videoserverns URL är `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * Innehålls-URL är `https://aodmarketingna.assetsadobe.com/`.
   * Tillgången är `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Interaktiva data är `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in den interaktiva videovisaren med fast storlek:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsiv designinbäddning med obegränsad höjd**

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

Att lägga till visningsprogrammet på en sådan sida liknar stegen för inbäddning med fast storlek. Den enda skillnaden är att du inte behöver definiera visningsprogrammets storlek explicit.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Skapa och initiera visningsprogrammet.

Alla steg ovan är desamma som med inbäddning med fast storlek. Lägg till behållar-DIV till befintlig `"holder"` DIV. Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[Direktdemonstrationer](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativ demoplats](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsiv inbäddning med definierad bredd och höjd**

Om det finns responsiv inbäddning med bredd och höjd definierad är webbsidans format annorlunda. Det ger båda storlekarna till `"holder"` DIV och centrera det i webbläsarfönstret. Dessutom anger webbsidan storleken på `HTML` och `BODY` -element till 100 procent.

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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
