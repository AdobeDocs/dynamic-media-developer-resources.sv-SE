---
title: Video360
description: HTML5 Video360 Viewer är en 360-graders videospelare som spelar upp strömning och progressiv 360-video som är kodad i H.264-format, som levereras från Dynamic Media Classic eller Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# Video360{#video}

HTML5 Video360 Viewer är en 360-graders videospelare som spelar upp strömning och progressiv 360-video som är kodad i H.264-format, som levereras från Dynamic Media Classic eller Adobe Experience Manager, Dynamic Media.

360-gradersvideor, även kallade engagerande videor eller sfäriska videor, är videoinspelningar där en vy i alla riktningar spelas in samtidigt och spelas in med en dubbelriktad kamera eller en samling kameror. Både en video och adaptiva videouppsättningar stöds. Visningsprogrammet har också stöd för arbete med progressiv video och HLS-strömmar på en extern plats.

Rekommenderade proportioner för 360-video är 2:1. Spatial ljud stöds inte. Visningsprogrammet är utformat för att endast fungera med 360-video. Om du försöker spela upp en video som inte är 360 resulterar det i förvrängd videouppspelning.

Visningsprogrammet är utformat för att fungera både i webbläsare för datorer och mobila enheter med stöd för HTML5-video. Visningsprogrammet har stöd för valfria verktyg för delning via sociala medier.

Visningsprogrammet Video360 använder direktuppspelad videouppspelning i HLS-format i HTML5-format i standardkonfigurationen när det underliggande systemet stöder det. På system som saknar stöd för direktuppspelning från HTML5 återgår visningsprogrammet till progressiv videoleverans i HTML5.

Visningstypen är 517.

## Demo-URL:er {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Systemkrav {#section-b7270cc4290043399681dc504f043609}

Se [Systemkrav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Använda Video360 Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-fil innehåller alla HTML5 Viewer SDK-komponenter som används av detta visningsprogram, resurser och CSS) som hämtats av visningsprogrammet under körning.

HTML5 Video360 Viewer kan användas både i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer eller i inbäddat läge, där den integreras med målwebbsidan med hjälp av dokumenterad API.

Konfigurationen och skalningen liknar den för andra visningsprogram som beskrivs i den här handboken. All skalning görs med CSS (Cascading Style Sheets).

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360-videoinnehåll kräver högre kodningsinställningar än standardvideo som inte är 360. Med andra ord måste 360-innehåll ha högre upplösning än icke-360-video för att uppnå samma tänkbara kvalitet. Vi rekommenderar att du använder följande inställningar för adaptiv videoförinställning för 360-video:

* 720p, 2 500 kbit/s
* 1080p, 5 000 kbit/s
* 1440p, 6600 kbit/s

Observera dock att visning av video som är kodad med sådana högkvalitativa inställningar kräver en anslutning med hög bandbredd på slutanvändarens enhet.

## Interagera med Video360 Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer innehåller en uppsättning standardkontroller för användargränssnitt för videouppspelning, t.ex. uppspelnings-/pausknapp, tidsbubbla för videouppspelning, indikator för uppspelningstid/total tid, volymkontroll och helskärmsknapp. Alla dessa kontroller grupperas i kontrollfältet längst ned i visningsprogrammets användargränssnitt.

På enheter med pekskärm döljs volymkontrollen från användargränssnittet, eftersom det bara är möjligt att styra volymen med enhetens maskinvaruknappar.

När visningsprogrammet körs i popup-läge är inte knappen för helskärm tillgänglig i användargränssnittet.

Visningsprogrammet har också stöd för olika verktyg för delning av sociala medier. De är tillgängliga som en enda knapp i användargränssnittet, som utökas till ett delat verktygsfält när användaren klickar eller trycker på det. Verktygsfältet för delning innehåller en ikon för varje typ av delningskanal som stöds, till exempel Facebook, Twitter, e-postdelning, inbäddning av koddelning och länkdelning. När verktygen för e-postdelning, inbäddning eller länkdelning är aktiverade visas en modal dialogruta med ett motsvarande inmatningsformulär. När Facebook eller Twitter anropas dirigeras användaren om till en standarddelningsdialogruta från en tjänst för sociala medier. Dessutom pausas videouppspelningen automatiskt när ett delningsverktyg aktiveras. Delningsverktygen är inte tillgängliga i helskärmsläge på grund av säkerhetsbegränsningar i webbläsaren.

Visningsprogrammet stöder 360 videouppspelning på följande:

* VR-headset (som Oculus Go och Oculus Rift)
* VR HMD-montering (huvudmonterad bildskärm) (som Google-kartong)
* Enheter som inte är VR-aktiverade (som webbläsare på stationära datorer, surfplattor och mobiltelefoner som inte är anslutna till VR HMD-monteringar)

Ingen ytterligare konfiguration krävs för att visa 360-videoinnehåll på VR-headset. Visningsprogrammet identifierar automatiskt VR-headset och visar VR-knappen ovanpå videoinnehållet. När du aktiverar den här VR-knappen växlar videouppspelningen till VR-läge. Visningsprogrammet har endast stöd för VR-återgivning i webbläsare med WebVR-stöd.

