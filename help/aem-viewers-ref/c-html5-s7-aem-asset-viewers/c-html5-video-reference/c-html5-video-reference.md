---
title: Video
description: Video Viewer är en videospelare som spelar upp strömmande och progressiv video som är kodad i H.264-format. Den levereras från Dynamic Media Classic eller Adobe Experience Manager med Dynamic Media.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2368'
ht-degree: 0%

---

# Video{#video}

Video Viewer är en videospelare som spelar upp strömmande och progressiv video som är kodad i H.264-format. Den levereras från Dynamic Media Classic eller Experience Manager med Dynamic Media.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Både en video och adaptiva videouppsättningar stöds. Dessutom har visningsprogrammet stöd för arbete med progressiv video och HLS-strömmar på externa platser. Det är utformat för att fungera både på stationära och mobila webbläsare som stöder HTML5-video. Det här visningsprogrammet har även stöd för valfria undertexter som visas ovanpå videoinnehåll, videokapitelnavigering och verktyg för delning via sociala medier.

I Video Viewer används direktuppspelad HTML5-videouppspelning i HLS-format i standardkonfigurationen när det underliggande systemet stöder det. På system som saknar stöd för direktuppspelning från HTML5 återgår visningsprogrammet till progressiv videoleverans i HTML5.

Visningstyp 506.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Använda Video Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Video Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler - en enda JavaScript-fil innehåller alla SDK-komponenter för visningsprogrammet som används av det här visningsprogrammet, resurser och CSS-kod som hämtats av visningsprogrammet under körning.

Du kan använda videovisningsprogrammet i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer. Du kan också använda visningsprogrammet i inbäddat läge, där det är integrerat i en målwebbsida med hjälp av det dokumenterade API:t.

Konfigurationen och skalningen av visningsprogrammet liknar de andra visningsprogrammen. All skalning görs med anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med Video Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Video Viewer innehåller en uppsättning standardkontroller för användargränssnitt för videouppspelning, t.ex. en knapp för uppspelning/paus, en tidsbubbla för videouppspelning, en indikator för uppspelningstid/total tid, volymkontroll, helskärmsknapp och växling för stängd bildtext. Alla dessa kontroller grupperas i ett kontrollfält längst ned i visningsprogrammets användargränssnitt.

På enheter med pekskärm döljs volymkontrollen från användargränssnittet eftersom det bara är möjligt att styra volymen med maskinvaruknapparna.

När visningsprogrammet körs i popup-läge är knappen för helskärmsläge inte tillgänglig i användargränssnittet.

Det går att navigera snabbt i innehållet i en video när videokapitlet är aktiverat. Videokameror visas som markörer i videonavigeringsspåret och kapiteltiteln och tillhörande beskrivning visas när du för musen över eller med en enda tryckning på pekskärmssystem. Användarna kan söka efter ett visst kapitel genom att markera en kapitelmarkör eller välja kapitelbeskrivningsbubblan.

