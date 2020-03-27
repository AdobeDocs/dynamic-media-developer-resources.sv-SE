---
description: HTML5 Video360 Viewer är en 360-graders videospelare som spelar upp direktuppspelning och progressiv 360-video som är kodad i H.264-format, som levereras från Scene7 Publishing System eller från AEM Dynamic Media.
seo-description: HTML5 Video360 Viewer är en 360-graders videospelare som spelar upp direktuppspelning och progressiv 360-video som är kodad i H.264-format, som levereras från Scene7 Publishing System eller från AEM Dynamic Media.
seo-title: Video360
solution: Experience Manager
title: Video360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360{#video}

HTML5 Video360 Viewer är en 360-graders videospelare som spelar upp direktuppspelning och progressiv 360-video som är kodad i H.264-format, som levereras från Scene7 Publishing System eller från AEM Dynamic Media.

360-gradersvideor, även kallade engagerande videor eller sfäriska videor, är videoinspelningar där en vy i alla riktningar spelas in samtidigt och spelas in med en dubbelriktad kamera eller en samling kameror. Både en video och adaptiva videouppsättningar stöds. Visningsprogrammet har dessutom stöd för arbete med progressiv video och HLS-strömmar på en extern plats.

Rekommenderade proportioner för 360-video är 2:1. Spatial ljud stöds inte. Visningsprogrammet är utformat för att endast fungera med 360-video. Om du försöker spela upp en video som inte är 360 resulterar det i förvrängd videouppspelning.

Visningsprogrammet är utformat för att fungera både i webbläsare för datorer och mobila enheter med stöd för HTML5-video. Visningsprogrammet har stöd för valfria verktyg för delning via sociala medier.

Visningsprogrammet Video360 använder HTML5-direktuppspelad videouppspelning i HLS-format i standardkonfigurationen när det underliggande systemet stöder det. På system som saknar stöd för HTML5-direktuppspelning återgår visningsprogrammet till progressiv HTML5-videoleverans.

Visningstypen är 517.

## Demo-URL:er {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Systemkrav {#section-b7270cc4290043399681dc504f043609}

Se [Systemkrav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Använda Video360 Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-uppsättning innehåller alla SDK-komponenter för HTML5 Viewer som används av just detta visningsprogram, resurser, CSS) som hämtats av visningsprogrammet under körning.

HTML5 Video360 Viewer kan användas både i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer eller i inbäddat läge, där den integreras med målwebbsidan med dokumenterat API.

Konfigurationen och skalningen liknar den för andra visningsprogram som beskrivs i den här handboken. All skalning görs med CSS (Cascading Style Sheets).

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensamma för alla visningsprogram - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360-videoinnehåll kräver högre kodningsinställningar än standardvideo som inte är 360. Med andra ord måste 360-innehåll ha högre upplösning än icke-360-video för att uppnå samma tänkbara kvalitet. Vi rekommenderar att du använder följande inställningar för adaptiv videoförinställning för 360-video:

* 720p, 2 500 kbit/s
* 1080p, 5 000 kbit/s
* 1440p, 6600 kbit/s

Observera dock att visning av video som är kodad med sådana höga kvalitetsinställningar kräver en anslutning med hög bandbredd på slutanvändarens enhet.

## Interagera med Video360 Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer innehåller en uppsättning standardkontroller för användargränssnitt för videouppspelning, t.ex. uppspelnings-/pausknapp, tidsbubbla för videouppspelning, indikator för uppspelningstid/total tid, volymkontroll och helskärmsknapp. Alla dessa kontroller grupperas i kontrollfältet längst ned i visningsprogrammets användargränssnitt.

Observera att på enheter med pekskärm är volymkontrollen dold från användargränssnittet, eftersom det bara är möjligt att styra volymen med enhetens maskinvaruknappar.

När visningsprogrammet körs i popup-läge är inte knappen för helskärm tillgänglig i användargränssnittet.

Visningsprogrammet har också stöd för en mängd olika verktyg för delning av sociala medier. De är tillgängliga som en enda knapp i användargränssnittet, som utökas till ett delat verktygsfält när användaren klickar eller trycker på det. Verktygsfältet för delning innehåller en ikon för varje typ av delningskanal som stöds, till exempel Facebook, Twitter, e-postdelning, inbäddning av koddelning och länkdelning. När verktygen för e-postdelning, inbäddning eller länkdelning är aktiverade visas en modal dialogruta med ett motsvarande inmatningsformulär. När Facebook eller Twitter anropas omdirigeras användaren till en standarddelningsdialogruta från en tjänst för sociala medier. Dessutom pausas videouppspelningen automatiskt när ett delningsverktyg aktiveras. Delningsverktygen är inte tillgängliga i helskärmsläge på grund av säkerhetsbegränsningar i webbläsaren.

Visningsprogrammet har stöd för 360 videouppspelning på VR-headset (som Oculus Go och Oculus Rift), VR HMD-monteringar (med huvudmonterad bildskärm) (som Google Cardboard) och andra enheter som inte stöder VR (som webbläsare på stationära datorer, surfplattor och mobiltelefoner som inte är anslutna till VR HMD-monteringar).

Ingen ytterligare konfiguration krävs för att visa 360-videoinnehåll på VR-headset. Visningsprogrammet identifierar automatiskt VR-headset och visar VR-knappen ovanpå videoinnehållet. När du aktiverar den här VR-knappen växlar videouppspelningen till VR-läge. Visningsprogrammet har endast stöd för VR-återgivning i webbläsare med WebVR-stöd.

För att du ska kunna använda VR-HMD-monteringar måste modifieraren anges `Video360Player.vrrender` `1` i visningsprogrammets konfiguration, vilket tvingar stereoskopisk återgivning.

På VR-headset och VR HMD-monteringspunkten ändras som svar på headset-rörelser, men inte i VR-läge.

När man tittar på 360-video på enheter som inte är VR-aktiverade kan man använda musen, pekfunktionen eller tangentbordet för att styra videouppspelning och synvinkel.

Visningsprogrammet har stöd för både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Visningsprogrammet är fullt åtkomligt via tangentbordet. Se [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Bädda in Video360 Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en länk som öppnar visningsprogrammet i ett separat webbläsarfönster när användaren klickar på den. I andra fall måste du bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup, inbäddning i fast storlek och responsiv designinbäddning.

Det går att bädda in flera videor på samma sida på både surfplattor och mobila enheter. I de flesta fall kan bara en video spelas upp i taget. När en användare börjar spela upp en video och sedan försöker spela upp en annan, pausas den första videon automatiskt. Videon som pausades automatiskt kommer ihåg den aktuella uppspelningstiden, så att användaren alltid kan återgå till den och återuppta uppspelningen. Det enda undantaget som den här regeln gäller är i Chrome-webbläsaren på Android 4.x-enheter, som kan spela upp videor parallellt.

**Om popup-läge**

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändrar storlek eller enhetens orientering ändras.

Det här läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med hjälp av `window.open()` JavaScript-anrop, korrekt konfigurerade `A` HTML-element eller någon annan lämplig metod.

Vi rekommenderar att du använder en HTML-sida som inte är tillgänglig för popup-åtgärder. Den anropas [!DNL Video360Viewer.html] [!DNL html5/] och finns under undermappen till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Du kan anpassa visuellt genom att använda anpassad CSS.

Följande är ett exempel på HTML-kod som öppnar visningsprogrammet i ett nytt fönster:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet tar normalt bara upp en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designade sidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Det här är det bästa alternativet för webbsidor som har en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet kan behöva ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`utan begränsningar, väljer visningsprogrammet automatiskt dess höjd enligt proportionerna för den resurs som används. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor med flexibla ramverk för webbdesign som Bootstrap, Foundation och så vidare.

Om webbsidan ställer in både bredd och höjd för visningsprogrammets behållare `DIV`fyller visningsprogrammet bara det området och följer den storlek som webbsidans layout ger. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållaren `DIV`.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i HTML-huvudet. Innan du kan använda visningsprogrammets API måste du ta med [!DNL Video360Viewer.js]. Filen [!DNL Video360Viewer.js] finns under undermappen [!DNL html5/js/] för din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Du bör bara referera till JavaScript- `include` filen för huvudvisningsprogrammet på sidan. Du bör inte referera till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körningen. Referera inte direkt till HTML5 SDK- `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökvägen (så kallad konsoliderad SDK `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversioner. Adobe sparar inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att om du skickar en direkt referens till ett sekundärt JavaScript `include` som används av visningsprogrammet på sidan så bryts visningsprogrammets funktion i framtiden när en ny produktversion distribueras.

1. Definierar behållaren `DIV`.

   Lägg till ett tomt `DIV` element på sidan där du vill att visningsprogrammet ska visas. Elementet måste ha ett definierat `DIV` ID eftersom detta ID skickas senare till visningsprogrammets API. DIV har den storlek som anges via CSS.

   Platshållaren `DIV` är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   För att helskärmsfunktionen ska fungera i Internet Explorer måste du kontrollera att det inte finns några andra element i DOM som har en högre staplingsordning än platshållaren `DIV`.

   Följande är ett exempel på ett definierat platshållarelement `DIV` :

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att antingen deklarera den för CSS-klassen på den `.s7video360viewer` översta nivån i absoluta enheter eller genom att använda `stagesize` modifierare.

   Du kan lägga in storleksändring i CSS direkt på HTML-sidan eller i en anpassad CSS-fil för visningsprogrammet, som sedan tilldelas till en förinställningspost för visningsprogram i AEM Resurser - on demand, eller skickas explicit med `style` kommando.

   Se [Anpassa Video360 Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) för mer information om hur du formaterar visningsprogrammet med CSS.

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på HTML-sidan:

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Du kan ställa in modifieraren i posten för visningsförinställningar i AEM Resurser - on-demand. `stagesize` Eller så kan du skicka det explicit med initieringskoden för visningsprogrammet med `params` samlingen, eller som ett API-anrop enligt beskrivningen i avsnittet Kommandoreferens, så här:

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   En CSS-baserad metod rekommenderas och används i det här exemplet.

1. Skapa och initiera visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.Video360Viewer` klassen, skickar all konfigurationsinformation till konstruktorn och anropar `init()` metoden för en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet ska åtminstone ha ett `containerId` fält som innehåller namnet på visningsprogrammets behållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet.

   I det här fallet måste objektet ha minst den URL-adress för bildservrar som skickas som `params` egenskap och den ursprungliga resursen som `serverUrl` `asset` parameter. Med det JSON-baserade initierings-API:t kan du skapa och starta visningsprogrammet med en enda kodrad, en webbadress för videoservern som skickas som `videoserverurl` egenskap, en första resurs som `asset` parameter och interaktiva data som `interactivedata` egenskap. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet anropar du metoden precis före den avslutande `init()` taggen eller på body- `BODY` `onload()` händelsen.

   Dessutom bör behållarelementet inte nödvändigtvis vara en del av webbsidans layout ännu. Den kan till exempel vara dold med hjälp av ett format som är tilldelat den. `display:none` I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När det inträffar återgår visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar `init()` metoden. Exemplet förutsätter följande:

   * Visningsprograminstansen är `video360Viewer`.
   * Platshållarens namn `DIV` är `s7viewer`.
   * URL:en för bildvisning är `https://s7d9.scene7.com/is/image`.
   * Videoserverns URL är `https://s7d9.scene7.com/is/content`.
   * Tillgången är `Viewers/space_station_360-AVS`.

   ```
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

   ```
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

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets behållares körningsstorlek `DIV`. I följande exempel kan du anta att webbsidan tillåter att visningsprogrammets behållare tar 40 % av webbläsarens fönsterstorlek, och låter dess höjd vara obegränsad. `DIV` HTML-koden för webbsidan ser ut så här:

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

Alla steg ovan är desamma som med inbäddning med fast storlek. Lägg till behållar-DIV i befintlig `"holder"` DIV. Följande kod är ett komplett exempel. Lägg märke till hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```
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

Om det finns responsiv inbäddning med definierad bredd och höjd är webbsidans format annorlunda. Det ger DIV:n båda storlekar och centrerar den i webbläsarfönstret. `"holder"` Dessutom ställer webbsidan in storleken på elementet `HTML` och `BODY` elementet till 100 procent.

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

Resten av inbäddningsstegen är identiska med stegen som används för responsiv inbäddning med obegränsad höjd. Följande exempel visas:

```
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

I stället för att använda JSON-baserad initiering kan du använda set-based API och no-args-konstruktor. Om du använder denna API-konstruktor används inga parametrar och konfigurationsparametrar anges med hjälp av `setContainerId()`-, `setParam()`och `setAsset()` API-metoder med separata JavaScript-anrop.

I följande exempel visas hur du använder inbäddning med fast storlek med det inställningsbaserade API:t:

```
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