För att kunna använda VR HMD-montering `Video360Player.vrrender` modifier måste anges till `1` i visningsprogrammets konfiguration, som tvingar stereoskopisk återgivning.

På VR-headset och VR HMD-monteringar sker en synpunktsförändring som svar på headsetets rörelse, men inte andra uppspelningskontroller tillhandahålls i VR-läge.

När man tittar på 360-video på enheter som inte är VR-aktiverade kan man använda musen, pekfunktionen eller tangentbordet för att styra videouppspelning och synvinkel.

Visningsprogrammet har stöd för både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Visningsprogrammet är fullt åtkomligt via tangentbordet. Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in Video360 Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en länk som när den är markerad öppnar visningsprogrammet i ett separat webbläsarfönster. I andra fall måste du bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup, inbäddning i fast storlek och responsiv designinbäddning.

Det går att bädda in flera videor på samma sida på både surfplattor och mobila enheter. Vanligtvis kan du bara spela upp en video i taget. När en användare börjar spela upp en video och sedan försöker spela upp en annan, pausas den första videon automatiskt. Videon som pausades automatiskt kommer ihåg den aktuella uppspelningstiden, så att användaren alltid kan återgå till den och återuppta uppspelningen. Det enda undantaget som den här regeln gäller är webbläsaren Chrome på Android™ 4.x-enheter, som kan spela upp videor parallellt.

**Om popup-läge**

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändrar storlek eller enhetens orientering ändras.

Det här läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med `window.open()` JavaScript-anrop, korrekt konfigurerat `A` HTML-element eller någon annan lämplig metod.

Vi rekommenderar att du använder en HTML-sida som inte finns i kartongen för popup-åtgärder. Den kallas [!DNL Video360Viewer.html] och den finns under [!DNL html5/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Du kan anpassa visuellt genom att använda anpassad CSS.

Här följer ett exempel på HTML som öppnar visningsprogrammet i ett nytt fönster:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet tar normalt bara upp en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designade sidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Den här metoden är det bästa alternativet för webbsidor med en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet måste ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`, utan att begränsa höjden, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den resurs som används. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor med flexibla ramverk för webbdesign som Bootstrap och Foundation.

Om webbsidan i annat fall anger både bredd och höjd för visningsprogrammets behållare `DIV`, fyller visningsprogrammet bara det området och följer den storlek som webbsidans layout ger. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definiera behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i huvudet HTML. Innan du kan använda visningsprogrammets API måste du se till att du inkluderar [!DNL Video360Viewer.js]. The [!DNL Video360Viewer.js] filen finns under [!DNL html5/js/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
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

   För att helskärmsfunktionen ska fungera i Internet Explorer måste du kontrollera att det inte finns några andra element i DOM som har en högre staplingsordning än platshållaren `DIV`.

   Följande är ett exempel på en definierad platshållare `DIV` element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att deklarera det för `.s7video360viewer` CSS-klass på översta nivån i absoluta enheter, eller med `stagesize` modifierare.

   Du kan ange storlek i CSS direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som senare tilldelas en förinställningspost för visningsprogrammet i Adobe Experience Manager Assets - On demand, eller skickas explicit med `style` -kommando.

   Se [Anpassa Video360 Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) om du vill ha mer information om hur du formaterar visningsprogrammet med CSS.

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på HTML-sidan:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Du kan ange `stagesize` modifierare i posten för visningsförinställning i AEM Assets - on-demand. Eller så kan du skicka det explicit med visarens initieringskod med `params` samling, eller som ett API-anrop enligt beskrivningen i avsnittet Kommandoreferens, så här:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.Video360Viewer` -klass, skicka all konfigurationsinformation till konstruktorn och anropa `init()` -metod i en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Objektet bör åtminstone ha `containerId` fält som innehåller namnet på visningsprogrammets behållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet.

   I det här fallet `params` objektet måste ha minst URL för bildserver som skickas som `serverUrl` och den ursprungliga tillgången som `asset` parameter. Med det JSON-baserade initierings-API:t kan du skapa och starta visningsprogrammet med en enda kodrad, en webbadress för videoservern som skickas som `videoserverurl` egenskap, ursprunglig tillgång som `asset` och interaktiva data som `interactivedata` -egenskap. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet, ring `init()` metod precis före stängning `BODY` eller på brödtexten `onload()` -händelse.

   Dessutom bör behållarelementet inte nödvändigtvis vara en del av webbsidans layout ännu. Den kan till exempel vara dold med `display:none` format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När det inträffar återgår visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar `init()` -metod. Exemplet förutsätter följande:

   * Visningsprograminstansen är `video360Viewer`.
   * Platshållarens namn `DIV` är `s7viewer`.
   * URL för bildservrar är `https://s7d9.scene7.com/is/image`.
   * Videoserverns URL är `https://s7d9.scene7.com/is/content`.
   * Tillgången är `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett fullständigt exempel på en enkel webbsida som bäddar in Video360 Viewer med fast storlek:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