Visningsprogrammet stöder både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Visningsprogrammet är fullt åtkomligt via tangentbordet.

Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Delningsverktyg för sociala medier med Video Viewer {#section-907d316fe1da4b87abb9775f02464704}

Video Viewer har stöd för verktyg för delning via sociala medier. De är tillgängliga som en enda knapp i användargränssnittet, som utökas till ett delat verktygsfält när användaren klickar eller trycker på det.

Verktygsfältet för delning innehåller en ikon för varje typ av delningskanal som stöds, till exempel Facebook, Twitter, e-postdelning, inbäddning av koddelning och länkdelning. När verktygen för e-postdelning, inbäddning eller länkdelning är aktiverade visas en modal dialogruta med ett motsvarande inmatningsformulär. När Facebook eller Twitter anropas omdirigeras användaren till en standarddelningsdialogruta från en tjänst för sociala medier. När ett delningsverktyg aktiveras pausas videouppspelningen automatiskt.

Delningsverktygen är inte tillgängliga i helskärmsläge på grund av säkerhetsbegränsningar i webbläsaren.

## Bädda in Video Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en länk som när den är markerad öppnar visningsprogrammet i ett separat webbläsarfönster. I andra fall är det nödvändigt att bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup, inbäddning med fast storlek och responsiv designinbäddning.

Det går att bädda in flera videor på samma sida på både surfplattor och mobila enheter. Vanligtvis kan du bara spela upp en video i taget. När en användare börjar spela upp en video och sedan försöker spela upp en annan, pausas den första videon automatiskt. Videon som pausades automatiskt kommer ihåg den aktuella uppspelningstiden, så att användaren alltid kan återgå till den och återuppta uppspelningen. Det enda undantaget som den här regeln gäller är webbläsaren Chrome på Android™ 4.x-enheter, som kan spela upp videor parallellt.

**Om popup-läge**

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändrar storlek eller enhetens orientering ändras.

Det här läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med `window.open()` JavaScript-anrop, korrekt konfigurerat `A` HTML-element eller någon annan lämplig metod.

Vi rekommenderar att du använder en HTML-sida som inte finns i kartongen för popup-åtgärder. Den kallas [!DNL VideoViewer.html] och den finns under [!DNL html5/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Du kan anpassa visuellt genom att använda anpassad CSS.

Här följer ett exempel på HTML som öppnar visningsprogrammet i ett nytt fönster:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt inbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet upptar normalt bara en del av webbsidans fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designsidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här alternativet är bäst för webbsidor som har en statisk sidlayout.

Inbäddning av responsiv design förutsätter att visningsprogrammet måste ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till visningsprogrammet på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`, utan att begränsa höjden, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den resurs som används. Den här metoden ser till att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor som använder ett responsivt designlayoutramverk som Bootstrap eller Foundation.

I annat fall, om webbsidan anger både bredd och höjd för visningsprogrammets behållare `DIV`, fyller visningsprogrammet bara det området och följer den storlek som anges i webbsidans layout. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter storleken på webbläsarfönstret.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definiera behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i huvudet HTML. Innan du kan använda visningsprogrammets API måste du se till att du inkluderar [!DNL FlyoutViewer.js]. The [!DNL FlyoutViewer.js] filen finns under [!DNL html5/js/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Relativ sökväg ser ut så här:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Referera endast till JavaScript för huvudvisningsprogrammet `include` på sidan. Referera inte till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körning. Ange särskilt inte direkt HTML5 SDK `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökväg (så kallad konsoliderad SDK) `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversionerna. Adobe har inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att du skickar en direkt referens till valfritt sekundärt JavaScript `include` som används av visningsprogrammet på sidan avbryter visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API. DIV har den storlek som anges via CSS.

   Platshållarens DIV är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   Kontrollera att helskärmsfunktionen fungerar som den ska i Internet Explorer. Kontrollera att det inte finns några andra element i DOM som har en högre staplingsordning än DIV:n för platshållaren.

   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att deklarera det för `.s7videoviewer` CSS-klass på översta nivån i absoluta enheter, eller med modifieraren `stagesize`.

   Du kan placera storleken i CSS direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet. Den tilldelas senare till en post för visningsförinställningar i Dynamic Media Classic eller skickas explicit med ett formatkommando.

   Se [Anpassa Video Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) om du vill ha mer information om hur du formaterar visningsprogrammet med CSS.

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på en HTML-sida:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Du kan ange `stagesize` modifiera antingen i posten för visningsförinställning i Dynamic Media Classic, eller skicka den explicit med startkoden för visningsprogrammet med `params` samling. Eller som ett API-anrop enligt beskrivningen i kommandoreferensavsnittet, som i följande:

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.VideoViewer` -klass, skicka all konfigurationsinformation till konstruktorn och anropa `init()` -metod i en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Objektet bör åtminstone ha `containerId` fält som innehåller namnet på visningsprogrammets behållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet. I detta fall `params` objektet måste ha minst URL för bildserver som skickas som `serverUrl` egenskap, webbadress för videoserver skickad som `videoserverurl` och den ursprungliga tillgången som `asset` parameter. Med det JSON-baserade initierings-API:t kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet, ring `init()` metod precis före stängning `BODY` eller på brödtexten `onload()` -händelse.

   Samtidigt behöver behållarelementet inte nödvändigtvis vara en del av webbsidans layout ännu. Den kan till exempel vara dold med `display:none` format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När den här åtgärden utförs återtas visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar nödvändiga minimikonfigurationsalternativ till konstruktorn och anropar `init()` -metod. Det här exemplet förutsätter `videoViewer` är visningsprograminstansen, `s7viewer` är namnet på platshållaren `DIV`, [!DNL http://s7d1.scene7.com/is/image/] är webbadressen till bildservern, [!DNL http://s7d1.scene7.com/is/content/] är webbadressen till videoservern, och [!DNL Scene7SharedAssets/Glacier_Climber_MP4] är tillgången.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in Video Viewer med fast storlek:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Responsiv designinbäddning med obegränsad höjd**

Med den responsiva designinbäddningen har webbsidan vanligtvis någon typ av flexibel layout på plats som bestämmer körningsstorleken för visningsprogrammets behållare `DIV`. I det här exemplet antar du att webbsidan tillåter visningsprogrammets behållare `DIV` för att ta 40 % av webbläsarens fönsterstorlek och låta dess höjd vara obegränsad. Webbsidans HTML-kod ser ut så här:

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

Att lägga till visningsprogrammet på en sådan sida liknar inbäddning med fast storlek. Den enda skillnaden är att du inte behöver definiera visningsprogrammets storlek explicit.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Skapa och initiera visningsprogrammet.

Alla steg ovan är desamma som med inbäddning med fast storlek. Lägg till behållare `DIV` till den befintliga &quot; innehavaren&quot; `DIV`. Följande kod är ett komplett exempel. Du kan se hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

Följande exempelsida visar hur responsiv designinbäddning med obegränsad höjd används i verkligheten:

[Direktdemonstrationer](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativ demoplats](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsiv design embedding with width and height defined**

Om det finns responsiv designinbäddning med definierad bredd och höjd är webbsidans format annorlunda. Det ger &quot; hållaren&quot; båda storlekar `DIV` och centrera det i webbläsarfönstret. Dessutom anger webbsidan storleken på `HTML` och `BODY` till 100 %:

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

De återstående inbäddningsstegen är identiska med responsiv designinbäddning med obegränsad höjd. Följande exempel visas:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Bädda in med Setter-baserat API**

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Med detta API tar konstruktorn inga parametrar och konfigurationsparametrar anges med `setContainerId()`, `setParam()`och `setAsset()` API-metoder med separata JavaScript-anrop.

I följande exempel visas inbäddning med fast storlek med set-based API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
