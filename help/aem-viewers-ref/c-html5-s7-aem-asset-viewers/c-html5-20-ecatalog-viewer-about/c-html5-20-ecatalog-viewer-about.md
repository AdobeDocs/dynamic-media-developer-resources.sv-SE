---
title: eCatalog
description: eCatalog Viewer är ett visningsprogram för en katalog som visar elektroniska broschyrer på uppslag eller sida för sida. Med eCatalog kan användare navigera i katalogen med hjälp av ytterligare element i användargränssnittet eller dedikerat miniatyrläge. Användarna kan också zooma in på alla sidor för att få bättre detaljer.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 8e243fa5-e375-41ce-8b49-2571023130c1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2158'
ht-degree: 0%

---

# eCatalog{#ecatalog}

eCatalog Viewer är ett visningsprogram för en katalog som visar elektroniska broschyrer på uppslag eller sida för sida. Med eCatalog kan användare navigera i katalogen med hjälp av ytterligare element i användargränssnittet eller dedikerat miniatyrläge. Användarna kan också zooma in på alla sidor för att få bättre detaljer.

>[!NOTE]
>
>Bilder som använder bildåtergivning (IR) eller användargenererat innehåll (UGC) stöds inte av det här visningsprogrammet.

Visningstyp 507.

Se [Systemkrav och krav](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Det här visningsprogrammet fungerar med kataloger och har stöd för valfria bildscheman och verktyg för delning via sociala medier. Den har zoomverktyg, katalognavigeringsverktyg, helskärmsstöd, miniatyrbilder och en valfri stängningsknapp. Visningsprogrammet har också stöd för verktyg för delning via sociala medier, utskrift, hämtning och Favoriter. Den är utformad för att fungera på stationära datorer och mobila enheter.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## Använda eCatalog Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Viewer representerar en JavaScript-huvudfil och en uppsättning hjälpfiler (en enda JavaScript-inkluderar alla Viewer SDK-komponenter som används av det här visningsprogrammet, resurser, CSS) som hämtats av visningsprogrammet under körning

Du kan använda eCatalog Viewer i popup-läge med en produktionsklar HTML-sida som finns i IS-Viewer eller i inbäddat läge, där den integreras med målwebbsidan med dokumenterat API.

Konfigurationen och skalningen liknar den för andra visningsprogram. All skalning görs med anpassad CSS.

Se [Kommandoreferens som är gemensam för alla visningsprogram - Konfigurationsattribut](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) och [Kommandoreferens som är gemensam för alla visningsprogram - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagera med eCatalog Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog Viewer stöder följande pekgester som är vanliga i andra mobilprogram.

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
   <td colname="col2"> <p> Väljer ny miniatyrbild i färgrutor. </p> </td> 
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
   <td colname="col2"> <p> Bläddrar igenom listan med katalogsidor om en bildruteövergång används. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lodrät dragning eller snärtning </p> </td> 
   <td colname="col2"> <p>När bilden är i ett återställningsläge utförs en inbyggd sidbläddring. </p> <p>När miniatyrbilder är aktiva rullas listan med miniatyrbilder. </p> </td> 
  </tr> 
 </tbody> 
</table>

Det går att aktivera en realistisk animeringseffekt för bläddring mellan katalogsidor. I så fall kan användaren hålla ned och dra ett sidhörn och vända på sidan.

Det här visningsprogrammet har även stöd för både pekrörelser och musindata på Windows-enheter med pekskärm och mus. Detta stöd är dock begränsat till webbläsarna Chrome, Internet Explorer 11 och Edge.

Det här visningsprogrammet är fullt åtkomligt via tangentbordet enligt beskrivningen i [Tangentbordstillgänglighet och -navigering](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Delningsverktyg för sociala medier med eCatalog Viewer {#section-eb575084a99647c3a9591f439f40b412}

eCatalog Viewer har stöd för verktyg för delning via sociala medier. De är tillgängliga som en knapp i huvudkontrollfältet som utökas till ett delningsverktygsfält när en användare klickar eller trycker på den.

Delningsverktygsfältet innehåller ikoner för varje typ av delningskanal som stöds, som Facebook, Twitter, e-postdelning, inbäddning av koddelning och länkdelning. När verktygen för e-postdelning, inbäddning eller länkdelning är aktiverade visas en modal dialogruta med ett motsvarande inmatningsformulär. När Facebook eller Twitter anropas omdirigeras användaren till en standarddelningsdialogruta från en social tjänst. Delningsverktygen är inte tillgängliga i helskärmsläge på grund av säkerhetsbegränsningar i webbläsaren.

## Bädda in eCatalog Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Olika webbsidor har olika behov av visningsprogrammets beteende. Ibland innehåller en webbsida en länk som, när den är markerad, öppnar visningsprogrammet i ett separat webbläsarfönster. I andra fall är det nödvändigt att bädda in visningsprogrammet direkt på värdsidan. I det senare fallet kan webbsidan ha en statisk sidlayout, eller använda responsiv design som visas på olika enheter eller för olika webbläsarfönsterstorlekar. För att tillgodose dessa behov har visningsprogrammet stöd för tre primära åtgärdslägen: popup-fönster, inbäddning med fast storlek och responsiv designinbäddning.

**Om popup-läge**

I popup-läge öppnas visningsprogrammet i ett separat webbläsarfönster eller på en separat flik. Det tar hela webbläsarfönsterområdet och justeras om webbläsaren ändrar storlek eller om en mobilenhets orientering ändras.

Popup-läget är det vanligaste för mobila enheter. Webbsidan läser in visningsprogrammet med `window.open()` JavaScript-anrop, korrekt konfigurerat `A` HTML-element eller någon annan lämplig metod.

Vi rekommenderar att du använder en färdig HTML-sida för popup-läge. I det här fallet anropas den [!DNL eCatalogViewer.html] och finns i [!DNL html5/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

Du kan anpassa visuellt genom att använda anpassad CSS.

Här följer ett exempel på HTML som öppnar visningsprogrammet i ett nytt fönster:

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**Om inbäddningsläge med fast storlek och responsivt designinbäddningsläge**

I det inbäddade läget läggs visningsprogrammet till på den befintliga webbsidan, som kanske redan har kundinnehåll som inte är relaterat till visningsprogrammet. Visningsprogrammet tar normalt bara upp en del av en webbsidas fastighet.

De viktigaste användningsområdena är webbsidor som är orienterade för datorer eller surfplattor, och även responsiva designade sidor som automatiskt anpassar layouten beroende på enhetstyp.

Inbäddning med fast storlek används när visningsprogrammet inte ändrar sin storlek efter den första inläsningen. Den här metoden är det bästa alternativet för webbsidor som har en statisk layout.

Inbäddning av responsiv design förutsätter att visningsprogrammet måste ändra storlek vid körning som svar på storleksändringen av behållaren `DIV`. Det vanligaste användningsområdet är att lägga till ett visningsprogram på en webbsida som använder en flexibel sidlayout.

I läget responsiv designinbäddning beter sig visningsprogrammet olika beroende på hur webbsidan ändrar storlek på sin behållare `DIV`. Om webbsidan bara anger behållarens bredd `DIV`, utan att begränsa höjden, väljer visningsprogrammet automatiskt höjden enligt proportionerna för den resurs som används. Med den här funktionen kan du vara säker på att resursen passar perfekt in i vyn utan utfyllnad på sidorna. Det här användningsexemplet är det vanligaste för webbsidor med responsiva layoutramverk som Bootstrap och Foundation.

I annat fall, om webbsidan anger både bredd och höjd för visningsprogrammets behållare `DIV`, fyller visningsprogrammet bara det området och följer den storlek som webbsidans layout ger. Ett bra exempel är att bädda in visningsprogrammet i en modal övertäckning, där storleken på övertäckningen anpassas efter webbläsarens fönsterstorlek.

**Inbäddning med fast storlek**

Du lägger till visningsprogrammet på en webbsida genom att göra följande:

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Anger visningsprogrammets storlek.
1. Skapa och initiera visningsprogrammet.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.

   Om du vill skapa ett visningsprogram måste du lägga till en script-tagg i huvudet HTML. Innan du kan använda visningsprogrammets API måste du se till att du inkluderar [!DNL eCatalogViewer.js]. The [!DNL eCatalogViewer.js] filen finns under [!DNL html5/js/] undermapp till din standarddistribution av IS-Viewer:

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

Du kan använda en relativ sökväg om visningsprogrammet distribueras på någon av Adobe Dynamic Media Classic-servrarna och den hanteras från samma domän. Annars anger du en fullständig sökväg till en av Adobe Dynamic Media Classic-servrarna som har IS-Viewer installerat.

Den relativa sökvägen ser ut så här:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
```

>[!NOTE]
>
>Referera endast till JavaScript för huvudvisningsprogrammet `include` på sidan. Referera inte till några ytterligare JavaScript-filer i webbsideskoden som kan hämtas av visningsprogrammets logik under körning. Ange särskilt inte direkt HTML5 SDK `Utils.js` biblioteket som läses in av visningsprogrammet från `/s7viewers` kontextsökväg (så kallad konsoliderad SDK) `include`). Orsaken är att platsen för `Utils.js` eller liknande visningsprogrambibliotek för miljön hanteras helt av visningsprogrammets logik och platsen ändras mellan visningsprogramversionerna. Adobe har inte äldre versioner av sekundära visningsprogram `includes` på servern.
>
>
>Det innebär att du skickar en direkt referens till valfritt sekundärt JavaScript `include` som används av visningsprogrammet på sidan avbryter visningsprogrammets funktioner i framtiden när en ny produktversion distribueras.

1. Definierar behållar-DIV.

   Lägg till ett tomt DIV-element på sidan där du vill att visningsprogrammet ska visas. DIV-elementet måste ha sitt ID definierat eftersom detta ID skickas senare till visningsprogrammets API.

   Platshållarens DIV är ett positionerat element, vilket innebär att `position` CSS-egenskapen är inställd på `relative` eller `absolute`.

   Följande är ett exempel på ett definierat DIV-platshållarelement:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Ange visningsprogrammets storlek

   Du kan ange den statiska storleken för visningsprogrammet genom att deklarera det för `.s7ecatalogviewer` CSS-klass på översta nivån i absoluta enheter, eller med `stagesize` modifierare.

   Du kan ange storlek i CSS direkt på HTML-sidan. Du kan också ange storlek i en anpassad CSS-fil för visningsprogrammet, som senare tilldelas till en post för visningsförinställningar i Dynamic Media Classic, eller skickas explicit med ett formatkommando.

   Se [Anpassa eCatalog Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) om du vill ha mer information om hur du formaterar visningsprogrammet med CSS.

   Följande är ett exempel på hur du definierar en statisk visningsstorlek på HTML-sidan:

   ```html {.line-numbers}
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Du kan ange `stagesize` modifierare i posten för visningsförinställning i Dynamic Media Classic. Eller så kan du skicka det explicit med visarens initieringskod med `params` samling, eller som ett API-anrop enligt beskrivningen i avsnittet Kommandoreferens, enligt följande:

   ```html {.line-numbers}
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initierar visningsprogrammet.

   När du har slutfört stegen ovan skapar du en instans av `s7viewers.eCatalogViewer` -klass, skicka all konfigurationsinformation till konstruktorn och anropa `init()` -metod i en visningsprograminstans. Konfigurationsinformation skickas till konstruktorn som ett JSON-objekt. Det här objektet har minst `containerId` fält som innehåller namnet på visningsprogrammets behållar-ID och kapslat `params` JSON-objekt med konfigurationsparametrar som stöds av visningsprogrammet. I det här fallet `params` objektet måste ha minst URL för bildserver som skickas som `serverUrl` och den ursprungliga tillgången som `asset` parameter. Med JSON-baserat initierings-API kan du skapa och starta visningsprogrammet med en enda kodrad.

   Det är viktigt att lägga till visningsprogrambehållaren i DOM så att visningsprogramkoden kan hitta behållarelementet med dess ID. I vissa webbläsare fördröjs skapandet av DOM tills webbsidan är slut. För maximal kompatibilitet kan du dock anropa `init()` metod precis före stängning `BODY` eller på brödtexten `onload()` -händelse.

   Samtidigt behöver behållarelementet inte nödvändigtvis vara en del av webbsidans layout ännu. Den kan till exempel vara dold med `display:none` format som tilldelats det. I det här fallet skjuter visningsprogrammet upp initieringsprocessen tills webbsidan återför behållarelementet till layouten. När den här åtgärden utförs återtas visningsprogrammet automatiskt.

   Följande är ett exempel på hur du skapar en visningsprograminstans, skickar de minsta nödvändiga konfigurationsalternativen till konstruktorn och anropar `init()` -metod. Exemplet förutsätter `eCatalogViewer` är visningsprograminstansen, `s7viewer` är namnet på platshållaren `DIV`; `https://s7d1.scene7.com/is/image/` är webbadressen för bildvisning, och `Viewers/Pluralist` är tillgången:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Följande kod är ett komplett exempel på en enkel webbsida som bäddar in eCatalog Viewer med fast storlek:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsiv designinbäddning med obegränsad höjd**

Med responsiv designinbäddning har webbsidan normalt någon typ av flexibel layout som bestämmer visningsprogrammets körningsstorlek `DIV`. I det här exemplet antar du att webbsidan tillåter visningsprogrammets behållare `DIV` för att ta 40 % av webbläsarens fönsterstorlek och låta dess höjd vara obegränsad. Den resulterande webbsidans HTML-kod ser ut så här:

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

Att lägga till visningsprogrammet på en sådan sida liknar inbäddning med fast storlek, men den enda skillnaden är att du inte behöver definiera visningsprogrammets storlek explicit.

1. Lägga till JavaScript-filen för visningsprogrammet på webbsidan.
1. Definierar behållar-DIV.
1. Skapa och initiera visningsprogrammet.

Alla stegen ovan är desamma som vid inbäddning med fast storlek. Lägg till behållaren `DIV` till den befintliga &quot; innehavaren&quot; `DIV`. Följande kod är ett komplett exempel. Du kan se hur visningsprogrammets storlek ändras när webbläsarens storlek ändras och hur visningsprogrammets proportioner matchar resursen.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Följande exempelsida visar mer verkliga användningsområden för responsiv designinbäddning med obegränsad höjd:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Flexibel storleksinbäddning med definierad bredd och höjd**

Vid inbäddning i flexibel storlek med definierad bredd och höjd är webbsidans format annorlunda. Det innebär att båda storlekarna kan anges för &quot; hållaren&quot; `DIV` och centrerar det i webbläsarfönstret. Dessutom anger webbsidan storleken på `HTML` och `BODY` till 100 %:

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
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Bädda in med Setter-baserat API**

I stället för att använda JSON-baserad initiering är det möjligt att använda set-based API och no-args-konstruktor. Med denna API-konstruktor tar inga parametrar och konfigurationsparametrar anges med `setContainerId()`, `setParam()`och `setAsset()` API-metoder med separata JavaScript-anrop.

I följande exempel visas inbäddning med fast storlek med set-based API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```
